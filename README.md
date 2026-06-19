# Population dynamics

Simulates the evolution of a defensive trait in a population through random mutations, and the Lotka-Volterra model for predator-prey dynamics.

# 1. Defensive traits

This model investigates the evolution of a defensive trait through mutations in a population. As a higher defensive trait increases the probability of survival, the mean score increases with time by random mutations. I have implemented a "cost" - a higher defensive trait decreases the offspring, as seen in nature (it takes more energy to develop, for example). As shown in the model, the mean of the normal curve tends to stay just below this point.

# 2. Lotka-Volterra model

The Lotka-Volterra model relates to the population dynamics of a predator species and a prey species, and is represented by the first order differential equations 

$$\frac{dx}{dt}= \alpha x-\beta xy$$
$$\frac{dy}{dt}=-\gamma y+\delta xy$$

for $x,y$ the populations of prey and predators and $\alpha, \beta, \gamma, \delta$ parameters representing prey growth rate, predation rate, predator death rate and reproduction rate respectively.

The graph shows that the populations of predators and prey tend to oscillate - as the prey population grows, the growth rate of the predator population increases and therefore the predator population grows as well. This increased predator population decreases the prey population, which reduces the availability of food and therefore decreases the predator population as there is no longer enough prey to sustain a large population. At a low predator population, the prey population then rebounds - repeating the cycle.

For $x'=x(\alpha (x- \beta y)$ and $y' = y(-\gamma + \delta x)$ the fixed points are at $(0,0)$ and at $(\frac{\gamma}{\delta}, \frac{\alpha}{\beta})$. With the parameters I've used this is x=30, y=20.

Using Euler's method for plotting introduced an error over time. For this system, the fixed point (not the origin) is a centre and therefore trajectories follow closed loops, however in the phase portrait with Euler's we see this slowly diverging. Using RK4 to plot gives much better results and the phase portrait reflects this. Additionally, the value $V = \delta x - \gamma log(x) + \beta y - \alpha log(y)$ should be constant - this is much more constant with RK4 than Euler's.

## Logistic prey growth

To make the model more realistic I've implemented logistic prey growth - a limit on how large the prey can grow, based on food available. This changes the nature of the fixed point, as now the phase portrait is a stable spiral. After linearising at the fixed point, the eigenvalues of the Jacobian are $\frac{-\gamma \alpha}{\delta k} \pm \sqrt{\alpha \gamma (\frac {\alpha \gamma}{\delta k} - 1)}$. As these are all positive constants, $Re(\lambda) < 0$. $k$ is usually much greater than all other constants, so the square root will be imaginary - therefore, this is a stable spiral.

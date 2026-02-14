# Population dynamics

Simulates the evolution of a defensive trait in a population through random mutations, and the Lotka-Volterra model for predator-prey dynamics.

# 1. Defensive traits

This model investigates the evolution of a defensive trait through mutations in a population. As a higher defensive trait increases the probability of survival, the mean score increases with time by random mutations. I have implemented a "cost" - a higher defensive trait decreases the offspring, as seen in nature (it takes more energy to develop, for example). As shown in the model, the mean of the normal curve tends to stay just below this point.

<img width="490" height="489" alt="clipboard" src="https://github.com/user-attachments/assets/901d27c4-5dd6-4f20-bba0-2cb84da69314" />


# 2. Lotka-Volterra model

The Lotka-Volterra model relates to the population dynamics of a predator species and a prey species, and is represented by the first order differential equations 

$$\frac{dx}{dt}= \alpha x-\beta xy$$
$$\frac{dy}{dt}=-\gamma y+\delta xy$$

for $x,y$ the populations of prey and predators and $\alpha, \beta, \gamma, \delta$ parameters representing prey growth rate, predation rate, predator death rate and reproduction rate respectively.

The graph shows that the populations of predators and prey tend to oscillate - as the prey population grows, the growth rate of the predator population increases (there is plenty of food available) and therefore the predator population grows as well. This increased predator population decreases the prey population, which reduces the availability of food and therefore decreases the predator population as there is no longer enough prey to sustain a large population. At a low predator population, the prey population then rebounds - repeating the cycle.

<img width="841" height="525" alt="clipboard1" src="https://github.com/user-attachments/assets/8cf80cd0-13e0-41df-9bed-58a2a404c6d6" />

<img width="532" height="547" alt="clipboard2" src="https://github.com/user-attachments/assets/ebf743db-67f3-4384-b882-3122486ea669" />



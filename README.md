# Population dynamics

Simulates the evolution of a defensive trait in a population through random mutations, and the Lotka-Volterra model for predator-prey dynamics.

# 1. Defensive traits

This model investigates the evolution of a defensive trait through mutations in a population. As a higher defensive trait increases the probability of survival, the mean score increases with time by random mutations. I have implemented a "cost" - a higher defensive trait decreases the offspring, as seen in nature (it takes more energy to develop, for example). As shown in the model, the mean of the normal curve tends to stay just below this point.

<img width="490" height="489" alt="clipboard" src="https://github.com/user-attachments/assets/901d27c4-5dd6-4f20-bba0-2cb84da69314" />


# 2. Lotka-Volterra model

The Lotka-Volterra model relates to the population dynamics of a predator species and a prey species, and is represented by the first order differential equations $$\frac{dx}{dt}= \alphax-\betaxy$$ $$\frac{dy}{dt}=-\gammay+\deltaxy$$ for $x,y$ the populations of prey and predators and $\alpha, \beta, \gamma, \delta$ parameters representing prey growth rate, predation rate, predator death rate and reproduction rate respectively.


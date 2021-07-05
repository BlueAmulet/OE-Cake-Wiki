OE-Cake does not simulate temperature in the traditional sense, of having a "heat" value associated with each particle. The Hot materials are basically just on/off and have no difference except how they are treated by other particles. However by using large masses of particles it is possible to use statistics to simulate certain kinds of particle behaviors that resemble temperature effects in real life.

Setting *resistanceCoefficient* in the [Parameters](/Parameters.md "Parameters") to a small negative number (start at -0.001) gives particles the property of self-motion. This causes Gas particles to always move and push, allowing them to inflate Elastic balloons for example. By changing how negative the value is you can change how quickly the particles "heat up". By changing *maxSpeed* you can change how "hot" the particles are allowed to get. In this mode, Water can evaporate if a particle randomly achieves enough speed to fly away from the liquid mass. [Anti-Viscous](/Viscous.md "Viscous") can also be used to simulate thermal motion in particles.

Using this technique it is possible to study Brownian motion in gasses and run more accurate gas pressure simulations.

If we are relating particle motion to temperature, It is generally impossible for any movable (ie. non-Wall) particle to reach absolute zero due to [quantum mechanical](/Quantum%20Physics.md "Quantum Physics") effects.

[Save-file analysis](/.oec%20File.md ".oec File") has revealed that particles under pressure actually develop higher temperatures. This is responsible for the [Sonic Boom](/Sonic%20Boom.md "Sonic Boom") reaction of particles under [pressure](/pressure.md "pressure").

![Yellow viscous, mixed with fuel on fire, and floating on Water.](/images/Viscous.jpg "fig:Yellow viscous, mixed with fuel on fire, and floating on Water.")
**Viscous** is a strange green gel that vaguely resembles toothpaste. Viscous is thicker and flows much slower than normal elements. When mixed with another material it is useful to make them have more friction, for example [Tensile](/Tensile.md "Tensile") + Viscous to make honey, or making Rigid/Wall less slippery. Counterintuitively, it also acts as a decent lubricant because it gets stuck where it is put and makes a layer between objects, and the individual particles are permitted to rotate which creates an interface between the surfaces.

Viscous also passes on it's damping properties to the rotation of the individual particles, converting shear forces to dampened particle rotation. Two surfaces sliding past each other on a thin layer of Viscous will actually drag the particles into rotating, one of the few materials in the game to have this behavior, providing damping between surfaces with nearly 0 particle thickness. This permits even tiny quantities of Viscous to have notable damping. The influence of individual particles can be considered a [quantum mechanical](/Quantum%20Physics.md "Quantum Physics") effect.

## Uses

### Anti-Viscous

There is a special material called Anti-Viscous. This is created by setting *viscosityCoefficient* in the [Parameters](/Parameters.md "Parameters") to a negative value. This makes Viscous want to flow more instead of less, and is useful for creating some very strange materials. Anti-Viscous can make rivers that flow uphill and extra-slippery materials. Adding Viscous to a liquid (such as Water or Gas) and setting the coefficient to a small negative number is a highly effective method of counteracting OE-Cake's inherent internal friction in fluids and increasing turbulence/Reynolds number. Viscosity is a time-dependent value meaning it's effect is relative to how much energy it is exposed to in a given amount of time. Anti-Viscous is very capable of "going nova" in that the reaction is extremely self-fulfilling, a tiny amount of energy input (such as jiggling a blob with your mouse or letting it fall to the ground) is enough to kick-start all the rest of the Anti-Viscous into a massive chain reaction. Anti-Viscous is fairly self-stable when the mass is at total rest, however negative values too high will make the material susceptible to self-reacting from [quantum](/Quantum%20Physics.md "Quantum Physics") Brownian motion, the natural microscopic vibration every particle possesses. OE-Cake has a certain amount of intentional damping added by the *dampingFlag* Parameter, which is designed to smooth out particle motion to look less "spiky" and random. This can be disabled but there is still some inherent quantum damping in all particle motion that is capable of containing Anti-Viscous with a mild negative value, since it costs a fairly large amount of energy just to move particles around this is sufficient to prevent mild Anti-Viscous nova reactions and create self-stable flowing structures.

### Nova Viscous

Viscous with the default settings has an unusual property. Under the right conditions, Viscous explodes into a swarm in a similar way to burning [Powder](/Powder.md "Powder"). When a Viscous particle is compressed against a non-Viscous particle with enough speed and force, for example by an explosion or heavy hammer, Viscous "glitches out" and explodes, sending particles flying away at *maxSpeed*. Exactly how and why this reaction occurs is not currently well known.

My theory is that, within the programming of Viscous, there is a part that was not designed to handle absolute maximum possible pressure. Under certain circumstances, something happens to individual particles to make them do something different. The reaction most commonly seems to happen between Gas and Viscous, but under unusual conditions I have seen Viscous react with Wall. I think maybe there is an [Integer Overflow](https://en.wikipedia.org/wiki/Integer_overflow) that suddenly snaps the particles into a high-speed state. The reaction is too fast to easily see exactly what happens between two particles, but it seems as if the Viscous snaps onto particles and orbits them for a split second, then catapults off in a random direction. The strange part is that it doesn't just happen once, the Viscous particles stay in this agitated state for an extended period of time, sometimes forever. It's almost as if they hold momentum. This glitched behavior can be explained by [quantum physics](/Quantum%20Physics.md "Quantum Physics"). Nova Viscous may be the only candidate suitable for use in creating a [quantum bomb](/Quantum%20Bomb.md "Quantum Bomb"). Allegedly a [Compressed Particle Gun](/Compressed%20Particle%20Gun.md "Compressed Particle Gun") or [Spin-Charged Elastic](/Spin-Charged%20Elastic.md "Spin-Charged Elastic") is capable of creating Nova Viscous, as hypothesized in the Compressed Particle Gun article, which may provide an avenue for exploration the intentional production of Nova Viscous.

<figure>
<img src="/images/OEcake%20Kittystorm" title="Example of Nova Viscous in action" width="335" alt="Example of Nova Viscous in action" /><figcaption aria-hidden="true">Example of Nova Viscous in action</figcaption>
</figure>

[Category:Materials](/CategoryMaterials.md "Category:Materials")
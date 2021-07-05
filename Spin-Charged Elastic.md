!["Crosses" showing warps and distortions caused by the Elastic Particles inside the "lattice" with spin](/images/Picture%207.png "fig:"Crosses" showing warps and distortions caused by the Elastic Particles inside the "lattice" with spin")**Spin-Charged Elastic (SCE)** is a special form of [Elastic](/Elastic.md "Elastic") that has unique properties and uses. It is caused by either a glitch or a limitation of the game engine. The **Rotating Elastic glitch** is a different form of SCE, known as Type B.

### [Depolarized](/Polarization.md "Polarization") Elastic

This is the default state of Elastic drawn by a normal tool. It is a lattice of particles that are perfectly aligned and spaced with zero rotation or spin value. This configuration responds to forces by stretching or compressing in a uniform manner and trying to return to its original shape. Each particle is connected by an invisible "join" which can be thought of as a fundamental force, like magnetism. The force binding Elastic particles together has a surprising analogy to the [nuclear force](https://en.wikipedia.org/wiki/Nuclear_force) in our world, which is responsible for the orbits of neutrons and protons in an atom. Both forces can either push or pull on the particles depending on the distance between them.

Particles in Elastic can rotate like a compass, they have North South East and West poles, though all rotation is relative since we can't really detect what direction a particle is pointing. Freshly drawn elastic will have all poles of the particles aligned North, or at least that is a useful psychological tool. Elastic particles can bind at any orientation and then resist rotation equivalent to *elasticCoefficient*. Using the Replace tool can often result in spin-charged particles because the Replace tool resets particle spin, see the section called **Degaussing** below. [Glass Elastic](/Glass%20Elastic.md "Glass Elastic") is a form of polarized Elastic where the lattice shape has been deformed but the polarity of individual particles is preserved.

## Polarized Elastic

The particles in Elastic can have their polarity changed by external forces, game mechanics or glitches. Since the particles are connected by a force that can transmit rotation, the combined influence of particles can create unique results.

### Type A: Random

The material traditionally known as "Spin Charged Elastic" is created when each individual particle is given a random rotation, causing Norths and Souths to cross and subjecting the physical lattice alignment of the shape to an extreme amount of internal force. This causes the collection of particles to warp and shake uncontrollably as alignments randomly flip between stable states and chaotically interact with other states.

Generally SCE Type A is created by dissociating the Elastic particles from their lattice shape, subjecting each individual particle to random rotation, then reassociating the particles into a shape again. After the elastic returns to it's normal shape or the charging force is removed, each twisted particle will not be able to return to an untwisted state because it is has been frozen into position by its neighbors, leading to the visible behavior.

Type A Spin-Charged Elastic can be made by:

-   setting elasticCoefficient in the [Parameters](http://oecake.wikia.com/wiki/Parameters) to a value greater than 1.5, letting the elastic glitch out for about 30 seconds, then setting elasticCoefficient back to 0.5 - This sets the Elastic's internal repulsion to a high value, exploding the particles which remain tied to each other while glitching out randomly, then setting the internal force back to normal. Each particle returns to its original neighbors, but with an added spin value.
-   setting elasticCoefficient to 0, sloshing the particles around a bit, then setting back to 0.5 - this temporarily disables Elastic physics, turning the particles into liquid. As they contact each other they will gently spin. Setting the value back will suck the particles back into a shape again but with significant internal stresses.

<!-- -->

-   with staticPressure based [Teleportation](/Teleportation.md "Teleportation") - Certain staticPressure settings cause severe force glitches. This can cause particles of Elastic to get cannonballed around the screen fast enough to spin-charge at least some of the particles
-   collisions with [Compressed particles](/Compressed%20particle.md "Compressed particle") - Compressed particles have enough mass to glitch out collision physics. Sometimes throwing a very dense Compressed Particle at a block of Elastic will Home Run some Elastic particles and spin charge them. This technique usually results in a largely untouched blob of Elastic with a few tainted particles.
-   contact with materials made at standardDistance [Parameter](/Parameters.md "Parameters") \< 0.2, and generally any material that generates [Force Fields](/Force%20Field.md "Force Field") - Super-dense materials or extreme speeds can also impact Elastic particles hard enough to put a kink in the lattice

### Type B: Correlated

The second type of Elastic is responsible for the **Rotating Elastic glitch** that happens if you try to draw on Elastic that has rotated from its original orientation. Some OE-Cake programming knowledge for you - Elastic and Rigid have slightly different programming than all of the other materials in the game which are mostly fluids. The particles in these materials are the same as any other, but they are "correlated" together so they share forces. When you hit a piece of Rigid, all of the particles change direction at the same time, so does Elastic in a delayed way. Any time you draw a shape of RIgid or Elastic, the particles drawn with that particular click of the mouse become brothers and stick together for life. Certain types of modification will reset the spin-[polarization](/polarization.md "polarization") of the group while ignoring rotation, such as being drawn on with the Pencil tool. When this happens, the position of each particle stays the same, but its spin value is reset to 0 with North pointing straight up.

Elastic is highly susceptible to this problem - rotating a block of Elastic by 90 degrees and then re-polarizing the block will result in every individual particle being given a 90 degree spin-charge, perfectly evenly distributed. Since each particles charge is highly correlated instead of being random, the block immediately begins rotating with an amount of force proportional to the degree of twist and the strength of elasticCoefficient. Elastic can also be harmed if any Rigid it is connected to is polarized. This effectively means that any and all creations made in OE-Cake using Elastic or RIgid **<u>MUST</u>** be made in a single pass with the game paused, to ensure every single particle has absolutely 0 spin-charge.

SCE Type B has some interesting properties that could be quite useful for creations. A spin-charged block of Elastic is highly efficient at producing rotational energy and could serve as a rotational replacement for Jet in engines. Type B produces infinite energy and also allows the user to tune the rotational power of their device to any degree without a Parameters change, allowing a greater variety in force-generating devices.

### Degaussing Elastic

#### Replace Method

Charged Elastic can be uncharged/repolarized by painting the particles with the Bucket or Replace tool, which resets the particle spin values. However they are not able to regenerate the lattice alignment so any deformation is permanent.

#### Robert's Comb

![Robert's Comb being used on a save file in [regex101](https://regex101.com/)](/images/Regex101.png "fig:Robert's Comb being used on a save file in regex101")
It's possible to "comb" spin-charged elastic with save file editing. Because SCE is caused by extremely high rotation values, it can be fixed by setting rotation values to 0. This can be done manually, but is much faster if done with regular expressions.

To use Robert's Comb, follow these steps:

-   Find a regex replace tool. There are lots of these tools in text editors or online. One such tool is [regex101](https://regex101.com/).
-   Open the [.oec file](/.oec%20File.md ".oec File") containing the SCE you want to comb in a text editor, such as Notepad.
-   Copy the entire file into the input area of whatever regex tool you're using.
-   Activate "substitution" or "replace" mode, and enter the following expressions:
    -   `(p 10 .+) \S+ \S+ \S+ \n` as the expression
        -   In some cases, you'll need `/(p 10 .+) \S+ \S+ \S+ \n/g`
    -   and `$1 0 0 0 \n` to replace/substitute.
-   Copy the output back into the .oec file.
-   Open the .oec file in [OE-Cake](/OE-Cake.md "OE-Cake"). The elastic should be restored back to normal.

Robert's Comb preserves the lattice of the elastic and removes any deformations, as long as the elastic hasn't been modified in any other way since the comb was applied.

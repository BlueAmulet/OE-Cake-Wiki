<img src="/images/Screen%20Shot%202018-11-13%20at%209.06.47%20PM.png" title="fig:Notice how all Rigid particles are facing the same direction as the block, and that the String particles did not rotate. " width="220" height="220" alt="Notice how all Rigid particles are facing the same direction as the block, and that the String particles did not rotate. " />
All individual particles have a **spin value,**separate from their **rotation value,**as one of their properties. I have decided to call this **polarization**. Particles can rotate as part of a group, but they can also have an offset relative to that group, a second-order rotation. Particle rotation in OE-Cake has some unusual effects. Basic particle physics does not seem to be hugely affected by whether particles are rotated or not. Most materials have no special rotation behavior - Water particles are always polarized straight up and down and never rotate. Rigid particles rotate as a solid. Elastic particles rotate in response to the object's deformation. Mochi, Tensile, and Powder, three materials with wildly different programming, have particles which are always polarized straight up and down. For this reason I believe most particle interaction does not take in to account rotation. Particles can spin in response to an external force, or rotate continuously at a fixed rate. **Spin** has momentum but no friction.

### Materials

[String](/String.md "String"), [Elastic](/Elastic.md "Elastic"), and [Viscous](/Viscous.md "Viscous") have unusual rotational behavior.

String particles behave as a solid but do not pay attention to rotation, even when connected to other particles such as Rigid. The joins in a String lattice seem to attempt to maintain a certain radial distance from each other, in both compression and tension, though it is difficult to play pool with a rope as the saying goes. String is always polarized in the direction it was created, except when connected to Elastic, then each particle will follow the rotation of the Elastic particle it is connected to. If String is created from particles with a 45 degree rotation (for example, using Bucket to convert a rotated Rigid block) the particles will always maintain that orientation no matter what. Viscous is also capable of "touching" String particles and causing them to rotate through viscous drag.

The joins in a lattice of Elastic attempt to maintain a certain distance and orientation from each other. This increases the internal stiffness of the material. Particle rotation as well as particle distance is used to calculate deformation, which allows single strands of Elastic to have inherent stiffness, unlike a strand of String. Elastic depends on each particle being polarized in the same direction, if connected particles have different rotations the [spin-charged Elastic](/Spin-Charged%20Elastic.md "Spin-Charged Elastic") glitch happens. The net rotation of each particle will be infinitely added into the solid causing it rotate under it's own power. This infinite force could be used to power creations.

Viscous particles rotate relative to their direction of flow, as if they were tumbling. When Viscous glitches out, the particles rotate more and more intensely until they go nova. Viscous is able to "touch" String particles and cause them to rotate. Under certain circumstances Viscous can start a particle rotating and not stop it, spin-charging the particle and causing the particle to rotate freely forever. The material String + Viscous is highly unusual, the particles seem to rotate relative to the forces applied, and then stay there. Perhaps SV could be used as some kind of memory material?

### Electrical Conduction

Electrical conduction in OE-Cake also has some highly direction-dependent effects. Conduction seems to work best from NE to SW on the screen, independent of Gravity angle. Conduction is also strongly affected by the rotation of particles, though exactly why is still not known.

### Supernova Effect

When the sound barrier in OE-Cake is broken, the particles go nova cause cause a cascading reaction. Usually the force dissipates, but if you generate enough force and contain it to a small enough area, [new physics](/Super-dense%20material.md "Super-dense material") occur. The standard rules of particle collision are broken and unusual things happen, the exact reason of which is not known. The strange lines are likely to be an artifact of how the game handles maximum pressure, and the lines are probably from the randomization engine not being able to keep up with the onslaught of angry particles, bleeding the pool dry and causing the randomness to be more correlated. This effect is not directly related to particle rotation, but it is another anisotropic phenomena in OE-Cake so it sorta fits under this topic.
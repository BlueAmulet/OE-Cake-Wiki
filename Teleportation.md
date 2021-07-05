**Teleportation** is a [quantum effect](/Quantum%20Physics.md "Quantum Physics") that is a result of how particles move in the game.

Particle movement often seems smooth, but it is actually the result of particles moving in "steps". When speeds are low, the forces between particles is sane. When speeds and pressures become too high, it is possible for a particle to move farther than an entire particle in a single frame. This causes shapes to slide through each other and for obstacles to be skipped over entirely.

The [Sonic Boom](/Sonic%20Boom.md "Sonic Boom") reaction is a consequence of particles teleporting under high [pressure](/pressure.md "pressure"). My theory is that through random chance, particles will essentially land right on top of one another, and if their positions are truly identical or even just extremely close, as the distance between them will approach 0 the reaction force trying to separate them will approach infinity. The critical pressure is the point where particles can teleport by 1 particle length, which permits their "nucleus" to become extremely close for a single frame, generating a proportional but unrealistic level of force, causing there to now be 2 particles at teleporting speed. In a cascading reaction the chain reaction of force spreads and consumes more particles.

*maxSpeed* in the [Parameters](/Parameters.md "Parameters") puts a hard cap on how far particles can travel in a single frame, allowing one to adjust the permissible level of teleportation the simulation can handle. *timeStepsPerFrame* also has an effect on the likelihood for particles to teleport.  

## Applications

Teleporting [Rigid Axis](/Rigid%20Axis.md "Rigid Axis") in OE-Cake is made possible by setting the [Parameters](/Parameters.md "Parameters") staticPressureFlag to 1, and staticPressureCoefficient to a very high number (1\<x≤100), and placing a square or rectangle of Rigid Axis inside a wall. The Axis will teleport to another place on the screen, then it will teleport back inside the wall, then back to the other place on screen.

Elastic Teleportation. In the [Parameters](/Parameters.md "Parameters") Window, change ElasticCoefficient to -0.5. All elastic materials will disappear. When ElasticCoefficient is turned back to the default value of 0.5, all of the elastic pieces will warp onto the screen. If the elasticCoefficient is left at -0.5 for too long, every particle in the lattice of the [Elastic](/Elastic.md "Elastic") object(s) will gain spin when the Parameter is turned back to 0.5. The elastic object will be Spin-Charged (see [Spin-Charged Elastic](/Spin-Charged%20Elastic.md "Spin-Charged Elastic")) , and every individual particle spins and distorts the overall shape of the object. The object permanently shakes and vibrates uncontrollably as a result.
As long as it is attached to the Elastic, An object will teleport with it.

### ζ-Space

The ζ-Space (or Zeta-Space) is a hypothetical "dimension" outside the sandbox. When the Drain flag is disabled, it is generally impossible for particles to exit the visible area. The area outside both generates and requires extreme forces for any particles to find themselves out there.

Under [hypercritical pressure](/Supercriticality.md#Hypercriticality "Supercriticality"), particles can be pushed into the ζ-space. This can be seen by pausing the simulation and enlarging the window, revealing particles that were out of bounds.

By modifying Parameters it is possible to set boundary variables in such a way that there is no allowed position for particles. You could set the left bounds farther to the right than the right bounds. You can set *boundsRadius* to increasingly large numbers. It is possible to create a nearly circular playing field in this manner. when the radii become so large they overlap, "positive" Zeta space is formed within the visible window, causing particles to teleport around their junction and be accelerated. Continuing to enlarge *boundsRadius* can create an environment where particles are constrained by the four corners which produces yet more unusual behavior, without crashing the game.

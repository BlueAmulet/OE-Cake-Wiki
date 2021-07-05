**Pressure** is a force applied over an area. Enabling *staticPressureFlag* in the [Parameters](/Parameters.md "Parameters") simulates more realistic pressure.

OE-Cake simulates pressure emergently as the result of particle velocity, and a fixed particle mass and repulsion coefficient. Since particles have weight and want to push each other away, the velocity at which two particles collide generates a proportional reaction force. This means that fluids under pressure actually begin vibrating at high speed, and the fact they push back is due to all the particles colliding with the walls and each other.

Changing the *standardDistace* Parameter allows particles to be drawn at precise distances, allowing one to set fluids to arbitrary pressures and solids to arbitrary densities. Particle density has a dramatic effect on [electricity](/Electrical%20Conduction.md "Electrical Conduction").

## Fluid Pressure

Note that most of this section was written with simple fluids like [water](/water.md "water") in mind. Elements such as [mochi](/mochi.md "mochi"), [viscous](/viscous.md "viscous"), and especially [powder](/powder.md "powder") act differently under the conditions described here.

### Hydraulics

The most obvious application of fluid pressure is [hydraulics](/Hydraulic%20Pressure.md "Hydraulic Pressure"), which involves using fluid pressure to perform some action.

### Explosives

As pressure is a force, it can be used destructively. High-pressure fluids, especially when combined with other destructive elements like [Heater](/Heater.md "Heater") or [Outflow](/Outflow%20%28Element%29.md "Outflow (Element)"), are often created when an explosive weapon is detonated.

### Pressure Gradient

A **pressure gradient** is a formation, stable or not, where the pressure or density of a fluid changes with distance. A pressure gradient is most commonly observed in fluid bodies under gravity or explosions.

### Vacuum

A **vacuum** is the absence of any particles. It is the lowest possible pressure.

Below surface pressure but above vacuum, particles do not interact very much. The natural tendency for a fluid to "spread out" no longer applies, and density gradients do not move towards equilibrium.

### Surface Pressure

**Surface pressure** is the closest that particles can be packed together without touching, i.e. the highest density without any pressure.

The pressure at the surface of a body of fluid is slightly above surface pressure. Fluid particles at surface pressure under a slight amount of pressure form a triangular structure.

Surface pressure can be easily achieved by setting *standardDistance* in the [Parameters](/Parameters.md "Parameters") to 0.99999 and drawing with a tool. This places particles essentially at the lowest density possible while still having contact, which is required for pressure.

#### Sub-Surface Pressure

**Sub-surface pressure** refers to a group of pressure levels where the arrangement of fluid particles changes. Some sub-surface pressure levels are past critical pressure. Fluids that exist past critical pressure but still do not exhibit the reaction are referred to as "quasi-critical".

Under slightly more pressure, particles arrange themselves into a grid-like pattern. Under normal gravity, this is only a few particles below the surface.

Under more pressure, particles arrange themselves into an amorphous, glass-like pattern. Critical pressure seems to be around this point. Under normal gravity, this state occurs quite deep below the surface.

Under yet more pressure, the amorphous pattern settles into a hexagonal, honeycomb-like pattern. As pressure approaches breakdown, the structure begins to break down again into an amorphous structure, and will begin shifting constantly.

### Critical Point

The **critical point** or **critical pressure** is the pressure at which a fluid can indefinitely sustain a [sonic boom](/Sonic%20Boom.md "Sonic Boom") reaction. See [supercriticality](/supercriticality.md "supercriticality").

#### Breakdown Pressure

**Breakdown pressure** is the pressure at which a [quasi-critical](/Supercriticality.md "Supercriticality") fluid can no longer exist.

##### Quasi-breakdown pressure

Quasi-breakdown pressure is slightly below breakdown pressure. Under quasi-breakdown pressure, a quasi-critical state can be maintained, but is incredibly unstable. Particles will shake rapidly and will likely break down. This motion is not to be confused with that exhibited at sub-surface pressures below quasi-breakdown, which are usually more stable. They are caused by the same increasing instability and quasi-breakdown can be thought of as the "point of no return".

#### Degeneracy

**Degeneracy** occurs between the critical and hypercritical points. At first, the sustained reaction appears like waves (phonons) traveling through an otherwise normal fluid. As pressure increases, the reaction becomes less localized and spreads throughout the entire body of fluid, which can be seen as a "full of holes" appearance. Between this point and hypercritical pressure, the "holes" become less pronounced and the density becomes more uniform.

### Hypercritical Point

**Hypercritical pressure** is the pressure at which [quantum effects](/Quantum%20Physics.md "Quantum Physics") begin to take place.

## Pressure in rigid or soft bodies

### Penetration

A piercing weapon relies on a very small contact point that results in an extremely high pressure, or a bullet travelling at a high enough speed. In both cases penetration is the result of [Teleportation](/Teleportation.md "Teleportation").

## Static Pressure

[Save-file analysis](/.oec%20File.md ".oec File") has revealed that with default settings, particles in the game do not have an internal "pressure" value that influences their behaviour. By enabling *staticPressureFlag* in the [Parameters](/Parameters.md "Parameters"), an additional calculation is applied to all particles during runtime and saved with each particle in the file. All default particle behaviours arise emergently out of just speed, location, and a fixed particle repulsion coefficient. This is the simplest explanation of the [Sonic Boom](/Sonic%20Boom.md "Sonic Boom") reaction - particles under pressure are not actually pushing back, they are vibrating at increasingly high speeds and the inertia of their impingement on the compressive particles provides the reactive force.

This page is a launch pad, introducing you to things that OE-Cake can do. It is meant to inspire, showing you new ideas to use in your creations.

If you have discovered how to build something new, post it here so that other people can enjoy the creations that can be made from it or the situations it can be put in. 

This page is intended to be a glossary of simple ideas. It will work best if it is filled with smaller things to make that don't really need their own page. If your idea takes more than 2-3 steps to create, it should have its own page that you link to from here.  

For downloads of pre-built creations see the [Creations Compendium](/Creations%20Compendium.md "Creations Compendium") page.

## Propulsion

Propulsion is the art of turning forces into movement.

### **<u>Inflow Powered</u>**

[Inflow](/Inflow.md "Inflow") can be used to push objects to extremely high speeds or generate large forces for lifting.

#### <u>Basic Inflow Rocket</u>

The material RIG (Rigid+Inflow+Gas) is useful for generating a gentle but continuous force, similar to an ion engine in real life. This type of engine does not generate a large amount of force, but is capable of eventually reaching any *maxSpeed* set in the [Parameters](/Parameters.md "Parameters"). RIG rockets provide little to no thrust when not moving, but generate more thrust at higher speeds.

#### <u>Powder Inflow Rocket</u>

The material [RIP](/Powder.md "Powder") for some reason generates more pushing force than the Basic Inflow Rocket. But be careful! If the smoke trail catches fire it will likely blow up the engine.

#### <u>PIE Rocket</u>

The material PIE generates an extremely large torrent of particles. It is great at generating very large forces but has trouble reaching high speed. You must make sure the Elastic is connected to the Rigid on your rocket for it to work well.
![Basic design for a stable Inflow rocket. The fins help direct gas straight behind the rocket, and help stabilize it if it wobbles.](/images/Screen%20Shot%202016-01-28%20at%207.38.28%20PM.png "Basic design for a stable Inflow rocket. The fins help direct gas straight behind the rocket, and help stabilize it if it wobbles.")

#### <u>Composite Rocket</u>

It is possible to make a rocket that works closer to real-life rockets, by using a [Fuel](/Fuel.md "Fuel") source and some Powder as propellant. See the article on [Rockets](/Rocket.md "Rocket") for how to build one.
<img src="/images/Fire%20Trail.png" title="This is a bipropellant Rocket in action. It uses Fuel and Powder to create thrust. |none" width="300" height="300" alt="This is a bipropellant Rocket in action. It uses Fuel and Powder to create thrust. |none" />

### **<u>Jet Powered</u>**

[Jet](/Jet.md "Jet") is the default material for making things move. The force that Jet pushes with can be changed by *jetCoefficient* in the [Parameters](/Parameters.md "Parameters").

#### <u>Jet Rockets</u>

Jet for missiles works perfectly if you can make your device symmetrical. Randomly drawing Jet with the Brush or Pencil tool on the corner of your rocket won't be useful, it has to be centered. The Replace tool can make it easier to create balanced Jet rockets.
<img src="/images/Screen%20Shot%202016-01-30%20at%205.49.09%20PM.png" title="A very basic Jet-powered missile. Notice the symmetrical design and centered Jet, which contribute to the missile&#39;s performance. The lines of force represent where and how hard the Jet is pushing, in this case the force is balanced. " width="220" height="220" alt="A very basic Jet-powered missile. Notice the symmetrical design and centered Jet, which contribute to the missile&#39;s performance. The lines of force represent where and how hard the Jet is pushing, in this case the force is balanced. " />

#### <u>Rotary Jet</u>

Jet and [Axis](/Rigid%20Axis.md "Rigid Axis") can easily be combined to create an object that generates rotational force, such as a wheel on a car or a waving machine. When creating things that move back and forth, the *device being moved* must be able to rotate more or move farther than the *device doing the pushing* or else they just get stuck rather than moving.
<img src="/images/Screen%20Shot%202016-01-30%20at%205.44.50%20PM.png" title="A waving machine" width="220" height="220" alt="A waving machine" />

## Fluid Control

Fluids such as [Gas](/Gas.md "Gas"), [Water](/Water.md "Water"), and [Viscous](/Viscous.md "Viscous"), can be moved from one place to another, generate pressure, and be used in many creations to make things happen.
<img src="/images/Chemical%20Mixer" title="Chemical_Mixer" width="330" height="330" alt="Chemical_Mixer" />

### <u>Pipes</u>

Pipes can be used to move fluids from one location to another. Sometimes the walls of the pipe must be made stronger in order to withstand higher pressure. The easiest way to do this is to go into [Points (View Mode)](/Points%20%28View%20Mode%29.md "Points (View Mode)") (hotkey: 2) and draw another layer on top of the wall of your pipe, without overwriting any particles. The goal is to get them as close as possible without deleting the layer underneath, so that it has twice as much to hold the water back. Pipes made of Jet+Wall can be effective, but Jet+Rigid is less effective because the high water pressure causes the Jet to try and move around.
<img src="/images/Screen%20Shot%202016-01-28%20at%205.48.09%20PM.png" title="A pipe transporting water. Notice the double-lined Wall, which helps it withstand higher pressure. " width="220" height="220" alt="A pipe transporting water. Notice the double-lined Wall, which helps it withstand higher pressure. " />

### <u>Valves</u>

Valves can be used to turn flow on and off or redirect it down a different pipe. Valves can be controlled by the mouse, a lever, or by the keyboard in the form of the [User](/User.md "User")'s element. The best design for a valve stops flow completely, yet can still be opened and closed easily.
<img src="/images/Screen%20Shot%202016-01-28%20at%206.37.27%20PM.png" title="A simple valve made of User with a cavity for it to get out of the way" width="280" height="280" alt="A simple valve made of User with a cavity for it to get out of the way" />

### <u>Nozzles</u>

Nozzles are useful when you want to spray something like water or fire in a tight, controlled jet. Nozzles can be used to give rockets more power and control.
<img src="/images/Screen%20Shot%202016-01-28%20at%206.53.56%20PM.png" title="Nozzle being used to turn pressure into speed" width="220" height="220" alt="Nozzle being used to turn pressure into speed" />

### <u>Hoses</u>

Hoses are flexible tubes that are useful for transporting fluids to a movable object, such as an aimable nozzle. Building a hose is usually easy, but making a hose that is both flexible and strong can be tricky.

The easiest way to make a hose is is to (while paused!) use the [Shape](/Shape.md "Shape") tool to create a block of Elastic that is as long and as wide as you need your hose to be, then delete most of the center from it but leaving walls at least 2 particles thick. You can then use the Replace tool with Rigid to connect each side of the hose to the other, making a series of parallel [links](/Linking%20particles.md "Linking particles") from each Elastic sidewall to the other. Do not overwrite too much elastic because the hose will be to stiff, and do now overwrite too little elastic or the hose will be floppy!

Warning! If at all possible, try to do all work on the hose before you unpause, OR position the hose at the same angle which it was created when modifying it. This is because Elastic has a glitch that causes it to twist strongly if it is worked on while rotated to a different angle than it was created.
<img src="/images/Screen%20Shot%202016-01-29%20at%202.20.26%20PM.png" title="A roughly made hose. Notice the linked parallel sections of Rigid along the sides. " width="220" height="220" alt="A roughly made hose. Notice the linked parallel sections of Rigid along the sides. " />

### <u>Pistons</u>

Pistons are useful ways to use water pressure to push something. A piston consists of a pipe to hold water and a watertight (but not too tight!) block of movable Rigid. The block of movable Rigid can be connected directly to something that needs to be pushed, or hold an axle for extra flexibility.
<img src="/images/Screen%20Shot%202016-07-08%20at%2021.45.15.png" title="A highly advanced creation using several pistons. Pieces that are the same color are &quot;linked&quot; to each other, except the piston heads. " width="220" height="220" alt="A highly advanced creation using several pistons. Pieces that are the same color are &quot;linked&quot; to each other, except the piston heads. " />

## Control Points

Sometimes the mouse alone just isn't enough to operate your creation. Maybe you need something held in place, or to rotate around an axle, or to convert one type of force into another.

### <u>Lever</u>

Think back to Jr. High (scary, i know). Levers are excellent ways to convert one type of movement into another, such as turning a lot of strength into speed, or making a weak force stronger. A type 2 lever can generate extremely large forces for pushing tight valves or crushing objects. Levers gan generate and receive incredible forces so they must be designed to handle them.
<img src="/images/Screen%20Shot%202016-01-29%20at%204.36.17%20PM.png" title="Screen_Shot_2016-01-29_at_4.36.17_PM.png" width="220" height="220" alt="Screen_Shot_2016-01-29_at_4.36.17_PM.png" />
<img src="/images/Screen%20Shot%202016-01-29%20at%204.36.45%20PM.png" title="A type 2 lever being used to open and close a valve. The linked sections are in red" width="220" height="220" alt="A type 2 lever being used to open and close a valve. The linked sections are in red" />

### <u>Axle/Connecting Rod</u>

**Axles** are used to transmit force to or from something that rotates, such as a wheel. **Connecting rods** are two axles linked together so that the source of power and the object being driven can both change their angle, which is important when designing efficient pistons. Pistons are only slightly useful if they can only push straight out, combining a piston with a connecting rod allows the target to move freely. In order to make an axle all you need to do is create a circle of Rigid (usually connected to a larger object, for example the body of a car) and surround it with a shell or casing (usually connected to the device being pushed, for example the wheel) made of more Rigid, then link the circle to the larger object so it stays in place while the rotating object moves around it.
<img src="/images/Two%20Stroke%20Double-Action%20Jet%20Powered%20Buggy" title="A car made in OE-Cake, using many axles" width="330" height="330" alt="A car made in OE-Cake, using many axles" />
<img src="/images/Screen%20Shot%202016-01-30%20at%201.43.09%20AM.png" title="A Jet-powered oscillator. The two black orbs are axles that have been linked creating a Connecting Rod, so that the rotation force of Jet-powered Axis can be turned into a back-and-forth motion on the other device. " width="220" height="220" alt="A Jet-powered oscillator. The two black orbs are axles that have been linked creating a Connecting Rod, so that the rotation force of Jet-powered Axis can be turned into a back-and-forth motion on the other device. " />
<img src="/images/Axle%20interconnections.png" title="This is a picture that shows the connections necessary to create a wheel powered by an external source. A powered wheel works best when connected to the crankshaft with four evenly spaced axlesin a &quot;+&quot; shape. " width="500" height="500" alt="This is a picture that shows the connections necessary to create a wheel powered by an external source. A powered wheel works best when connected to the crankshaft with four evenly spaced axlesin a &quot;+&quot; shape. " />

### <u>Pump</u>

Whenever you need pressurized fluid that can travel with an object, or desire water pressure that does not come from the [Pour (Inflow)](/Pour.md "Pour") option, or more pressure than normal [Inflow](/Inflow.md "Inflow") can provide, there is no replacement for the *centrifugal pump.* Don't let the name intimidate you, they are simple to make and extremely effective. The power of Rigid, Jet, and Inflow combined equals something greater than just the individual pieces. The easiest way to make an efficient and effective pump is to cut a circle out of some Wall with the material [XOR](/Circles%20%28Crafting%29.md "Circles (Crafting)"), then [Replace](/Replace.md "Replace") the beam of XOR with [Rigid Axis](/Rigid%20Axis.md "Rigid Axis"), then Replace a few particles along the edge with Jet to make it spin, and Replace most of the rest of the particles with Rigid Axis Inflow, such as the material RXIQ if you want a Water pump. All materials can be replaced with normal Rigid to create a pump that can be easily moved around, or move itself around.
<img src="/images/Screen%20Shot%202016-02-19%20at%2002.58.29.png" title="Basic design of a self-priming centrifugal pump" width="220" height="220" alt="Basic design of a self-priming centrifugal pump" />
<img src="/images/Screen%20Shot%202016-02-19%20at%2002.58.48.png" title="Pump in action. Inflow Pumps are the only efficient design, pumps fed from a reservoir can never raise the fluid level higher than the input source. |alt=" width="220" height="220" alt="Pump in action. Inflow Pumps are the only efficient design, pumps fed from a reservoir can never raise the fluid level higher than the input source. |alt=" />
<img src="/images/Perfect%20Flamethrower" title="A pump in action, and how to build it" width="330" height="330" alt="A pump in action, and how to build it" />

## Explosives

Explosives generate large forces to cause damage or propel objects.

### **<u>Powder</u>**

Powder is easily the most versatile explosive. Powder has many variables in the [Parameters](/Parameters.md "Parameters") that allow it to be used as everything from a gentle pushing force to a violent impactor. Changing Powder's parameters can radically change it's performance

### **<u>Mochi</u>**

Mochi is a powerful alternative to Powder. Mochi does not generate any heat to melt Elastic or ignite Fuel, but is extremely good at pushing things out of the way.

#### <u>Impact Bomb</u>

The material MI (Mochi + [Inflow](/Inflow.md "Inflow")) is an excellent compact explosive. It does not take up much space or weigh much, and detonates on impact or when moved violently. It is very volatile and must be handled carefully.

Warning! A pure mochibomb *WILL* crash OE-Cake! It becomes so incredibly powerful by Inflow-ing an extremely large quantity of particles. Pure mochibombs (just the material MI) must be used with [Drain](/Drain.md "Drain") mode on or with lots of Outflow nearby! This problem is worse on slower computers.
<img src="/images/Screen%20Shot%202016-01-31%20at%201.58.26%20AM.png" title="Demonstration of the awesome power of a Mochibomb. The test computer died shortly after this image was captured. " width="300" height="300" alt="Demonstration of the awesome power of a Mochibomb. The test computer died shortly after this image was captured. " />

#### <u>Stable Impact Bomb</u>

A pure mochibomb is rather delicate. The material VIM is much more resistant to love taps and rough handling.

#### <u>Two-Staged Impact Bomb</u>

The material MIP (or occasionally MIF) is an excellent explosive that is much less likely clog up your game. A two-staged Mochi explosion must be controlled by having a timer made of [Hot](/Heater.md "Heater") nearby. This limits the explosion to a certain radius, useful for keeping performance in check. It is the most useful explosive in the game because it comes in a small package, creates a large number of particles when detonated, and attacks with pressure, Hot, and shrapnel.
<img src="/images/Screen%20Shot%202016-01-31%20at%202.14.53%20AM.png" title="The basic design for a controlled explosive. The red material is actually RH and is linked to the explosive casing, so that the bomb (and it&#39;s timer) can be safely moved around. " width="220" height="220" alt="The basic design for a controlled explosive. The red material is actually RH and is linked to the explosive casing, so that the bomb (and it&#39;s timer) can be safely moved around. " />
<img src="/images/Screen%20Shot%202016-01-31%20at%202.15.35%20AM.png" title="Two-Staged Explosive during the first stage of explosion" width="220" height="220" alt="Two-Staged Explosive during the first stage of explosion" />
<img src="/images/Screen%20Shot%202016-01-31%20at%202.16.06%20AM.png" title="Two-Staged Explosive during the second stage of the explosion" width="220" height="220" alt="Two-Staged Explosive during the second stage of the explosion" />

### **<u>Elastic</u>**

#### <u>EFI</u>

The material Elastic + Fuel + Inflow can create a very stable and yet extremely powerful explosive. A shape made out of EFI must be surrounded by a non-Inflow material to stop it from Inflow-ing particles all over the place. The EFI material can be be hit extremely hard without detonating or Inflow-ing any particles, making it ideal for powerful and stable explosives that are set off by a specific trigger. The EFI material works best when triggered by a smaller explosive made out of Powder to cause a more powerful chain reaction.

#### <u>Brittle</u>

Surprisingly, Brittle is useful for a special type of explosive. The material PEB is a delicate material that is set off by gentle contact. It does not explode hard but it explodes hard enough to mess up the completion of a level, such as by a piece landing on some nearby Hot and causing a further chain reaction that destroys your character.
<img src="/images/Screen%20Shot%202016-01-31%20at%201.59.49%20AM.png" title="Material PEB exploding in it&#39;s unique way" width="220" height="220" alt="Material PEB exploding in it&#39;s unique way" />

### **<u>Jet</u>**

Jet is a useful additive to explosives. It helps generate a much larger pushing force, can blast through shields and barriers, and produces a much more firey explosion in [Blob](/Blob%20%28View%20Mode%29.md "Blob (View Mode)") mode. Liquid Jet combined with Mochi (the [Mochi-Jet reaction](/Mochi-Jet%20reaction.md "Mochi-Jet reaction")) produces a special type of explosion, but creating a useful bomb using this reaction is difficult.
<img src="/images/Screen%20Shot%202016-01-31%20at%202.34.11%20AM.png" title="The Mochi-Jet reaction" width="220" height="220" alt="The Mochi-Jet reaction" />

### **<u>standardDistance</u>**

After changing the *standardDistance* variable in the [Parameters](/Parameters.md "Parameters") to a lower value, the [Shape](/Shape.md "Shape") tool will automatically draw explosions with any fluid (such as Powder, Water, or even Brittle). Lower *standardDistance* values will produce more powerful explosions.

Warning! Setting the *standardDistance* variable too low (probably around 0.3 depending on your computer) may result in extreme lag! If set extremely low you run the risk of drawing more particles than can fit on your screen, and we all know how slow OE-Cake can get even when half full!

### <u>**Compressed Particles**</u>

[Compressed particles](/Compressed%20particle.md "Compressed particle") make excellent explosives, having a very high energy density in a very small package, as well as having the ability to be fired and be configured for contact or kinetic triggering. A compressed particle made of Powder + Inflow is an extremely potent conventional explosive. Though I haven't tried it, it is likely a Compressed Particle made of Mochi+Inflow would be the most compact way to produce a Mochibomb. It is also theorized that compressed particles exhibit [entanglement](/entanglement.md "entanglement") and may be a catalyst for creating [Nova Viscous](/Viscous.md "Viscous").

## Projectile Launcher

A projectile can be used to cause damage or travel long distances. Reaching these high speeds can be difficult, especially for delicate creations such as explosives.

If you want to make things go even faster, you can change the *maxSpeed* [Parameter](/Parameters.md "Parameters") to a larger number:

-   maxSpeed=0.5 default, pretty normal
-   maxSpeed=5 wicked fast

There are several different ways to fire things in OE-Cake:

### **<u>Explosive Powered</u>**

Guns are creations designed fire small projectiles around the sandbox. Useful and powerful guns are difficult to make in OE-Cake. Guns usually use an explosion to fire a solid projectile at high speed. Most guns typically use [Powder](/Powder.md "Powder") to generate the pressure required to fire something.

#### <u>Basic Cannon</u>

Make a circular belly of Wall connected to a pouch that holds a projectile. Put a small piece of rigid in the pouch. Fill the rest with Powder. Ignite and enjoy! This type of cannon works best when the pressure from the explosion can be completely contained, except for an opening where the explosion is used to fire something.　Cannons are not good at firing bombs because they often blow up in the barrel. <img src="/images/Screen%20Shot%202015-12-09%20at%2004.16.53.png" title="A small but effective Cannon. Fill with Powder+Inflow for greater effect.|link=http://oecake.wikia.com/wiki/File:Screen_Shot_2015-12-09_at_04.16.53.png|none" width="220" height="220" alt="A small but effective Cannon. Fill with Powder+Inflow for greater effect.|link=http://oecake.wikia.com/wiki/File:Screen_Shot_2015-12-09_at_04.16.53.png|none" />

#### <u>Efficient Cannon</u>

Barrels and other normal gun-like things are very difficult to make properly in OE-Cake. The normal real-life style of cannon does not work very well because Powder is not good at pushing. A cannon that makes better use of the default settings would look very different. The example below uses [RXG](/Rigid%20Axis.md "Rigid Axis") for the body, MIPG for the propellant, and Rigid+Gas for the projectile.<img src="/images/Screen%20Shot%202015-12-09%20at%2004.26.25.png" title="What a more efficient cannon could look like|link=http://oecake.wikia.com/wiki/File:Screen_Shot_2015-12-09_at_04.26.25.png|none" width="275" height="275" alt="What a more efficient cannon could look like|link=http://oecake.wikia.com/wiki/File:Screen_Shot_2015-12-09_at_04.26.25.png|none" />

### **<u>Elastic Powered</u>**

[Elastic](/Elastic.md "Elastic") is an efficient way to contain power that you want to release in a controlled manner. Elastic can also gently accelerate delicate packages to high speed, and be reused multiple times.

#### <u>Slingshot</u>

It is possible to build a machine in OE-Cake that can stretch a band of Elastic, storing energy to fire a projectile. See the [Hydraulic Slingshot](/Hydraulic%20Slingshot.md "Hydraulic Slingshot") article for more details.
<img src="/images/Screen%20Shot%202015-12-09%20at%2004.36.12.png" title="A hydraulically powered slingshot firing a large projectile|link=http://oecake.wikia.com/wiki/File:Screen_Shot_2015-12-09_at_04.36.12.png|none" width="288" height="288" alt="A hydraulically powered slingshot firing a large projectile|link=http://oecake.wikia.com/wiki/File:Screen_Shot_2015-12-09_at_04.36.12.png|none" />

### **<u>Fluid Powered</u>**

The pressure of [Water](/Water.md "Water") or [Gas](/Gas.md "Gas") can be used to gently accelerate objects to high speed. This type of weapon is useful because it is relatively non-destructive (to nearby objects), simple to design, and can be easily reloaded and reused. A disadvantage is that they are "dirty" because of all of the exhaust material left over.

#### <u>Blowgun/Pneumatic gun</u>

A blowgun consists of a projectile that fits loosely in a barrel, a chamber to hold the air, and a device to push on the air hard enough to fire the projectile out of the barrel. The projectile should be centered in the barrel, and usually works better when it has a small platform to sit on to hold it in place.
<img src="/images/Screen%20Shot%202016-02-29%20at%2022.06.34.png" title="Basic design for a blowgun. Gravity pulled a block of Jet onto the Gas, which forced it and the projectile out of the barrel. " width="220" height="220" alt="Basic design for a blowgun. Gravity pulled a block of Jet onto the Gas, which forced it and the projectile out of the barrel. " />

#### <u>Shockwave Cannon</u>

This is close to the design of a cannon in real life. A loose projectile is placed in a barrel, behind that is a belly that holds Gas. A small amount of [Powder](/Powder.md "Powder") is placed at the back of the chamber away from the projectile. When the powder is lit, the explosion generates a shockwave in the Gas that fires the projectile out of the barrel. When designing the barrel and projectile, the projectile should be able to move freely in the barrel but not be so loose that lots of air escapes around it. This cannon is useful because it separates the dangerous Powder explosion from the projectile, allowing bombs to be fired from an explosive-based weapon.
<img src="/images/Screen%20Shot%202016-01-31%20at%203.17.39%20PM.png" title="Screen_Shot_2016-01-31_at_3.17.39_PM.png" width="600" height="600" alt="Screen_Shot_2016-01-31_at_3.17.39_PM.png" />
<img src="/images/Screen%20Shot%202016-01-31%20at%203.17.49%20PM.png" title="Screen_Shot_2016-01-31_at_3.17.49_PM.png" width="600" height="600" alt="Screen_Shot_2016-01-31_at_3.17.49_PM.png" />
<img src="/images/Screen%20Shot%202016-01-31%20at%203.18.02%20PM.png" title="An example shockwave cannon. A small amount of Mochi is used to hold the projectile in place and prevent Gas from escaping. Powder + Inflow is used as the explosive." width="600" height="600" alt="An example shockwave cannon. A small amount of Mochi is used to hold the projectile in place and prevent Gas from escaping. Powder + Inflow is used as the explosive." />

### **<u>Jet Powered</u>**

Jet can be used to quickly accelerate objects to high speed. This type of weapon is useful because it is relatively non-destructive (to nearby objects), simple to design, and can be easily reloaded and reused. And they don't create exhaust.

#### <u>Bolt Action Gun</u>

Make a rectangle out of RP. Use the replace tool to create a bullet shaped piece of fuel inside the cartridge with a piece of jet at the base of the bullet.

<img src="/images/Bullet.png" title="Bullet.png" width="201" height="201" alt="Bullet.png" />

Then you need to create a gun to fire the bullet. Create a large T shaped piece of rigid held in place with wall on the left and right with a little room to slide around. To the right of the rigid create a chamber that the bullet fits into, then make a barrel that the fuel part of the bullet fits into. Create a small hole on the bottom of the chamber and a trigger made out of Rigid-Axis tipped with RH. Above the right of the T shaped rigid make a magazine to hold the bullets.
<img src="/images/BoltGun.png" title="BoltGun.png" width="289" height="289" alt="BoltGun.png" />

Pull the bolt back to let a bullet fall into the gun, then push the bolt to the right. Pull the trigger and the gun will fire.

### <u>**Glitch Guns**</u>

Various glitches or "unique physics" in the game can be used to create weapons.

#### <u>Compressed Particle Gun</u>

See the page [Compressed Particle Gun](/Compressed%20Particle%20Gun.md "Compressed Particle Gun") for details regarding a weapon made from [Compressed Particles](/Compressed%20particle.md "Compressed particle").

## Projectiles

Projectiles are objects designed to cause damage. The many materials can all be used to produce different types of projectiles.

### **<u>Solid</u>**

Solid projectiles rely on their weight and speed to cause damage. Solid projectiles are easy to use and can withstand being handled roughly and the extreme forces of being fired.

#### <u>Arrow</u>

An arrow is a narrow, pointy, aerodynamic projectile. They are very good at slicing through the air (or a target) and delivering a large amount of damage to a small area. Arrows actually work best in an atmosphere (surrounded by Gas) because it helps it always point the correct direction.
<img src="/images/Screen%20Shot%202016-01-31%20at%203.58.32%20PM.png" title="Arrow with bumps on the back that act as stabilizing fins, tipped with the armour-piercing material RJH" width="220" height="220" alt="Arrow with bumps on the back that act as stabilizing fins, tipped with the armour-piercing material RJH" />

#### <u>Cannonball</u>

The simplest, age-old projectile. A cannon ball can be used against different targets when made of different materials: the basic Rigid ball is rather light and not powerful, but this makes it easy to handle. Rigid + [Hot](/Heater.md "Heater") makes it effective against String, Elastic, Fuel, and Powder-based targets. Rigid + [Viscous](/Viscous.md "Viscous") can made Rigid more effective. [Jet](/Jet.md "Jet") provides an extremely powerful impact but can be hard to fire. High-density Rigid cannonballs (made by changing the *standardDistance* [Parameter](/Parameters.md "Parameters")) can be much more effective.
<img src="/images/Screen%20Shot%202016-01-31%20at%204.04.29%20PM.png" title="Normal ol&#39; cannonball. And a cannonquadrilateral. " width="220" height="220" alt="Normal ol&#39; cannonball. And a cannonquadrilateral. " />

#### <u>Bullet</u>

Basically, a bullet is an aerodynamic cannonball. They fly better in the air and can actually provide more damage than a cannon ball because they are pointy.
<img src="/images/Screen%20Shot%202016-01-31%20at%204.11.22%20PM.png" title="Different bullet designs, with varying degrees of stability." width="220" height="220" alt="Different bullet designs, with varying degrees of stability." />

<u>Pellets</u>

Firing many small projectiles, or liquid Hot, can be more useful than a single large one. Holding the liquid/pouch of projectiles together long enough to fire it, but still allowing it to separate in-flight, is difficult.

### **<u>Composite</u>**

Composite bombs are formed of multiple, usually custom, [materials](/Material.md "Material") arranged in patterns that give them useful behavior.

#### <u>Basic Bomb</u>

A simple but effective bomb that is stable but detonates on impact is surprisingly easy to make. The [Shape](/Shape.md "Shape") tool can easily make square shaped bombs and the Brush tool can easily make circular projectiles if you change the [Parameter](/Parameters.md "Parameters") *brushWidth.*The bomb's casing should be made of Rigid + Powder so that it does not stick around after exploding.
<img src="/images/Screen%20Shot%202016-01-31%20at%203.35.47%20PM.png" title="Basic circular bomb suitable for being fired from a cannon. The small block to the side is Rigid + Hot and is linked to the bomb&#39;s casing. " width="245" height="245" alt="Basic circular bomb suitable for being fired from a cannon. The small block to the side is Rigid + Hot and is linked to the bomb&#39;s casing. " />

#### <u>Fusion Bomb</u>

A Fusion Bomb is an advanced type of composite bomb. See the [full article](/Fusion%20Bomb.md "Fusion Bomb") for details.

<img src="/images/Screen%20Shot%202016-03-08%20at%2020.50.34.png" title="Fusion bomb shortly after detonation" width="220" height="220" alt="Fusion bomb shortly after detonation" />

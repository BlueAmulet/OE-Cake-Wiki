A **rocket** is a form of propulsion that works by pushing particles very fast away from a source, usually with the help of an explosion.

Any [Inflow](/Inflow.md "Inflow") of particles, such as [Gas](/Gas.md "Gas") + Inflow or [Water](/Water.md "Water") + Inflow, will push the opposite direction as the flow. If you surround the Inflow with [Rigid](/Rigid.md "Rigid") and only let the flow go out of a small hole, the shape will begin to move the other direction. The higher the pressure the faster it will move. This is how all of the \[<http://oecake.wikia.com/wiki/How_to_Build_a>...#Basic_Inflow_Rocket Basic Rockets\] work. Basic rockets will be good enough for most jobs, and you should try to use one first. However sometimes you may need more out of a Rocket, such as higher thrust, a cool fire trail as seen below, more realistic physics and simulation, or you just like building complicated things in OE-Cake like me.
<img src="/images/Rocket%20Diagram.png" title="fig:Clear diagram of the basic design for a bipropellant Rocket. Notice the Inflow Pumps, which generate Fuel + Gas, and the piece of PIE at the top which generates Powder. The combustion chamber in the middle is critical for this type of Rocket to work. " width="220" height="220" alt="Clear diagram of the basic design for a bipropellant Rocket. Notice the Inflow Pumps, which generate Fuel + Gas, and the piece of PIE at the top which generates Powder. The combustion chamber in the middle is critical for this type of Rocket to work. " />
<img src="/images/Fire%20Trail.png" title="fig:This is the bipropellant Rocket in action. It is firing in an atmosphere of pure Gas (not L+G). " width="300" height="300" alt="This is the bipropellant Rocket in action. It is firing in an atmosphere of pure Gas (not L+G). " />

## How to Build a Rocket

First you should be familiar with building \[<http://oecake.wikia.com/wiki/How_to_Build_a>...#Pump Pumps\], because they are the Gas+Fuel source for advanced Rockets. You also need to know how to change the [Parameters](/Parameters.md "Parameters").

The body of the Rocket is made of Rigid drawn with the Parameter `standardDistance` set to 0.5, you can draw it by hand with the Pencil tool. You need to double-layer it (draw closely beside the first line to make another layer) to handle the high pressure of the explosion and pumps better.

The blue material is Rigid+Cold+Water (RCQ), the Water helps put out accidental ignition of the pumps (but by that point it's too late) and the Cold makes sure the Rigid+Water doesn't evaporate into Rigid+Water+Light+Gas. Making the pump chambers RCQ isn't useful because you can't fix the engine blowing up. However the important place to have RCQ is right at the tips of the entrance to the combustion chamber, which makes it much harder for fire to spread backwards into the pump, especially for when the rocket gets bumped.

You need a combustion chamber for this to work properly. A combustion chamber works by having an exit very slightly smaller than the entrance, which causes the flow to slow down a little bit. This makes some of the Fuel+Gas flow backwards around the curved part to the beginning of the chamber. If this Fuel+Gas is "on fire" with [Hot](/heater.md "heater"), it will set more Fuel on fire and keep the reaction going, making all Fuel exiting the chamber be on fire without causing the Hot to travel backwards into the pumps.

The fan blades were drawn at `standardDistance=0.5` because they produce more Inflow pressure, using the Shape tool for perfect rectangular blades. Note that there are small pieces of Jet at the tips of the fan blades, and they are positioned so that the Jet makes the two spin opposite directions. It doesn't really matter what direction they spin so long as they spin the opposite. The Jet was added with the Replace tool, and `lineWidth=0.5` which makes the Replace tool precise enough to Replace individual particles. The reason why the Jet is surrounded by Rigid is so that the Jet force is perfectly aligned, and because Jet will mess up if it is in contact with the other particles, <em>and</em> because it makes Inflow much more powerful which messes things up.

The Replace tool was used to put the Inflow on the already-drawn blades. The Inflow material is FRIG (yeah, really). FRIGL if you want the resulting fire to "burn upwards" like the fire in the image over there. The awkward blob in the top-middle is the material PIE, which causes a huge Inflow of Powder. There is actually too much PIE there, you only need a 2-tall by 3-wide piece of PIE, when drawing make sure the PIE is placed very close to the Rigid (but make sure it doesn't overwrite!) so that it sticks.

Now you will need to do the hard part, which is tuning the Parameters. The variables `fuelLightProbability`, `fuelExtinguishProbability`, `powderLightProbability`, `powderExtinguishProbability`, and the all-important `powderExplosionCoefficient`, will need to be changed in order to make the ignition and explosion work properly. I can't tell you the exact values to use because every rocket will be slightly different, but all of the values will be much lower than their default settings. I will provide mine so that you know approximately where to start, and have a working fuel/powder mixture to try out.

The Rocket in the images above works on approximately two parts Fuel+Gas to one part Powder, it is important to use that ratio with these values.

`fuelLightProbability=0.01`

`fuelExtinguishProbability=0.001`

`powderLightProbability=0.02`

`powderExtinguishProbability=0.0025`

`powderExplosionCoefficient=0.2`
<img src="/images/Working%20Powder%2BFuel%20Rocket" title="fig:For some reason this video only works if you click the little &quot;i&quot; at the bottom of the screen to see the video on it&#39;s own page!" width="330" height="330" alt="For some reason this video only works if you click the little &quot;i&quot; at the bottom of the screen to see the video on it&#39;s own page!" />

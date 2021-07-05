 In order to change these settings:

1\. Save a file somewhere.

2\. Open this file with a text editor.

3\. Scroll to the bottom to find the list of parameters.

4\. Change variables.

5\. Save and make sure the extension is .oec  

## Parameters

Notably absent from the Parameters are any settings for [Rice](/Rice.md "Rice"), [Rigid](/Rigid.md "Rigid"), [Wall](/Wall.md "Wall"), or [Water](/Water.md "Water"), leading me to believe they have specially programmed physics that are different from the other materials.

-   <span>\`time\`</span>
    -   The current runtime, seems to be in tens of seconds.
    -   Can't really think why this would need to be changed.
    -   This setting is less suitable for timing things, because it always records your subjective time. This means it records the number of seconds that pass in real-time, not the number of seconds that pass in the game. The speed of time in the game can be changed with the parameter below, making this timer unreliable
-   \`timeSteps\`
    -   Number of iterations the program has computed.
    -   This is a counter of how many moves the program has made since you first hit File>New
    -   It essentially counts how long the game has been unpaused and running
    -   You can use this as a timer, for example:
    -   If you manually set it to 0, you can use it to calculate velocity by starting paused, then quickly unpausing and pausing again, then measuring how far something moved
-   \`scale\`
    -   The overall size of the [canvas](/canvas.md "canvas"), the grey area where you are drawing
    -   Setting a lower number results in a larger canvas, making everything look smaller
    -   higher results in a smaller canvas, but everything looks bigger
    -   This is because *scale* represents the particle radius in pixels, how wide each dot is
    -   Canvas size follows the inverse square rule:
        -   with the default being scale=8,
        -   scale=4 has 4x the volume of scale=8
        -   scale=2 has 16x volume,
        -   scale=16 has a quarter of the volume of scale=8

<!-- -->

-   \`timeStepsPerFrame\`  
    -   Global speed multiplier
    -   The number of physics iterations per frame the game tries to process
    -   Setting smaller numbers gives better performance (more FPS) but gives a "slow-mo" effect
    -   Setting higher results in a "fast-forward" effect, if your computer can handle it
    -   Generally, higher numbers lower your FPS especially on big creations
    -   Fast-motion may be useful for small, fast paced games,
    -   or for studying small numbers of particles over a long time, because time passes faster
    -   *timeStepsPerFrame* is also used to calculate the length of the particle trails in [Circle (Blur)](/Circles%20%28View%20Mode%29.md "Circles (View Mode)") viewing mode
    -   Useful when combined with FRAPS to do slow-mo or fast-mo (apparently FRAPS got rid of that function)

<!-- -->

-   \`framesPerSecond\`  
    -   Sadly, cannot be changed.  At least we know the framerate though.

<!-- -->

-   \`pauseFlag\`  
    -   Represents whether the game is paused or not.
    -   Manually modifying this variable can be useful for games that you want to start automatically
    -   For example a puzzle game, you design it while paused then manually modify the save to "unpaused" so it starts playing as soon as it's opened
    -   *pauseFlag* is also useful in diagnosing save file corruption, a corrupted game cannot start paused because the Parameters are at the bottom of the file and will fail to be read, thus it takes the default of starting unpaused

<!-- -->

-   \`randSeed\`  
    -   The root of all that is random.

<!-- -->

-   \`gravityFlag\`  
    -   Whether or not [Gravity](/Gravity.md "Gravity") is enabled.

<!-- -->

-   \`gravityAcceleration\`  
    -   The base strength behind the force of gravity acting on objects.
    -   Setting higher results in a more aggressive gravitational attraction, but doesn't make things fall faster.
    -   Should probably just be left alone.

<!-- -->

-   \`gravityAmplification\`  
    -   The multiplier that determines gravity behaviour.
    -   Higher numbers make things fall faster, on sharper parabolic curve.
    -   For the physicists out there: if I'm not mistaken, I believe this is similar to being able to chose both sides of a constant - *gravityAccel* could represent the number of distance units that were covered, and *gravityAmp* could represent the units of time that were passed. Usually time is just left to "1", but we have control over both in this program

<!-- -->

-   \`gravityAngle\`  
    -   Angle in radians that everything based on gravity tries to follow.
    -   Changing this value rotates the "down" direction around the middle of the screen
    -   0 degrees = 0 radians (normal)
    -   90 d = 1.5707963268 r (right side)
    -   180 d = 3.1415926536 r (upsidedown)
    -   270 d = 4.7123889804 r (left side)

<!-- -->

-   \`boundsFlag\`
    -   [Outflow mode](/Drain.md "Drain"), makes stuff be eaten when it falls off the edges of the screen  

<!-- -->

-   \`boundsThickness\`  
    -   How far off-screen the edge collision happens  
    -   Setting to a positive number pushes particles inwards, away from the edges  
    -   Setting to a negative number lets particles fall off the side a bit, could be useful for hiding things just off the side, but why?  
    -   It is possible this setting was never intended to be used, or has a hidden function  
    -   Also seems to mess with fluid's physics  

<!-- -->

-   \`boundsLeft\`, \`boundsRight\`, \`boundsBottom\`, \`boundsTop\`
    -   How large of an area the particles can move around in  
    -   This allows a canvas that is larger or smaller than the size of your window, if combined with the *scrollFlag* Parameter (ctrl+f to find)  

<!-- -->

-   \`boundsRadius\`  
    -   Size of the canvas's curved corners  
    -   Larger numbers make rounder corners  
    -   negative numbers create exceptionally strange physics  

<!-- -->

-   \`standardDistance\`  
    -   Density at which all particles are drawn by their tools  
    -   If each particle is 1 unit across, the default *standardDistance* is 0.75 which means the particles are slightly touching when they are drawn. This is so that Rigid and Wall are dense enough to seem solid. This number is pretty large by default to keep the number of particles lower, which helps performance
        -   Setting to 0.5 creates Rigid and Wall that is very strong, closer to metal  
        -   Setting a value of 0.1 means that you are drawing 10 particles in the space of 1, as you can imagine this is quite a lot! This will cause fluids to immediately explode, and large amounts of anything will crash your game  
        -   A value of 0.25 is fun to play with, everything explodes immediately, Rigid becomes extremely heavy. Play with Outflow mode for extra safety  
    -   The default setting is also pretty close to the settling density of all of the fluids, ie. Viscous, Powder, Water, and the others. This means that when you use the Bucket tool to fill an area, the fluid doesn't splash much and settles quickly. The settling density of Water is actually a little bit closer to 0.7  
    -   Strongly affects how [Inflow](/Inflow.md "Inflow") and [Powder](/Powder.md "Powder") handle
        -   Inflow is doubly affected: the denser the original block of Inflow is drawn, the more powerful it will try to Inflow. Also, *standardDistance* values change how powerful the flow of Inflow is. Use this double sensitivity to make Inflow that works as you need it to at any *standardDistance* value  
        -   The settling density of Powder is directly determined by *standardDistance*. It seems as if the particle size is determined by the parameter, because Powder with low *standardDistance*values will easily flow through cracks. Setting to an extreme value will cause Powder to have very strange physics. For example it is through this reaction that the [Powder-Snow Reaction](/Powder-Snow%20Reaction.md) occurs.  
        -   Changing the *standardDistance* of Powder strongly changes it's physical properties, giving another degree of freedom with which to modify Powder's behavior  

<!-- -->

-   \`standardDensity\`  
    -   Affects particle size for particle-to-particle collision  
    -   probably also the game's base resolution for physics calculations  
    -   Can severely mess up material physics so use wisely  
    -   Smaller numbers produce fluids that are more dense, giving them more detail and realism  
    -   more detailed fluids cost more performance  
    -   Strongly damages Tensile physics  

<!-- -->

-   \`maxSpeed\`  
    -   Essentially the particle speed limit.  
    -   I don't know what is fast or slow, but surpassing \`maxSpeed=5\` for anything more than individual particles is relatively difficult, it takes an absolutely incredible amount of power for something large to reach that speed without Jet  
    -   This is almost like being able to control the speed of light, this is the fastest possible speed in which it is possible for one thing to cause something to happen at a different location  
    -   Rigid actually violates this speed of light, because there is no "propagation" of the force pushing on Rigid, all parts of the Rigid move instantly together, meaning it is possible to use a line of Rigid to poke something faster than it would be possible to physically move something to that location, in a way Rigid is a relativistic material that can reach through time to poke something in the future... trippy mang...  

<!-- -->

-   \`pressureCoefficient\`  
    -   Magnitude of the force at which particles repel each other.  
    -   Setting to 0 essentially disables particle collision.  
    -   Low values can decrease the game's overpressure reaction, and increase settling density while also slightly changing the physics  
    -   has an effect on the "stiffness" of Rigid and Wall, their ability to resist water squeaking through and being squeezed into another piece of Rigid under enough force  

<!-- -->

-   \`repulsionCoefficient\`
    -   The only time I've seen this variable in action is when normal density fluid particles (ie. water) are pressed up against extremely dense (\`standardDistance>0.2\`) sections of Wall. Normally there is a slight glitch where the particles fire away at high speed, which looks like gentle boiling against the surface in question.  
    -   Setting to 0 seems to have few adverse effects, and allows you to use excessively dense materials with less of an issue  
    -   Also causes shockwaves through water to be much more visible in [Points](/Points%20%28View%20Mode%29.md "Points (View Mode)") and [Crosses](/Crosses%20%28View%20Mode%29.md "Crosses (View Mode)") view modes  
    -   I believe this value is an "emergency backup" force that pushes particles apart if they are squeezed into the same location, because lowering it reduces the chances of fluids blowing up under pressure, and increasing it can cause fluids to explode under the slightest touch and never return to equilibrium  

<!-- -->

-   \`dampingFlag\`
    -   Enables a special particle behaviour that tends towards less energetic collisions
    -   This helps keep all the fluids in the game more tame, setting to 0 causes explosions to get really out of hand, and everything is jittery
    -   Setting to 0 will result in a large performance increase especially at high particle counts, but may result in spastic high-speed collision physics especially with water/gas  

<!-- -->

-   \`dampingCoefficient\`
    -   The percentage of energy lost per collision  
    -   Or, how much less a particle will bounce each time  
    -   *dampingCoefficient* also has an effect on the maximum amplitude of shockwaves  

<!-- -->

-   \`staticPressureFlag\`
    -   One of my favorite hidden settings.  
    -   Enables a special particle mode that calculates more accurate pressure.  
    -   Can be used to create sound waves, cavitation, and more accurate water density physics.  
    -   Slightly decreases performance  
    -   These settings require a lot of tweaking to get right. Only change them by small amounts at a time, and look for the little details that change  

<!-- -->

-   \`staticPressureCoefficient\`
    -   The force that static pressure pushes back with  
    -   Higher values try to "fill in" gaps in the fluid more, like the cavitation behind a fast object  
    -   Lower values "push back" less  
    -   Also controls the "speed of sound" in the fluid, higher numbers make shockwaves propagate faster  
    -   This setting can be used to replace the normal particle physics programmed using *pressureCoefficient.*I believe *pressureCoefficient*causes the particles to behave like little marbles, bouncing together to look like water, each having a circular shape. With *pressureCoefficient*set to 0, this value replaces the force that pushes particles apart from each other, by looking at the particles as a volume instead of individual points. It seems to be much smoother, as if they are part of a fluid.  
-   \`staticPressureIteration\`
    -   How many particles are used to determine pressure  
    -   This has a very large impact on both performance and realism  
    -   Setting to 1 or 2 will produce fairly realistic flow without too large of a performance hit  
    -   Setting to a higher number will produce much more realistic pressure but will significantly reduce performance  
    -   Good for long-recording physics sims that you speed up later  

<!-- -->

-   \`staticMaxPressure\`
    -   Determines the maximum reasonable shockwave you want to handle  
    -   Pretty much how "sharp" the shockwave can look  
    -   Setting this number very low (less than 0.001) can help control very aggressive explosions and overpressure situations  
    -   Setting this number higher (5-10 or more) allows a wider dynamic range of pressures, if the parts of your sim can handle it  

<!-- -->

-   \`springCoefficient\`
    -   Determines String's bounciness  
    -   The attractiveness between two string particles seems to follow an exponential curve. String is pretty sloppy at first, but very hard to pull far apart. See the section on Elastic for another similar material  

<!-- -->

-   \`springIteration\`
    -   The length of the String fiber, or how many particles get in on the String calculations  
    -   Too low makes String sloppy, too high makes it stiff(er)  
    -   has a direct impact on the performance cost of String, higher numbers are more expensive  

<!-- -->

-   \`elasticCoefficient\`
    -   The strength with which Elastic attempts to return to it's original shape  
    -   The stretchiness between two Elastic particles seems to follow a linear scale. Elastic has a high internal stiffness, and while stretching it smoothly gets harder and harder to pull apart  
    -   Set to 0.9 to produce a strange, [glass-like substance](/Glass%20Elastic.md "Glass Elastic") (view in Crosses)  
    -   Set to 1 to cause Elastic to... uh, explode  
    -   Set to 3 to easily create [Spin-Charged Elastic](/Spin-Charged%20Elastic.md)  

<!-- -->

-   \`elasticIteration\`
    -   The number of particles that get involved in the Elastic calculation, for example if you set it to 5, one particle will be able to pull on particles up to 5 away  
    -   Low numbers make elastic very sloppy like jello, high numbers make it stiffer like rubber  
    -   has a direct impact on the performance cost of Elastic, higher numbers are more expensive  

<!-- -->

-   \`mochiElasticityCoefficient\`
    -   How clingy Mochi is.  
    -   Doesn't seem to be able to be set above 0.1  

<!-- -->

-   \`mochiSpringCoefficient\`
    -   Mochi's internal tension, it's tendency to form globs.  

<!-- -->

-   \`mochiIteration\`
    -   How far away one individual particle will spread its coefficients.  

<!-- -->

-   \`viscosityCoefficient\`
    -   How viscous Viscous is.  
    -   Positive numbers make Viscous resist flow  
    -   Negative numbers make Viscous want to flow, it is quite strange  
    -   Negative numbers can be used to create non-linear phenomena, for example anti-Viscous plus Powder makes sand that can flow on it's own and likes to move  

<!-- -->

-   \`viscosityIteration\`
    -   How many... oh you get it.  

<!-- -->

-   \`surfaceTensionCoefficient\`
    -   The force stopping the particles from leaving the blob.  
    -   Seems related to surface tension in drops.  
    -   Too low produces small drops that have trouble coalescing into larger drops  
    -   Too high creates a surface that squeezes so hard particles get shot out  
    -   Specifically affects just the surface  

<!-- -->

-   \`surfacePressureCoefficient\`
    -   Extra force holding the particles together in a shape, for when just surface tension isn't enough.  
    -   Higher values produce rigid circles and make coalescing difficult, lower values make it watery  
    -   Affects the pressure inside the droplet  
    -   These two settings are very hard to tune, and need to be retuned for each situation where the limited default tensile effect is not sufficient.  
    -   There is an easily noticeable bug with the default settings: disable gravity (or use the material GT) and create a decently large blob. Above a certain size \`surfacePressureCoefficient\` overcomes the *pressureCoefficient* and the blob starts to explode internally, expelling particles one at a time until it goes under the critical mass 

<!-- -->

-   \`surfaceTensionIteration\`
    -   Controls a length from one of two things, or maybe both: the arc representing the surface of the blob, and/or the radial representing the depth of the blob  
    -   This seems to represent how large of a blob the game thinks is good enough  

<!-- -->

-   \`powderSpringCoefficient\`
    -   How bouncy Powder is, how hard each particle pushes away from one another  
    -   Can slightly affect powder density  
    -   Seems to act a bit like the "coarseness" of the material, lower numbers producing a fine powder and higher numbers making something more like sand or pebbles  

<!-- -->

-   \`powderDampingCoefficient\`
    -   Powder's tendency to "settle" and form a lattice  
    -   higher values make something like icing sugar, settling fast  
    -   lower values makes something more like salt, which tumbles  
    -   negative values cause Powder to dislike settling, making it tumble more. However it makes it respond poorly to impacts  

<!-- -->

-   \`powderFrictionCoefficient\`
    -   'nuff said. How much Powder resists flow.  
    -   These three parameters plus *standardDistance* make [Powder](/Powder.md "Powder") the most complicated material  
    -   By delicately tweaking these variables you can create an extremely wide variety of materials with very specific properties  
    -   These variables allow Powder be anything from a liquid to a semi-solid  
    -   Increasing teh value makes powder that is more sandy, making something akin to dirt  
    -   decreasing the value makes powder that is more watery, making something that flows  
    -   negative values make Powder that dislikes being still, occasionally causing it to create rivers in itself and vastly increasing it's ability to tumble and flow. Can lead to some very strange non-linear behavior.  

<!-- -->

-   \`powderLightProbability\`
    -   The chance that a non-lit Powder particle will ignite when contacting a Hot particle  
    -   Setting to 1 causes an entire mass of Powder to ignite instantly  
    -   Low numbers make Powder harder to ignite, useful for Powder-powered engines  
    -   Low numbers draw the explosion out, lowering the peak force at any one moment but allowing the explosion to last longer. This is called "brisance", the ability of an explosive to destroy things. Lower numbers make Powder better at pushing things, for example in bullets or engines.  
    -   Having the numbers too low can cause incomplete combustion in some cases, by making it too difficult to light  
    -   Higher numbers make the explosion more snappy, increasing the peak force at any one moment, but making the explosion not last as long. This increases Powder's ability to destroy things or move heavy weights  
    -   Setting to 0 disables powder combustion, useful for when you want Powder and Hot to play together  
    -   Setting to 0 and adding Fuel will restore Powder's ability to burn  
    -   When combining Powder and Fuel, the *LightProbability*and *ExtinguishProbability*for each material will interact and cause a different than usual burn pattern, usually the faster-acting variable takes control  
    -   Fuel mixed with Powder also provides the ability to put the Powder out when in contact with Water, allowing more precise control of burn patterns and explosions. Placing a small amount of water on top of/beside the Powder can make the explosion last longer  

<!-- -->

-   \`powderExtinguishProbability\`
    -   The chance that an ignited Powder particle will "burn up"  
    -   Setting to 1 causes a mass of Powder to essentially disappear when ignited  
    -   Setting to 0 results in a very energetic swarm of deadly Hot particles  
    -   Low numbers make Powder explosions last longer and makes them better at pushing and moving, generally making them more powerful  
    -   High numbers make explosions more clean and snappy with less lingering  
    -   setting the number too high can cause incomplete combustion in some cases, due to each particle not surviving long enough to light others  

<!-- -->

-   \`powderExplosionCoefficient\`
    -   My favorite. The amount of force that throws each particle away when ignited.  
    -   Setting to 0 results in a material that can be an alternative to Fuel, for example when doing experiments with [Electrical Conduction](/Electrical%20Conduction.md "Electrical Conduction")  
    -   Setting to 0 creates a material that slowly disappears without creating the fire animation, which is good for things like erosion, evaporation, dissolving, rotting, or crumbling  
    -   When each particle catches on fire, it is given this amount of speed using the same scale as *maxSpeed*and never slows down  
    -   This variable works surprisingly well with many different numbers. Overdoing this value is not the best way to make Powder more explosive. It is better to decrease *powderExtinguishProbability* to make the explosion last longer, increasing it's pushing ability  
    -   Setting both this number and *powderExtinguishProbability* lower makes Powder with low brisance that is good at providing constant pressure, for example as a fuel in an engine, it also makes Powder that is good at pushing without teleporting through walls  
    -   setting this number higher makes powder much more forceful, useful for powerful explosions with a smaller, economic amount of powder  
    -   setting it too high often causes the Powder to travel so fast it can teleport through walls and itself, which actually reduces it's ability to push things and making the explosions messier and less precise  
    -   *maxSpeed* actually has an effect on the power of explosions, because increasing *maxSpeed* increases the inertial impact of each Powder particle which makes explosions more powerful, but also strongly increases the amount of "bleeding through" walls  

<!-- -->

-   \`brittlenessCoefficient\`
    -   the amount of force it takes to rip particles of Elastic or String from each other
    -   Lower values are good for things that crumble easily
    -   higher values are good for realistic creations, because it allows you to create Elastic or String features that work like normal, but will "break" when stressed too hard
    -   negative values are not possible sadly, because it causes the material to collapse instantly. I think. I haven't actually tried anti-brittle... somebody should make a video about the results.
    -   Setting to 0 just makes stuff collapse

<!-- -->

-   \`jetCoefficient\`
    -   The magnitude of Jet's force  
    -   Has an interaction with the Fire particles created by burning objects  
    -   negative values are sometimes useful, I just won't say what for right now ;)  

<!-- -->

-   \`fuelLightProbability\`
    -   How quickly fire spreads
    -   Set to 1 to have the fuel ignite instantly
    -   Set to 0 to have all your hopes and dreams destroyed
    -   Lower numbers are good to make "fuel" for lamps, or to decrease the chances of a fire spreading backwards into a container

<!-- -->

-   \`fuelExtinguishProbability\`
    -   How quickly a particle "burns up"
    -   Setting to 0 makes things burn forever.

<!-- -->

-   \`upCoefficient\`
    -   How strongly Light tries to climb against the direction of gravity
    -   Setting to a high number causes boats and airships to be easier to build, don't cheat yourself though!
    -   [Light](/Light.md "Light") and [Dense](/Dense.md "Dense") work by trying to move towards or away from gravity, when in contact with a non-light or dense particle. Actual density is not changed, the effect does not work in zero-g, and it only works with physical contact
    -   Light and Dense can be used to create a compass-like effect

<!-- -->

-   \`downCoefficient\`
    -   How strongly Dense tries to fall towards gravity.
    -   if *up* and *down* coefficients are set to the same value, the material LD will be neutral
    -   setting one higher or lower can make LD that is slightly heavier or lighter than Water, allowing four separations - Light > L+D > Water > Dense for example.

<!-- -->

-   \`yukiSpringCoefficient\`
    -   How sticky [Snow](/Snow.md "Snow") is.
    -   Higher numbers make it glue-ey
    -   Lower numbers make it more watery
-   \`yukiMeltingProbability\`
    -   How "cold" snow is, changes how fast Snow melts itself

<!-- -->

-   \`resistanceFlag\`
    -   Makes all particles require energy to travel, instead of moving forever
    -   Causes objects to gradually loose speed, useful for top-down games
    -   Creates a very different atmosphere for the game, almost Falling Sand-esque
    -   Very little performance impact

<!-- -->

-   \`resistanceCoefficient\`
    -   How quickly particles change their speed
    -   Small positive values can make the game feel nicer, less speedy and messy
    -   Small positive values change how water flows and splashes in particular
    -   Positive values can be useful to control particle behavior when *dampingFlag*is disabled
    -   Negative values cause particles to always attempt to speed up, this causes very strange flow patterns, sometimes even self-flowing rivers
        -   truely stationary particles will never move, because you can't accelerate off of 0
        -   Gas will seem to have an internal pressure, it will push back with a certain force and can inflate Elastic balloons
        -   small to moderate negative values can enhance vorticity and flow when doing large-scale fluid experiments, by counteracting OE-Cake's natural internal friction in fluids
        -   moderate to high negative values act like omnidirectional gravity, this sounds cool but usually just results in everything going crazy
        -   maximum craziness with negative values can be controlled with *maxSpeed*

<!-- -->

-   \`fireFlag\`
    -   Whether or not to render the Fire shader

<!-- -->

-   \`fireProbability\`
    -   How likely a given Hot+Fuel (or Jet+Hot) particle will emit a fire particle
    -   A value of 1 produces a completely solid flame, useful for following extremely fast moving objects or creating tracers or visual light shows
    -   Low values are good for bulk materials, special effects, or to improve performance
    -   Higher values make brighter fire, by spawning more fire textures faster
    -   Also remember the fire texture can be changed, allowing more possibilities
    -   If you want to make your own fire texture, relatively low opacity is best

<!-- -->

-   \`fireLife\`
    -   How long a fire particle will last
    -   Gradually fades during this time
    -   negative values are strange

<!-- -->

-   \`fireBouyancyCoefficient\`
    -   How quickly fire particles will travel upwards
    -   Useless without gravity
    -   can also be set negative

<!-- -->

-   \`splashFlag\`, \`splashProbability\`, \`splashExpansion\`, \`splashMinLife\`
    -   Splash stuff
    -   Increasing *splashProbability* and lowering *splashMinLife* and *splashExpansion*can create splashes that more closely represent the splash behaviour, by making it more sensitive to smaller effects and reducing the tendency for Splash particles to smother what you're looking at.
    -   *splashExpansion* represents how far a Splash texture flies compared to how hard the splash was, I personally like this value quite low because it makes the splashes stay closer to the source and be less goofy

<!-- -->

-   \`bubbleFlag\`, \`bubbleProbability\`,  \`bubbleLife\`, \`bubbleBuoyancyCoefficient\`
    -   Bubble stuff.
    -   Bubble and Splash have an impact on performance and are both very broken. The Bubble and Splash particles don't always fade away, leading to a screen eventually covered in mist. Which is probably why they are disabled by default. They both work sometimes, but expect them to fail eventually. Especially Bubble. It's pretty broken. Bubble only dissolves when there is water nearby, so deleting Water while it's bubbly can cause the bubbles to be permanently left behind. Neither Bubble nor Splash ghosts are saved so you can get rid of them by saving and reopening.

<!-- -->

-   \`pouringFlag\`
    -   Whether or not to Pour/Inflow

<!-- -->

-   \`pouringRainFlag\`
    -   The Rain mode

<!-- -->

-   \`pouringLocation\`
    -   Pouring offset
    -   Uses same units as *boundsRight*, so if your *boundsRight*is 100 than *pouringLocation=100*will be close to the right edge

<!-- -->

-   \`pouringThickness\`
    -   Size is relative to *boundsRight* units
    -   pouring width increases symmetrically

<!-- -->

-   \`pouringVelocity\`
    -   Speed of particles when spawned
    -   Uses same metric as *maxSpeed*

<!-- -->

-   \`pouringTimer\`
    -   Appears to be a random number
    -   Cannot be changed
    -   perhaps has something to do with undersampling the pour vs. the framerate?

<!-- -->

-   \`pouringMaterial\`
    -   The atomic number of the element you wish to pour.
    -   Simply input a recipe code here to pour any arbitrary combination of elements
    -   Sadly it does not seem like it is possible to set a custom color for the given material
    -   see [save file manipulation](/.oec%20File%20Manipulation.md ".oec File Manipulation") for how to obtain a recipe code

<!-- -->

-   \`pouringLayer\`
    -   Evidence of layering?
    -   Doesn't seem to affect anything.

<!-- -->

-   \`clearFlag\`
    -   Enables and disables the background color
    -   Also background/foreground textures

<!-- -->

-   \`clearColorRed\`, \`clearColorBlue\`, \`clearColorGreen\`, \`clearColorAlpha\`
    -   The RGB values representing the background color, on a scale between 1 and 0. To convert the R, G, or B component of your desired color to the scale used by OE-Cake, use this formula:
    -   desiredValue = rgbValue / 256
    -   for example, white would be 1 for all of them, black would be 0 for all of them, and middle grey would be 0.5 for all of them

<!-- -->

-   \`mouseRadius\`
    -   The size of the Move/right-click-drag function
    -   smaller numbers give more precision and force
    -   larger numbers spread out the force for moving delicate things, and even larger numbers allow you to "grab" something completely

<!-- -->

-   \`mouseDelay\`
    -   Over how much time the Move/right-click-drag function applies velocity to particles
    -   Lower numbers result in sharp and speedy dragging, higher numbers result in more "throwey" or "windy" dragging
    -   A moderately high number is ok, it averages out your motions and makes sure one place on the creation doesn't take all the force

<!-- -->

-   \`mouseForce\`
    -   The maximum force you can put onto particles
    -   Useful for making a less aggressive throw tool, for working with gas/water or delicate creations.

<!-- -->

-   \`lineWidth\`
    -   Drawing radius for Brush
    -   Can be used to create easy perfect circles of any size

<!-- -->

-   \`usersCharge\`
    -   Whether or not a piece of Users is touching a particle "below" it, in the direction of gravity
    -   This causes a sudden kick of force in the "upwards" direction, with speed equal to *usersSpeedY* but a force higher than *usersForceY,*and then stops more positive force on the Y axis while in the air
    -   A slightly clumsy way of handling the problem of jumping, because it only takes one Users particle to be touching some "ground" and every particle is affected, also works pretty badly in water/gas

<!-- -->

-   \`usersMaxCharge\`
    -   The maximum jump velocity for Users, when in gravity and touching a floor-like surface
    -   Might be a multiplier for *usersForceY*
    -   Is used to make jumps be more aggressive than just normal upward movement

<!-- -->

-   \`usersSpeedX\`
    -   The maximum velocity possible for Users to travel under it's own power along the x-axis of the screen

<!-- -->

-   \`usersSpeedY\`
    -   The maximum velocity possible for Users to travel under it's own power along the y-axis of the screen

<!-- -->

-   \`usersForceX\`
    -   How quickly Users will accelerate to \`usersSpeedX\` / how strong Users is along the x-axis

<!-- -->

-   \`usersForceY\`
    -   How quickly Users will accelerate to \`usersSpeedY\` / how strong Users is along the y-axis

<!-- -->

-   \`usersX', \`usersY\`
    -   User's current impulse
    -   Manually entered numbers will be held until you press an arrow key for that axis
    -   Can be used to make Users always try to move along a given axis, makes some veeeeery weird fluids
    -   Users+Gas, with low *usersSpeed* and low *usersForce* values, and a manually entered *usersX/Y* value, will act like it's in gravity. It will always move a certain direction, it's really weird. You can make it fall up, or to the side, or into the corners.
    -   Very small *usersForce* values mixed with moderate *usersSpeed*values can be used to precisely change the effective density of Users+Water. Setting *usersY* to a small positive number will effectively make the Water less heavy, and small negative numbers will effectively make it slightly more heavy

<!-- -->

-   \`viewWidth\`, \`viewHeight\`
    -   Your window size.
    -   Can be used to force a given window size, irrespective of \`boundsLeft\`, \`boundsRight\`, \`boundsBottom\`, \`boundsTop\` only when *scrollFlag* is enabled.
    -   The *bounds* variables can be used to make an extremely large canvas, then the *view* variables can be used to make the window sized normal for your screen, even if you can't see the whole canvas

<!-- -->

-   \`scrollFlag\`
    -   An interesting display mode
    -   When enabled, will allow you to move just the viewport to a different part of the canvas, without changing the boundary location or any particle location, allowing you to "look" around an extremely large level
    -   Can also be combined with *scale* to effectively zoom the view without changing the canvas size
    -   Also, disconnects viewWidth/viewHeight from boundsRight/boundsTop, allowing you to change the window size without affecting the things that have been drawn
    -   Very useful for projects you intend to share, because a person's screen size will no longer resize the canvas.
    -   Sometimes OE-Cake on Windows will not respect this setting, more testing is needed to find out why

<!-- -->

-   \`scrollX\`, \`scrollY\`
    -   The offset for translating the viewport to a different location
    -   The units are the same size as *boundsRight* and *boundsTop,*so if your canvas is 100 units wide, setting *scrollX*to -50 will put it close to the middle
    -   that's right, *scrollX*and *scrollY*are backwards, negative numbers move to the right and upwards for some daft reason

<!-- -->

-   \`scrollAngle\`
    -   Rotates the viewport to an arbitrary angle in Radians, just like *gravityAngle*
    -   Useful for watching everything upside-down... I guess
    -   Useful when combined with *gravityAngle* and the *bounds* variables (to resize the rotated window to fit your screen), because you can make the "pour" stream or the Rain come from any side of the screen. Technically the "pour" always comes from the "top", but you can visually rotate the top to another side, change the window to fit, then change the angle of gravity to make it seem normal. This change has no known impact on physics. However I'm now wondering how this would affect the anisotropic nature of [Electrical Conduction](/Electrical%20Conduction.md "Electrical Conduction") and extreme explosions...

<!-- -->

-   \`colorFlag\`
    -   Toggles between Material and Color viewing mode
    -   Whether or not to render arbitrarily colored particles
    -   Pretty sure this was added in the update because materials were not originally able to be colored

<!-- -->

-   \`renderMode\`
    -   Viewing mode.

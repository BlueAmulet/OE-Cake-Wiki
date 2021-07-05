With enough patience, it is possible to use Water/Gas to generate hydraulic pressure that powers creations.

[Hydraulic Slingshot](https://www.youtube.com/watch?v=ENg_6IxN3xk&feature=youtu.be)

[Hydraulic Cannon](https://www.youtube.com/watch?v=Ww6M7GFnHww&feature=youtu.be)

Here are some steps:

-   <u>Generating Pressure</u>

The easiest way by far is to use the Pour (Windows) / Inflow (OSX) mode. This mode just keeps adding particles until the game crashes or something blows up, or you use the pressure to accomplish work. Be sure to have Outflow somewhere to vent excess particles.

-   <u>Walls</u>

Normally under high pressure, particles can squish through walls and generally not go where they are supposed to. Setting the StandardDistance parameter to 0.5 allows you to draw much denser walls that can withstand much higher pressure. Remember to return the value to 0.75 for normal gameplay because it changes how things behave and may break the device.

-   <u>Watertight Valves</u>

In order to direct your water through various pipes you must have a valve system. The easiest way to open and close valves is to make them out of the material JUR, which is User-controlled Jet. The valve should just be a loose-fitting rectangle in a cubby hole, that can move up and down or side to side.

[Valves in action](https://youtu.be/Ww6M7GFnHww?t=92)

-   <u>Pistons or other Outputs</u>

Obviously this water pressure must be used for something. In *Hydraulic Slingshot*, water pressure is used to stretch an Elastic band, storing energy for firing a projectile. In <span class="">*Hydraulic Cannon*, water pressure powers a piston that aims the cannon, an Elastic band to fire the projectile, and a reset mechanism to return the firing pouch to it's original location. Water pressure could also be used for a firehose, to lift something, or many other purposes. </span>

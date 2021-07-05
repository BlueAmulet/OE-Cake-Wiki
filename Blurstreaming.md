**Blurstreaming** is a technique related to [Jetstreaming](/Jetstream.md "Jetstream") which allows us to observe the internal properties of the particles and produce more visually rich simulations. In [Circles (Blur)](/Circles%20%28View%20Mode%29.md "Circles (View Mode)") view mode, the particles will leave a tail behind them when they move quickly or are subjected to forces. The *timeStepsPerFrame* [Parameter](/Parameters.md "Parameters") influences the length of the tail as it relates to the forces involved. Sadly this also affects simulation speed which requires a careful balance between the desired tail length and the desired temporal resolution.

When a particle travels very fast or is subjected to extreme forces, it generates a tail that is directional and proportional to the forces involved. The tail adds color and brightness to the pixels, allowing the space between particles to be filled or to highlight changes in velocity or pressure. With this knowledge it is possible to design a simulation where the tail forms a significant portion of the visual result, providing visualization distinct from the particles themselves. [Velocity Painting](/Velocity%20Painting.md "Velocity Painting") is such a technique, where the collective tails of many particles are manipulated in such a way as to draw patterns.

Blurstreaming can be used to observe more detail in fluid simulations by highlighting flow and pressure.  
<img src="/images/Screen%20Shot%202016-01-31%20at%202.15.35%20AM.png" title="fig:Screen_Shot_2016-01-31_at_2.15.35_AM.png" width="768" height="768" alt="Screen_Shot_2016-01-31_at_2.15.35_AM.png" />
<img src="/images/SNiXjjW.png" title="fig:SNiXjjW.png" width="768" height="768" alt="SNiXjjW.png" />
<img src="/images/Elastic%20Force.png" title="fig:The simulation only has a handful of particles but the extreme tails give the impression that the screen is full. This was caused by modifying Elastic&#39;s Parameters to generate extreme internal force" width="768" height="768" alt="The simulation only has a handful of particles but the extreme tails give the impression that the screen is full. This was caused by modifying Elastic&#39;s Parameters to generate extreme internal force" />  
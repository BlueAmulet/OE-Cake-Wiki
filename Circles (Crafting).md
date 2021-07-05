There are three ways to create perfect circles in OE-Cake:

## Parameters

-   Change *lineWidth* in the [Parameters](/Parameters.md "Parameters") to the desired radius of the circle. Using the Brush or Replace tool, click and move the mouse very slowly until the tool activates. This techneque produces circles with a rough edge so it may be necessary to use another technique to create a smooth edge.

## Material XOR

<img src="/images/Screen%20Shot%202015-12-09%20at%2018.12.04.png" title="Material XOR being used to cut a complex radial shape" width="220" height="220" alt="Material XOR being used to cut a complex radial shape" />

-   Using the material XOR, one can cut perfect circles out of a block of Wall. Create a block of Wall at least as large as the desired circle, then place a 2 or 3 particle-wide beam of XOR, centered, in the block, as tall as the circle needs to be. If the circle is small enough you can drag the beam around with the mouse, but if it's too large you should replace a small section of the beam with XORJ, which should make it start cutting automatically.

<!-- -->

-   If you cut symmetric patterns out of each end of the bar of XOR you can create complex radial patterns or features such as an axle. The XOR method works best on very large circles with a high particle count because it can be automated using Jet. This technique produces circles with a rough edge so it may be necessary to use another technique to produce a smooth edge.
-   This technique makes it easy to create higher quality circles using the "tape"material, Elastic + Mochi. After you have cut your circle, draw a few straight lines of tape inside the circle and stick them to to the walls. The Elastic's natural stiffness will smooth out bumps and the Mochi will help hold it in place.

## String + Gas Pressure

<img src="/images/Screenshot%20from%202019-03-24%2013-23-41.png" title="The outside material is String and the inside material is Tensile. Notice how the circle is nearly perfect despite the low particle count. The four extra particles are the corner particles of the String square. This is a perfect way to create axles. " width="220" height="220" alt="The outside material is String and the inside material is Tensile. Notice how the circle is nearly perfect despite the low particle count. The four extra particles are the corner particles of the String square. This is a perfect way to create axles. " />

-   A recently discovered technique allows perfectly smooth circles of any size. Simply draw a rectangle of String, then Delete all of the interior particles leaving a 1 particle thick boundary. Fill this with Gas + Inflow to create a self-inflating balloon. This works because Gas pressure pushes evenly in all directions, and String has no stiffness between particles so it is free to take whichever shape it feels like. A lower *standardDistance* value can also be used to 'inflate' the String balloon. This is the only technique that produces perfect smooth edge on the first pass.
-   Originally discovered by:

<img src="/images/E%20L%20A%20S%20T%20I%20C%20OE%20Cake" title="E_L_A_S_T_I_C_OE_Cake" width="330" height="330" alt="E_L_A_S_T_I_C_OE_Cake" />

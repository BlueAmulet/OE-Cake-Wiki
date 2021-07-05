<span>The **Background Color** (BG Color) is a setting in OE-cake that can be changed. It is useful when using a view mode such as </span>[Points](/Points.md "Points")<span> to add contrast to make everything more visible. Changing the background color drastically affects the mood of a project. </span>

To change the background color:

-   OSX: click the right color tab on the Tools box
-   Windows: click the "BG Color" button on the "Scene" tab
-   Background Image: create a solid color image of the color you want and set it as the Background texture
-   Parameters: the software way to permanently change a save's background color is to change these values in the Parameters:  
    clearColorRed  
    clearColorGreen  
    clearColorBlue
-   These parameters represent the RGB values of the background color, but mapped between 1 and 0. If you want to translate RGB values into these values, the formula *desiredClearColorValue = targetRGB/256* will give you the correct value for the *clearColorRed/Green/Blue* parameter. You must perform this calculation for each of the Red, Green, and Blue portions of the background's color.

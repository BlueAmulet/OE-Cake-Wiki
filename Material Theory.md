**Material Theory** is the study of how [materials](/Material.md "Material") behave as a property of a particle.

[Theoretical Physics](/Theoretical%20Physics.md "Theoretical Physics") is the study of the most advanced and difficult simulations in the game.

[Advanced Simulations](/Advanced%20Simulations.md "Advanced Simulations") require extensive knowledge of how particles behave.

[Quantum Physics](/Quantum%20Physics.md "Quantum Physics") is the study of how numerical limitations of the game affect particle behavior.

A [Meta Material](/Meta%20Material.md "Meta Material") is a material designed to behave in a special way to produce a different effect.

[Material Science](/Materials%20Science.md "Materials Science") is the study of practical applications of the materials.

[Mixtures](/Mixture.md "Mixture") are the result of blending two materials to create new behavior.

[Material Substitutions](/Material%20Substitutions.md "Material Substitutions") permit one material to mimic certain properties of another, allowing materials to take alternative roles.

[Null Theory](/Null%20Theory.md "Null Theory") is the study of the Extraneous Nulls and their uses in the game.  

## Materials

Within the game, materials are stored as a 32-bit number. However, it's better to think of it as a "switchboard" with 32 toggle switches. Each switch is either up or down. If the switch is up, the particle contains the respective element. Otherwise, it doesn't. All switches down produces [True Null](/True%20Null.md "True Null"). If only switch 1 is up then the material [A-Null](/Null.md "Null") will be drawn. If switches 2 and 3 are up, the material Brittle + Cold will be drawn.

Each [element](/Material.md "Material") has specific programming that alters how the particle behaves and interacts with other particles. Combinations of elements can allow extensively complex interactions to emerge naturally.

Elements are the base property of a material that describes certain behavior. For example Brittle allows particles to "tear" if enough force is applied to them, however Brittle on it's own has absolutely no special behaviors and acts just like Null unless it is combined into a mixture containing String or Elastic.  
![The numbers above and beside the table represent the hexadecimal encoding of each material in the save file\|alt=](/images/Elements.png "The numbers above and beside the table represent the hexadecimal encoding of each material in the save file|alt=")

### Save File Material Numbers

The numbers outside the table represent the associated materials and how they are saved in the file. If you want to create a given material, be it a single element or a large recipe, the numbers beside the table are critical. Simply multiply the top numbers by the side numbers to get a given element - for example Gas is at horizontal position 4 and vertical position 10, so pure Gas will be saved in the file as material number 40. To mix elements, simply add their numbers together - for example Fuel is at position 2 and 10, making it element number 20. So Gas + Fuel = 40 + 20 = material number 60 in the save file. If you wanted to make Gamma Gas it would be Gas (40) + Gamma (10,000,000) = material number 10,000,040 in the save file. However one must remember the material number is hexadecimal, so numbers bigger than 9 don't immediately "rollover" - in hex, the next number is 'A' then through till 'F' to represent 16 increments. Normal addition is sufficient for simple recipes but using a programming calculator to activate the appropriate bits makes it much easier to find the code for complex mixes. Each of the 32 bits represents an element in alphabetical order with bit 1 being A for A-type Null and so forth. Alternatively one could simply add the numbers normally then convert the resulting decimal number to hex.

### Modifying the Save File

[Save File Manipulation](/.oec%20File%20Manipulation.md ".oec File Manipulation") is the practice of using external programs to modify the save to produce results otherwise impossible within the game.

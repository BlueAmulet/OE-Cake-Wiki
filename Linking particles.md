![Rigid that's been linked.](/images/Link1.jpg "Rigid that's been linked.")**Linking particles** is a useful technique in OE-Cake that allows distant particles to move as if they are stuck together. This technique allows very complicated creations to be made.

## Methods

### Replace

To link particles, use the [Replace](/Replace.md "Replace") tool with Rigid to paint over all shapes you want linked. Only works with Rigid objects, be careful not to touch anything you don't want linked.

Also, if you use the Replace tool with the Delete element, you can cut holes in Rigid without it falling apart.

Modifying *lineWidth* in the Parameters alters the precision at which particles can be grouped. If attempting to link many or distant particles, sometimes it is easier to link a few random ones nearby so you can reposition the screen before also linking the intended particles, then removing the placeholder particles once the final shape is achieved.

### Paint Spillover

The Paint tool merges nearby groups of particles that have the same material and color. You can create a custom material, set a custom color, paint two shapes, then when you click one of them a second time, it will automatically bind them together. I believe the Paint spillover distance can be controlled in the Parameters by modifying the *standardDistance* parameter. This method can also act somewhat like a "magic wand" tool since you can vary the select range based on particle distance.

### Pencil Modifications

The Pencil tool is also capable of merging shapes, as well as drawing on existing shapes without harming them. It's easy - carefully start drawing so the first particle is *very* near the surface of the shape, but does NOT overwrite anything. If drawn particles are close enough they will bond to the shape and allow you to add changes non-destructively. By carefully positioning shapes and aligning the first and last particles in the linking line, it is possible to draw an addition from one shape to another bonding them both without overwriting particles, at which point you can use Replace + Eraser like usual to cut holes where needed.

### Save File Modification

The easiest and most powerful method of linking particles. The [.oec file](/.oec%20File.md ".oec File") is organized in a fairly simple manner. The third column in any given particle is the "group index" it is part of. All Rigid particles have an index that represents which particles are part of it's family. By drawing shapes in the exact position and configuration needed while the game is paused, and making the shapes a distinctive color, it is trivial to use a regex program or even just Find and Replace to simply make all particles of that color part of the same group. This eliminates the tedious and often difficult manner in which particles must be connected using the Replace tool.

Example:

You draw shape number 1 and this is one of it's particles:

    p 20000 1 ff 808080ff 47.5015 38.647 -0.000213921 0.000145131 47.5015 38.647 0 0 0 

Then you draw something else, then you draw shape number 2, and it's particles look something like this:

    p 20000 3 ff 808080ff 47.5015 38.647 -0.000213921 0.000145131 47.5015 38.647 0 0 0 

The first column is *p* which signifies this is indeed a particle, not a *j* join or something else in the save. Next is 20000 which is the [Material Code](/Material%20Theory.md "Material Theory") for Rigid.

Next, we finally have a difference. Particle A has a 1 and Particle B has a 3. If you only want to combine these two shapes, all you need to do is use Find and Replace in most text editing programs. Simply Find all *20000 3 ff 808080ff*'s in the file, and Replace them with *20000 1 ff 808080ff* then open the save and voila! The two shapes are now linked exactly as they appeared.

By using different colors you can easily create separate groups. By drawing the shape you want linked and immediately saving, it will be the final group of particles at the bottom of the save making it easy to identify. Using a color picker that supports hex makes it easier identify different groups of particles.

## Caveats

Be careful not to hurt the Rigid shapes, because they will fall apart. Do not burn them, draw on them with any tool, let them touch [Outflow](/Outflow.md "Outflow"), or otherwise change them in any way, because they will forget their attachment and fall apart. The group index limits the game to 256 groups, which puts a hard cap on the maximum number of blocks of Rigid that can be in play at once. This means any mechanical machine will be limited to that many Rigid components, Rigid used for decorative purposes (ie. gravel or letters or something) will be limited to 256 entities, and the burning behavior of Fuel will be different in the presence of complex machinery.

Examples:

<https://www.youtube.com/watch?v=EKt1VgV81iQ&feature=youtu.be>

<http://www.youtube.com/watch?v=hfmg0uRcHBY>

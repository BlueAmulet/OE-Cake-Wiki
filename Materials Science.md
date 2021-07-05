**Materials science** is the process of engineering substances. Not to be confused with chemistry or [material theory](/Material%20Theory.md "Material Theory"), materials science is less concerned with how materials work within the game itself and more with the design of new materials for various uses. In the context of materials science, "material" is more loosely defined and includes [allotropes](/Allotropy.md "Allotropy"), [metamaterials](/Meta%20Material.md "Meta Material"), [parameter editing](/Parameters.md "Parameters"), and combinations of these techniques.

  

## Material

An important part of engineering materials is the [material](/material.md "material") itself. The materials in question are generally solid ([Wall](/Wall.md "Wall"), [Rigid](/Rigid.md "Rigid"), [Rigid Axis](/Rigid%20Axis.md "Rigid Axis"), [Elastic](/Elastic.md "Elastic"), [String](/String.md "String"), [Brittle](/Brittle.md "Brittle"), etc.)

  

### Metamaterials

In the context of materials science, [metamaterials](/Meta%20Material.md "Meta Material") are considered their own materials. Combining materials can help bring out properties that would be hard to obtain otherwise.

  

## Structure

The structure of the particles in the material is important too. This includes density, [allotropy](/allotropy.md "allotropy"), organization of different particles in metamaterials, and other properties. Structure does not have to be consistent throughout the entire material; for example, there could be a material with an outer "shell" with a different structure than the center.

  

## Production & Processing

Materials science concerns the engineering of materials for specific or general applications, so it's necessary that there be ways to synthesize materials and fashion them into the desired shape. See the [Circles (Crafting)](/Circles%20%28Crafting%29.md "Circles (Crafting)") article for discussions about various techniques related specifically to making circles.

  

### Shaping

Many applications of materials require specific shapes. Depending on the material, there are different ways to form it into the desired shape.

  

#### Carving (subtractive)

A common method of forming material into a desired shape is to create a block of material larger than the final product, then subtract material (via [Eraser](/Eraser.md "Eraser")) until the desired result is achieved. If a mistake is made and too much material is removed, the undo function can be used to undo the mistake.

  

#### Casting

If a specific shape needs to be created several times with high precision, then the method of casting can be used. Casting first involves creating the subject that a cast will be made of, through any other shaping method. Then, a cast is created by submerging the subject in a fluid and replacing the fluid with [wall](/wall.md "wall") (using [Bucket](/Bucket.md "Bucket")). The subject is removed, and the cast is trimmed down into the appropriate size. A hole is created at the top of the cast to pour a fluid into, then the fluid is replaced with the desired material and removed. The cast can be reused ad infinitum to create several rough copies of an object. Casting can be an effective technique for creating ammunition or obstacles.

  

#### Smoothing

Many techniques fail to produce shapes with smooth surfaces. One method to produce a smooth surface is to use the "tape" material Elastic + Mochi. By drawing lines with the Pencil tool or using the Shape tool to produce thin lines, one can stick the layer onto the surface of the shape and effectively average out irregularities. This will position particles in a consistent manner relative to each other, producing a surface that can handle pressure from fluid or mechanical means.

  

### Precision

Precision is critical for creating strong and efficient components. The game automatically aligns newly created particles to a grid based on display pixels, even though the internal location precision is much higher than visible. It is impossible to draw two separate particles closer than a pixel without changing Parameters. All tools align particles first to the display grid, then subsequent particles will be positioned relative to *standardDistance* offset from the starting particle.

Using operating system based tools such as handicap/accessibility tools can permit higher precision drawing, by controlling mouse movements or zooming the display.  

##### Alignment

Precisely aligning particles can be difficult since OE-Cake has no "snapping" functions to ensure particle alignment. Misaligned particles reduces the smoothness and efficiency of machines.

Whenever possible, subtractive drawing techniques are often the fastest and easiest ways to ensure alignment. By starting with a block of Wall that is larger than the required shapes, one can delete particles where necessary ensuring all components are aligned to the same grid.

Occasionally it is needed to align other completed shapes to add to them - by creating a tight-fitting box one can wedge the required shape inside of it. If the resolution (number of particles involed) is low enough and the particles have the same spacing, the particles will sit between each other firmly locking themselves in place.

The material Wall + User is very effective for precision alignment. Changing the User's parameters allows the arrow keys to move shapes with varying degrees of speed and precision. This material can also be used effectively to align shapes to the X or Y axis - by drawing a thin line with the Shape tool you can slowly move it closer and closer to the shape until it flattens against the line.

Rigid+Axis allows shapes to be rotated with precision. Euclidean geometry techniques can allow arbitrary angles and precision alignment.

#### Measurement

Precisely measuring distances in the game is fairly limited, essentially the only options are to draw shapes in the game or take a screenshot and measure pixels. One could also create a background texture but this requires a view mode that is harder to draw in. The most precise method involves editing particle locations in the save file.  

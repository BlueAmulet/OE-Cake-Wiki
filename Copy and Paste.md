OE-Cake has the ability to copy and paste entire creations from one save to another. This is because the save file does not have a special format, all particles and Parameters are just normal numbers and letters. Since each file is just text, we are able to copy and paste creations from one file to another. This allows a person to create many copies of something, to position things in a different save without unpausing the main save, and to run different simulations with different Parameters and combine the results. Aided by [regex techniques](/.oec%20File.md ".oec File") the possibilities are endless.

## Techniques

There are multiple ways to **copy and paste** objects in OE-Cake, each has their advantages and disadvantages.

See the [.oec File Manipulation](/.oec%20File%20Manipulation.md ".oec File Manipulation") article for techniques related to repairing broken saves and more advanced operations.

  

### Basic Techniques

[Save file](/.oec%20File.md ".oec File") modification takes advantage of the fact that the OE-Cake's save file is stored as plain text. The easy techniques works best when the only particles on the screen are those you wish to copy, it is very difficult to tell which particles belong where in a complicated creation. Copy and pasting is capable of remembering material type, velocity, particle rotation, color, and more, but has trouble with solids such as Rigid and Elastic. When pasting particles, one must ensure that the content begins on a new line - in the new save, you must click after the final particle, including it's trailing space character, and hit 'enter' to create a new line, and then paste the content. This ensures the first particle from the new content is on it's own line and not pasted onto the final particle in the new save. It is easy to have errors in this manner, for example depending on exactly how you selected the particles in the first save, you may have accidentally selected the hidden 'newline' character and when you paste, there is now an extra blank line between the old particles and the new particles, which will break the save.

  

#### Drag And Drop

Simply copying everything from one save to another (except the header and Parameters) is good for precisely copying shapes made out of Wall, as well as static and flowing fluids. One can simply highlight all the particles in one save, then drag and drop them after the final particle in the new save. Detailed creations can be pasted and easily returned to their original materials if every piece is a different color. When pasting the object, it occasionally works at the top of the OE-Cake save file, but pasting works more reliably when the object is pasted at the bottom of the save file. Rigid, String, and Elastic cannot be easily copied and pasted but it is possible with [proper techniques](/.oec%20File%20Manipulation.md ".oec File Manipulation").

1.  Create the shape you wish to copy and paste.
2.  Save the file to somewhere you can access it.
3.  Open the file with a text editor. If the save only contains the shape you want copied, the procedure is simple.
4.  All of the numbers between the header (# OctaveEngine Casual (Sep  1 2008) version 2) and the [Parameters](/Parameters.md "Parameters") at the bottom of the file represent your shape. Select all particles (not including header or Parameters) and copy them to the clipboard.
5.  Re-open the file in OE-Cake.
6.  <span>Use the </span>[Move](/Move.md "Move")<span> tool to move your creation out of it's current location, unless you want to paste the new particles right on top of it. </span>
7.  Save.
8.  Re-open the file in a text editor, and paste the old series of particles above or below the current list.
9.  Save the file with the text editor and *make sure* the file ends in .oec
10. Open in OE-Cake and enjoy two copies of your shape.  

<img src="/images/Two%20Stroke%20Double-Action%20Jet%20Powered%20Buggy" title="An example video of a creation in OE-Cake that was partially made using the copy and paste technique. Jump to 8:00 for the demonstration|none" width="330" alt="An example video of a creation in OE-Cake that was partially made using the copy and paste technique. Jump to 8:00 for the demonstration|none" />

#### Texture remapping

This technique takes advantage of OE-Cake's ability to import pictures into the game and it's ability to convert pictures into patterns of particles.

OE-Cake can sometimes save textures, but only when their file path does not contain any spaces or special characters and the file stays in the same location, for example in the same folder that the saved .oec file resides in. If there is an error recovering the original texture file (such as the picture being deleted or the save file gets moved), OE-Cake will revert to a series of colored particles in the same pattern as the original image. These particles can then be deleted and/or [Replaced](/Replace.md "Replace") to generate a new copy of an [object](/object.md "object"). This technique is prone to slight rasterization errors and cannot remember different material types. It is good for quickly creating many simple objects.

Video demo here: <https://www.youtube.com/watch?v=5cZ-uIF7n9M&feature=youtu.be>

1\. The real first step is to make your creation. It doesn't matter what viewing mode you're in for this part.  

2\. Now, switch to crosses. Circle mode also works, but seems to be a bit less reliable.  

3\. Extract a screencap of your item. A close crop is more practical. This works best if the object is completely vertical or horizontal. If you make your image a PNG you can use alpha to control exactly how it's printed. All pixels with an alpha level below 50% will not be printed.  

4\. Before you place an image, chose your material and StandardDistance. Using finer StandardDistance combined with a photo taken in Blob viewing mode can produce very smooth, reliable objects, with the downside that they cannot be made as fine because the Blob shader makes everything... well, blobby. In general it's best to print at a StandardDistace and Scale equal to your original creation.

5\. Drag and Drop as many as needed. On my system, occasionally I needed to drag multiple times to get a single print. Sometimes it would only print black particles. Drag and Drop does not seem to work on a long-running project, so if you just can't get it to work, save close and reopen the project then try again. You can see the original photo in Blob (Texture) mode. You can reposition the textures with the Arrow/Move tool or by right-clicking, but cannot yet modify or clean them up.

6\. After you have placed as many instances as you want, SAVE the game. This converts the image(s) into a matrix of StandardDistance resolution in the material (including custom) you specified. Then close and reopen. Since OE-Cake! does not save the original images, you now have just a bunch of particles, preferably colored and positioned as they appeared in the photo.  

NOTE: If you are printing detailed, antialiased, or blurry images, you are likely to have distortion (mainly from reduced resolution) and you may need to clean up a halo around the object. Also visible in the video, not every print was made equal. One was a little stumpy. So either print one at a time and check every print, or print more than you need and delete the excess/duds. 

7\.  If you did not use transparency or postprocess your image, you will likely need to delete the (apparently) invisible background particles from around your object. If you made your object with multiple colors, it is easy to make each part of a different material, for example making multiple missiles for a launcher. You can use the Material viewing mode (hotkey: 0) to check whether you deleted all of the background material. 

Extra: If you want to print detailed and accurate photographs/real images into OE-Cake, set StandardDistance to 0.1. This works best if they are pretty small because you're printing a \*lot\* of particles all at once. However StandardDistance at 0.2 is adequate. 
<img src="/images/Nu9abrB.png.jpg" title="A screenshot inserted into the game with StandardDistance=0.2 and Viewing Mode Circles" width="220" height="220" alt="A screenshot inserted into the game with StandardDistance=0.2 and Viewing Mode Circles" /> 

### Advanced

#### FF particle grouping

Currently there is an apparently unused variable attached to all particles. Hypothetically this variable could be used to tag diverse particle types into groups without affecting their color.

#### Quicksaving

There are two techniques that enable more precise manipulation of the save file. Temporal saves create time gaps that can be easily selected in the save but provides no way to single out shapes. Spacial saves help select individual components for transport to the new save.

##### Temporal

Previously we had no good method of differentiating parts of the save, meaning that creations needed to be copied and pasted in bulk, we couldn't select a certain section. This technique has its pros and cons but is one more tool in our belt.  It takes advantage of the temporal ordering of the save file, each new particle is added to the bottom in an orderly manner. This makes it easy to place "markers" before and after we start building a different section of a save, but it does not behave like a normal "selection" tool style of copy and paste which would allow us to visually select the desired particles. This technique creates a persistent marker that will never forget the range of particles it represents, allowing a simulation to be iterated into a new state, permitting the particles to develop new positions and velocities before being copied.

It's actually fairly easy. Whenever you want to quicksave, just place a single particle of Wall in a corner of the screen where it won't hurt anything. In fact you could place it within the empty space in the rounded corners of the screen and it would have no impact on any running simulation at all. Make it a color that you would never actually use in your creation, like bright pink. If you place a particle before you start building a different section of the creation, you will have a marker in the save file that you can find later. When you are done a section you place another dot of that same color beside the first. In the save file these two particles will be very distant because of the other particles you drew in between. When you want to copy a certain section of the creation that you quicksaved, you can use the Find tool in Notepad to search for all bright pink Wall particles only, and it will show you the different sections of the creation between each particle. This is because all particles drawn after you placed a pink Wall particle will also be after it in the save. If you use many dots of pink Wall you can divide your save up into many different sections.

By using different shades of color you can "modulate" the saves and have multiple different interleaved "save files", allowing many distinct groups of particles to be targeted. This is a highly advanced technique that probably doesn't have a whole lot of utility, but I could see it being useful to provide "save groups" by using different colors to encode saves around different parts of a creation as you create them. Like I could use the color A00000 at the beginning and end of the whole creation so I can copy the entire thing at once if I want, then I could use the color A00001 before building just the wheels on a car, then the color A00002 to represent the engine, and A00003 to represent the body, and so on. By placing particles at specific times, they will create bookmarks in the save as new particles are added in order.

##### Spacial

There are some ways to isolate specific zones of a save for copying but they are generally clumsy and limited. The Replace tool allows you to paint specific sections a very unique color that you can search for later. The Bucket tool makes it easy to one-click-pick many parts from a creation. These work best while paused. Pretty much any time you can use the tools to change the color of particles, you make it easy for yourself to Ctrl+F all particles of that color and cut them from the save to move to the other save. It is harder to copy fluids and this technique is not capable of copying creations with detailed color information.

By using the Pencil tool to create dots of a specific color at important locations, you can use that particle as a spacial reference point from which to use regex to find all particles within a given distance, for example. Using advanced functions and some math it would be pretty straightforward to copy and paste arbitrary geometry out of a sim. Using just 3 dots it is possible to reconstruct a bounding volume around a given area.

One can plan ahead by using the Shape tool to make a block of Wall that encompasses the working area, then deleting all but the 4 corner particles. This will perfectly align particles into a rectangle, simplifying the regex operations needed to determine an area for copying and pasting.

## Usage Cases for Copy and Pasting

There are situations where copy/pasting is the best solution, and times where it is better to start from scratch.

### Pros

\- Good for copying colorful, detailed, or precise creations made out of Wall, such as mazes, gears, images, or specific patterns

\- allows you to have a "master" save where the Parameters are set up to make the final result work well, and "slave" saves that have the Parameters set up in a way that makes sense for creating that piece that is later put in the master

\- Copy/Paste is able to save speed and direction of particles, so you can make one save with Parameters that work well for an advanced gun that fires a bullet at high speed, then you can teleport the bullet into a new save with Parameters suited to a realistic target. This allows one to create an entirely new class of creations, where you can have two entirely different simulations with specially tuned Parameters that can't work together, and connect them by only the important part (such as the speeding bullet)

-Copy/Paste saves the location of each individual particle, this can be a good thing by allowing you to place objects inside of other objects in a way that would normally be impossible.

\- Copy/Paste is able to effectively clone objects, allowing mass-production, fewer errors, making the creation of large machines much less tedious. It allows the creation of very high volumes of small creations in an exponential fashion. You can double the number of objects with every copy/paste allowing you to reach a thousand objects with just 10 pastes. You can also perform linear growth by re-pasting a given number of objects over and over again.

-The principles behind Copy/Paste can be manipulated to create astonishingly complex results

\- Copy/Paste allows you to run mini-simulations on just a small part of a larger creation, as well as allowing you to un-pause only a small part of a whole machine. Imagine this - a weight is going to fall on a see-saw and catapult a cup of water across a table. You want the cup to be full, but you can't un-pause the simulation to let the water settle without the weight also falling. You can simply copy the cup to a new save file, convert it to Wall so it stays in the exact same spot, fill it with Water and let it completely settle, then copy the full cup of Water back to the original save without ever unpausing it.

### Cons

\- it is difficult to tell which parts of a simulation relate to which parts in the save file. It would be extremely tedious to pick out the exact particles you want so we are pretty much forced into copying every single particle from one save to another indiscriminately

\- Copy/Paste almost always breaks [Linked Rigid](/Linking%20particles.md "Linking particles") in both sides of the paste, Linked particles from both saves will collapse immediately or get their links confused and have random connections. It's pretty strange to see. You need to convert everything to Wall and then convert it back in the new save.

-Elastic often can't be copy/pasted either

\- Pasted particles will be in the exact same spot as they were in the original save. So if you want to have 2 of something you can't just do a straight copy/paste, you need to copy the creation first, re-open the save and move the original out of the way, save, then paste and re-open to find your second object

  

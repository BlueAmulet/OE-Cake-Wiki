<figure>
<img src="/images/Screen%20Shot%202018-10-07%20at%207.43.34%20PM.png" title="A haunt of ethereal particles. Water, boat is Fuel, Brittle person, Powder in the boat, and some Tensile Gas. " width="240" height="240" alt="A haunt of ethereal particles. Water, boat is Fuel, Brittle person, Powder in the boat, and some Tensile Gas. " /><figcaption aria-hidden="true">A haunt of ethereal particles. Water, boat is Fuel, Brittle person, Powder in the boat, and some Tensile Gas. </figcaption>
</figure>

### OSX Way

In the OSX version of OE-Cake, it is possible to use the Material Mixer to produce "ghost particles" - normal materials with the transparent Gas texture seen in Circles mode. You can have Rigid, Brittle, Powder, any material. Just select Gas or Snow from the Materials pane with the mouse, acquiring a transparent color. Go to Tools \> Attributes, and then un-select Gas and Light and re-select whatever materials you want. They will be drawn with the clear color. <img src="/images/Screen%20Shot%202018-10-07%20at%208.12.35%20PM.png" title="fig:End result of the new technique" width="262" height="262" alt="End result of the new technique" />

### Better Way

It turns out that there is a way for either OS to make any material transparent in Circles mode, and it's surprisingly easy. You just need a text editor with the "Find and Replace" function.

1.  Make a creation that you want to convert into transparent particles
2.  Save the file then open it with the editor
3.  Search for "ff" and replace all with "b2"
4.  Search for " b2 " and replace with " ff ", including the spaces. This fixes the "ff" column that was replaced by "b2" in the first pass
5.  Save and re-open the file in OE-Cake, you now have clear particles in circles mode!

Test file with clear particles

<https://drive.google.com/uc?export=download&id=15ptWQF9JprH5JgcoEjtCFLrKzXkGXmDY>
<img src="/images/Screen%20Shot%202018-10-07%20at%2011.07.41%20PM.png" title="fig:Screen_Shot_2018-10-07_at_11.07.41_PM.png" width="220" height="220" alt="Screen_Shot_2018-10-07_at_11.07.41_PM.png" />

### Transparent Particles

OE-Cake supports full transparency for all materials, but only through save file modification. OE-Cake saves color as a 30-bit hex, complete with full alpha channel. The "better way" technique is actually changing the alpha of the particles to be partially transparent. You can change the transparency to any level if you use a decimal to hex converter.

In the save file, the fifth column is the hex code for the color of the material. It's in the format RRGGBBAA, the last two characters are the hex for it's transparency. Each pair of letters represents a brightness value from 0-254, in hex. If you know the hex color of the material you want to change, you can search for and modify a single material. Sadly the transparency mostly only shows the grey background, though since each particle is clear it makes it easier to see overlap and things like pressure and movement.
<img src="/images/Invpart-1%20%28dragged%29.png" title="fig:Invpart-1_(dragged).png" width="240" height="240" alt="Invpart-1_(dragged).png" />

### Invisible Particles

In Blob view mode, any particles with a transparency less than 50% will not be rendered, making the material invisible. Sadly full transparency is not supported in Blob mode.

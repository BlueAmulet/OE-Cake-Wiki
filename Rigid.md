![Rigid, floating and with Jet inside.](/images/Rigid.jpg "fig:Rigid, floating and with Jet inside.")
**Rigid** is a green, solid material. It floats just under the surface of Water. Rigid cannot usually be snapped or broken, even with Brittle added. Occasionally, exceptional amounts of force will damage Rigid and cause it to collapse. Rigid can be used to [link](/Linking%20particles.md "Linking particles") separate pieces of a creation together and make incredibly complex simulations.

### Uses

![A fully functional engine made completely out of linked pieces of Rigid](/images/Screen%20Shot%202016-07-08%20at%2021.45.15.png "fig:A fully functional engine made completely out of linked pieces of Rigid")
Rigid is one of the most underrated materials in the game. With the discovery of linked particles, Rigid allows the user to make nearly anything you can imagine. Rigid is such a basic material, but it's how you use it that matters.  

The only setting that really affects Rigid is *standardDistance*, because it changes how dense and therefor how strong Rigid behaves.  

### Behind the Scenes

For some reason, the more dense Rigid is, the less it is able to rotate. Rigid drawn around *standardDistance*=0.2 has significant trouble rotating at all.  It is yet undetermined what causes this behavior.

OE-Cake has an internal limitation of 256 groups of Rigid particles. The number of particles in a group has no significance, but at any time there can only be up to that many separate blocks of Rigid before the game glitches, usually by not permitting further subdivisions or chaotically shuffling rigid groups which destroys detailed creations.

This means that it is impossible to use large amounts of Fuel alongside clockwork Rigid devices, and that Rigid cannot be effectively used to create something like gravel with any quantity.

[Category:Materials](/CategoryMaterials.md "Category:Materials") [Category:Image wiki templates](/CategoryImage%20wiki%20templates.md "Category:Image wiki templates")

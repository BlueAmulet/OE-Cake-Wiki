Due to the way [OE-Cake](/OE-Cake.md "OE-Cake") is programmed, it's possible for particles to have infinite velocity. For an explanation on what this means, see [Floating-Point Numbers](/Floating-Point%20Numbers.md "Floating-Point Numbers").

## Effects

The properties of infinite velocity particles have not been experimented with too much.

Based on some testing with [anti-viscous](/Viscous.md "Viscous"), they likely do not move, turn any particle they touch into infinite velocity particles, and delete themselves after a few seconds.

Note that infinite velocity particles WILL corrupt save files! If you attempt to save a file containing infinite velocity particles, it will fail to be read. This will cause particles to be deleted or broken and will reset all parameters to default. Be careful using infinite velocity particles to avoid save file corruption.

## How to achieve

The infinite velocity bug can easily be obtained with [anti-viscous](/Viscous.md "Viscous"). Large amounts of anti-viscous causes enough acceleration to reach infinite velocity, creating buggy infinite velocity particles.

Whether or not it is possible to create infinite velocity particles of arbitrary properties via save file editing is unknown, as infinite velocity particles prevent save files from being loaded. It could be possible to create a particle with finite velocity that is interpreted by the game as infinite due to rounding errors, though.

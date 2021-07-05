This page is a temporary place we will use to work on a complete overhaul of the [Recipes](/Recipes.md "Recipes") page.

If you want to add a recipe that's just a random word typed into OE-CAKE, don't. Such entries will be removed without warning if they aren't actually useful. Mnemonics containing repeated ingredients or ingredients with no effect on the material should be listed in notes and should not be included in the recipe itself.

Most recipes listed here should not contain more than a few components, as most large recipes are completely useless outside of the occasional one that looks cool.

## Recipe Codes

A "recipe code" is a string of letters that represent a recipe. If you type a recipe in using [Mix Mode](/Mix%20Mode.md "Mix Mode"), then you will get the material it represents.

An example of a recipe code would be "PIE", which creates a material that spews flammable [powder](/powder.md "powder") in all directions.

### Save File Recipe Codes

Within the save files, recipes are instead stored as a [hexadecimal](https://en.wikipedia.org/wiki/Hexadecimal) number. It works by sorting all the ingredients by alphabetical order, then finding the corresponding power of 2 (A = 1, B = 2, C = 4, D = 8, and so on) and adding them together. For more technical information, see [.oec File.](/.oec%20File.md ".oec File")

## Recipes

### Level Elements

These are various recipes that could be useful in user [levels](/levels.md "levels"), such as player characters or obstacles.

| Recipe | Name                    | Properties                                                          | Uses                                                                                                     | Notes                                                                 |
|--------|-------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| UR     | [User](/User.md "User") | Can be moved by pressing arrow keys.                                | As a player character to navigate a [level](/Levels.md "Levels").                                        | This is the material you get when you select "User" in the game's UI. |
| URP    |                         | Can be moved like UR. Destroyed by heat.                            | Can be used in levels where the player must avoid heated objects.                                        |                                                                       |
| URG    | Flying User             | Can be moved in all directions, unaffected by gravity.              | Can be used in levels where the player should not be affected by gravity while other objects should.     |                                                                       |
| UW     |                         | Can be moved in all directions, unaffected by gravity or collision. | Extremely useful for precisely positioning shapes that will later be Replaced with a different material. |                                                                       |

  
===Explosives===
Recipes that are explosive themselves or can be useful components in explosive weapons.

| Recipe | Name             | Properties                                                                                                   | Uses                                                                                                                              | Notes                                                                                                                         |
|--------|------------------|--------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| RP     | Rigid Powder     | Rigid body that burns quickly when heated.                                                                   | As a casing to contain more powerful explosives, or as a fuse.                                                                    |                                                                                                                               |
| RIP    |                  | More volatile RP that creates a more powerful explosion but is much less stable.                             | As an explosive, or a charge to detonate another explosive by violently compressing it.                                           |                                                                                                                               |
| MI     | Mochi Bomb       | Extremely volatile explosive that detonates on impact, creating large amounts of [Mochi](/Mochi.md "Mochi"). | As an explosive.                                                                                                                  | Can cause extreme lag or crash the game easily. Use with caution.                                                             |
| MIP    |                  | Flammable version of mochi bomb.                                                                             | As an explosive. Can reduce lag and make destruction more visible compared to MI, and can burn or melt targets.                   |                                                                                                                               |
| MIV    |                  | More stable mochi bomb. Less likely to detonate when impacted, but is no less powerful.                      | As an explosive. Generally more practical than MI due to its stability.                                                           |                                                                                                                               |
| PAY    | Incendiary Paint | Sticks to surfaces and burns rapidly when heated.                                                            | To accelerate burning of [fuel](/fuel.md "fuel") or melting of [string](/string.md "string") or [elastic](/elastic.md "elastic"). |                                                                                                                               |
| FI     |                  | Creates massive amounts of liquid [fuel](/fuel.md "fuel") when impacted.                                     | As an explosive. Particularly useful for burning, and can last for a long time.                                                   | For bombs using FI as a payload, it's much more powerful when compressed by a smaller explosion. An RIP casing achieves this. |
| EFI    |                  | A more stable version of FI. Less likely to detonate until set on fire.                                      | As an explosive. Does not sacrifice any power for stability and is very effective.                                                | Effectively becomes FI when ignited.                                                                                          |

  
===Propulsion===

| Recipe | Name                 | Properties                                                                                         | Uses                                                                    | Notes                                                                |
|--------|----------------------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|----------------------------------------------------------------------|
| JR     | [Jet](/Jet.md "Jet") | Pushes particles attached to itself.                                                               | Primarily for propulsion. Can be used as a piercing projectile.         | This is the material you get when you select "Jet" in the game's UI. |
| PIE    |                      | Creates a stream of [powder](/powder.md "powder").                                                 | Powerful thruster when the exhaust is directed into a single direction. |                                                                      |
| RIG    |                      | Creates a stream of [gas](/gas.md "gas").                                                          | Weak but stable and constant thruster.                                  |                                                                      |
| MIPG   |                      | Explodes when ignited, creating a high pressure explosion. Unaffected by gravity and quite stable. | As a propellant for a projectile.                                       |                                                                      |

  

### Projectiles

| Recipe | Name | Properties                                                                            | Uses                                        | Notes                               |
|--------|------|---------------------------------------------------------------------------------------|---------------------------------------------|-------------------------------------|
| RHJ    |      | Much more forceful than normal [Rigid](/Rigid.md "Rigid"). Can melt and burn targets. | For penetrating most weaker targets easily. | Harder to propel than normal Rigid. |
| RV     |      | For some reason, slightly more forceful than [Rigid](/Rigid.md "Rigid").              | As a simple projectile.                     |                                     |

  
===Utilities===

| Recipe | Name | Properties                                                        | Uses                                                                                                              | Notes |
|--------|------|-------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-------|
| XOR    |      | Rotates around a fixed point and deletes particles that touch it. | To cut perfect [circles](/Circles%20%28Crafting%29.md "Circles (Crafting)") in bodies of [Wall](/Wall.md "Wall"). |       |

  
==="Modified" materials===
Recipes that act similar to one of their ingredients, primarily improved in some way.

| Recipe | Name                                                                              | Properties                                                                                                                      | Uses                                                                                                                        | Notes                                                        |
|--------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| EVM    | Dampened Elastic                                                                  | An improved [Elastic](/Elastic.md "Elastic") material that can't be intersected as easily. Is also a bit more dampened.         | Most common cases where Elastic is used.                                                                                    |                                                              |
| WJ     | Stronger Wall                                                                     | Capable of holding fluids of much higher pressure than [Wall](/Wall.md "Wall").                                                 | Hydraulic machines that require high fluid pressures.                                                                       |                                                              |
| JH     | [Gubraithian Fire](/Gubraithian%20Fire.md "Gubraithian Fire") or Everlasting Fire | Acts like [fire](/fire.md "fire") or liquid [heater](/heater.md "heater"), but creates a fire effect and never stops burning.   | To create the fire effect without the material slowly burning away.                                                         |                                                              |
| LD     | [LightDense](/LightDense.md "LightDense")                                         | Does nothing with default parameters, but changing the densities of Light and Dense causes it to lie somewhere between the two. | A 4th density between Light and Dense other than Water.                                                                     |                                                              |
| CH     | [Cool Heat or IcyHot](/Cool%20Heat.md "Cool Heat")                                | Has properties of [Heater](/Heater.md "Heater"), except for not boiling [water](/water.md "water").                             | In any case where something needs to be melted/ignited without boiling water, for example a trigger for an underwater bomb. | In most cases needs to be combined with R or W to be useful. |

  
===Lasers===
See [Laser Recipes](/Laser.md#Laser-Recipes "Laser") for more laser recipes.

| Recipe | Name | Properties                  | Uses                                                                           | Notes                                                                  |
|--------|------|-----------------------------|--------------------------------------------------------------------------------|------------------------------------------------------------------------|
| UHI    |      | Melting laser.              | See [laser](/laser.md "laser"). Pressing left or right will explode the laser. | "SUSHI" can be used as a mnemonic for the recipe - the S's cancel out. |
| DIY    |      | High-power exploding laser. | See [laser](/laser.md "laser").                                                |                                                                        |

  

### Spectacle

If a recipe results in something that looks particularly cool but doesn't have many practical uses, it can be placed here.

| Recipe | Name            | Properties                                                                                          | Uses | Notes                                                                                                    |
|--------|-----------------|-----------------------------------------------------------------------------------------------------|------|----------------------------------------------------------------------------------------------------------|
| EF     |                 | Soft material that melts as it burns.                                                               |      | T, V, M, or Y could be added to give the material the appearance of burning wax or plastic when ignited. |
| FREI   | Condensed Flare | When lit on [fire](/Burning.md "Burning"), melts to a big amount of active [Fuel](/Fuel.md "Fuel"). |      | if FREI doesn't work as intended, which is acts [elastic](/Elastic.md "Elastic"), try FEI.               |
| SPY    | Tin Foil        | Forms orthogonal shapes, crinkles                                                                   |      | Surprisingly stiff, deformable material. Combining with Brittle resembles something like sheet metal.    |

  

### Unsorted

All unsorted recipes will be placed here until they can be moved to another category.

<table>
<thead>
<tr class="header">
<th><p>Recipe</p></th>
<th><p>Name</p></th>
<th><p>Properties</p></th>
<th><p>Uses</p></th>
<th><p>Notes</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>WD</p></td>
<td></td>
<td><p>Anything that clips into the wall will be moved upwards.</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>WL</p></td>
<td></td>
<td><p>Anything that clips into the wall will be moved downwards.</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>WY</p></td>
<td></td>
<td><p>Wall that visibly scorches when heated.</p></td>
<td><p>To test penetrating power of heat-based weapons/explosives, or for aesthetic purposes.</p></td>
<td><p>Setting the <a href="/color.md" title="color">color</a> to black will make the scorch marks darker.</p></td>
</tr>
<tr class="even">
<td><p>IO</p></td>
<td></td>
<td><p>Liquid that creates large amounts of liquid outflow.</p></td>
<td><p>Destruction. Potentially an obstacle in a <a href="/Levels.md" title="Levels">level</a>. Can be used as a <a href="/Laser.md" title="Laser">laser.</a></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>AY</p></td>
<td><p>Paint</p></td>
<td><p>Fluid that sticks to other objects, but not itself.</p></td>
<td></td>
<td><p>NY does not have the same properties and acts like normal Yuki.</p></td>
</tr>
<tr class="even">
<td><p>EM/SM</p></td>
<td><p>Tape</p></td>
<td><p>Flexible material that adheres to surfaces.</p></td>
<td><p>For attaching two objects weakly. Has some advantages over default mochi, such as being less "messy".</p></td>
<td><p>Since it sticks to an objects surface, it is useful for creating layers. Also since Elastic adds stiffness, it helps create a smooth curve.</p></td>
</tr>
<tr class="odd">
<td><p>QFC</p></td>
<td></td>
<td><p>Decays extremely slowly when heated.</p></td>
<td></td>
<td><p>In most cases needs to be combined with R or W to be useful.</p>
<p>The decay is extremely slow, and it may take several seconds for even one particle to disappear.</p>
<p>The decay rate can be adjusted with the <em>fuelLightProbability</em> and <em>fuelExtinguishProbability</em> parameters.</p></td>
</tr>
<tr class="even">
<td><p>PEB</p></td>
<td></td>
<td><p>Shatters into several small bits when touched even gently.</p></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p>BESTP</p></td>
<td></td>
<td><p>A more stable PEB, which can explode on its own but can last longer.</p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>RCQ</p></td>
<td></td>
<td><p>Rigid material that extinguishes fire. Cannot evaporate.</p></td>
<td><p>To keep a fuel source in a <a href="/rocket.md" title="rocket">rocket</a> or combustion engine from igniting.</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>PY</p></td>
<td></td>
<td><p>When <em>standardDistance</em> is reduced to around 0.5, it starts moving on its own in strange ways.</p></td>
<td></td>
<td><p>See <a href="/Powder-Snow%20Reaction.md" title="Powder-Snow Reaction">Powder-Snow Reaction</a>.</p></td>
</tr>
<tr class="even">
<td><p>EVP</p></td>
<td><p>Space foam</p></td>
<td><p>Low density foam-like material. Hardly affected by gravity and difficult to penetrate. Extremely flammable.</p></td>
<td><p>As armor against non-heated piercing projectiles or to dampen the speed of fast-moving object.</p></td>
<td></td>
</tr>
</tbody>
</table>

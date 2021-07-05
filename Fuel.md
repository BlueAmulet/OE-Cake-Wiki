![Fuel. A fire hazard seen in levels, and a house made of fuel being burned down.](/images/Fuel.jpg "Fuel. A fire hazard seen in levels, and a house made of fuel being burned down.")
**Fuel** is the burny stuff you see in a lot of OE-Cake videos. It burns. It's a solid material that catches on fire when exposed to Hot. Fuel can be added to any material to make it burn. As Fuel burns, it disintegrates as particles disappear. Fuel is responsible for the [Fire](/Fire%20%28shader%29.md "Fire (shader)") animation in Shader and Blob mode.

### Uses

Fuel is often used to make [Levels](/Levels.md "Levels") harder, by mixing it with the [User](/User.md "User") element. You can pour or inflow liquid Fuel, or create it by pressing *esc + F + esc*. The [Fire](/Fire.md "Fire") material is simply liquid Fuel + Hot. Although you cannot Inflow the Fire material, you can fake it by inflowing Fuel from something and immediately setting it on fire.

Fuel + Water is difficult to burn because it puts itself out. However Fuel and Water, with certain [Parameters](/Parameters.md "Parameters"), create the [Conductive Material](/Electrical%20Conduction.md "Electrical Conduction") for simulating electricity. Fuel + Cold makes [IcyHot](/Cool%20Heat.md "Cool Heat"), a flammable material that does not evaporate water.

Fuel [burns](/Burning.md "Burning") in an unusual way. Burning does not destroy all of the [links](/Linking%20particles.md "Linking particles") between particles, causing a crumbling structure to have "floating bits" as sections form groups while it collapses. Save-file analysis has revealed that this is caused by an internal limitation of OE-Cake - when Rigid burns, it separates into smaller Rigid groups. The game stores the number of Rigid groups as a single byte - creating a maximum of 256 allowable groups of Rigid. Extremely large burning structures easily surpass this, complicating the ability for Fire and Rigid to play together.

[Category:Materials](/Category_Materials.md "Category:Materials")

The **Extraneous Nulls** (or **Outer Nulls**) are 6 materials that can only be accessed through [save file editing](/.oec%20File.md ".oec File"). They exist due to the fact that [materials](/Material.md "Material") are stored as 32-bit integers, but only 26 of the bits are actually used. The extraneous nulls are just the leftover 6 materials.

The Extraneous [Nulls](/Null.md "Null") can facilitate [advanced simulations](/Advanced%20Simulations.md "Advanced Simulations").

## Types

There are exactly 6 extraneous nulls, which are named null alpha, null beta, null gamma, null delta, null epsilon, and null zeta.

The extraneous nulls can be used in recipes, and combined with normal materials. In recipes, they should be written using the lowercase forms of the corresponding Greek letters. For example, [Elastic](/Elastic.md "Elastic") + [Inflow](/Inflow%20%28Element%29.md "Inflow (Element)") + Null Alpha + Null Epsilon would be abbreviated EIαε.

Because extraneous nulls have no impact on the physics of a given material, [recipe](/Recipes.md "Recipes") names containing extraneous nulls should be formatted like *EI αε* or *EI(αε)*, for clarity.

## Obtaining

Extraneous nulls and recipes containing extraneous nulls can only be obtained via save file editing. See [.oec File](/.oec%20File.md ".oec File") for a method on how to create extraneous nulls.

However, there are ways to create large amounts of extraneous nulls.

The first method is [Robert's Comb](/Spin-Charged%20Elastic.md "Spin-Charged Elastic"). You can use find-and-replace or regex replace to replace large amounts of some material with extraneous nulls.

The second method is [Spuit](/Spuit.md "Spuit"). If you create even one particle of extraneous null, you can use the spuit tool to create arbitrary amounts of it.

## Properties

On their own, extraneous nulls have absolutely no effect on the behavior of particles. They behave in the same manner as normal Null.
![A block of R(β) resting on a block of OW(β) without being absorbed.](/images/Extraneous%20null.png "fig:A block of R(β) resting on a block of OW(β) without being absorbed.")

### Outflow Filtering

[Inflow](/Inflow%20%28Element%29.md "Inflow (Element)") and [Outflow](/Outflow%20%28Element%29.md "Outflow (Element)") are notable exceptions. The way Outflow works is that it absorbs any particle that shares no ingredients with it. Luckily, this includes extraneous nulls. This means you can create Outflow that arbitrarily cannot eat some material.

### Immutability

Because extraneous nulls have no properties whatsoever on their own, they are effectively immutable. They behave as a liquid, but cannot burn, evaporate, or trigger Snow to melt. Instead, they are useful as permanent tags attached to a particle, which can only be read by Outflow and have no other effects on the behavior of the particle.

#### Inflow Immutability

[Inflow](/Inflow%20%28Element%29.md "Inflow (Element)") containing extraneous nulls will pass the extraneous nulls to the particles they create, allowing multiple forms of materials to co-exist in an environment made with different forms of Null Outflow.

## Uses

Extraneous nulls have only recently been discovered, so the uses of them have not been explored.

It is theorized that the selective absorption and creation properties of these extra Nulls may be used to create cellular automata or chemical computers with up to 6 significant bits.

It is possible to create cell-like structures in various ways. By making a slightly pressurized atmosphere of Gas, blob-like shapes emerge from most materials. Naturally Tensile forms stable blobs due to it's oil-like behaviour. But if Jet is added to the Gas atmosphere or the cells, and set to an appropriately low value, more behaviour emerges. Elemental properties allow many behaviours to occur as well as promoting more complex interactions over time.

By having the edge of the screen made of IWG(J?) originating from different Nulls and the cells made of appropriate materials with their own Nulls, chemical signaling may allow these blobs to selectively absorb or repel certain elements, changing their internal state. Such a creation has not yet been made or shown to be effective.

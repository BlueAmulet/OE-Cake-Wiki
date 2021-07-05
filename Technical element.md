A **technical element** is an element hidden from the player that serves some technical purpose. All technical elements are [auxiliary elements](/Auxiliary%20Element.md "Auxiliary Element").

There are two technical elements: [A-Null](/A-Null.md "A-Null") and [N-Null](/N-Null.md "N-Null").

## A-Null

[A-Null](/A-Null.md "A-Null") is used by [Water](/Water.md "Water") and [Snow](/Snow.md "Snow") to create a "surface" effect. In water, this is a purely visual effect, but in snow, the surface material has different physics.

A-Null has the effect of making particles look lighter, which is why the surface water effect is visible. As snow shares the same "brightening" property, it's invisible with snow.

Water does not have any different physical properties when containing A-Null, but snow + A-Null does not stick to itself and only sticks to other materials. This causes the standard snow (QY) to behave differently at its surface, and is why AY has a paint-like behavior.

## N-Null

[N-Null](/N-Null.md "N-Null") is used by [Elastic](/Elastic.md "Elastic") and [String](/String.md "String") to form the [joints](/joints.md "joints") that hold these materials together and by [Wall](/Wall.md "Wall") and [Rigid](/Rigid.md "Rigid") to bind themselves to the elastic materials.

N-Null only exists for a single physics step. After it is created, it will create joints where possible, and then delete itself from the material.

It is not possible to draw Elastic, String, Wall, or Rigid without N-Null. It is added to the particles automatically, regardless of the recipe you're trying to draw. If N-Null is removed from the recipe through save file editing before the joints are formed, the material will not form any joints.

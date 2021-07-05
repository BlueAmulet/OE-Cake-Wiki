**N-Null** is a material responsible for the formation of [elastic joints](/Joints.md "Joints") between particles when they are first placed. N-Null is a [null](/null.md "null") element and an [auxiliary element](/Auxiliary%20Element.md "Auxiliary Element").

## Description

N-Null exists to create the bonds between Elastic, String, and other materials when they are first placed into the simulation. N-Null is automatically added to any recipe containing the elements [Wall](/Wall.md "Wall"), [Rigid](/Rigid.md "Rigid"), [Elastic](/Elastic.md "Elastic") or [String](/String.md "String") when drawn in (meaning they cannot be drawn without N-Null), and in the next physics step, the N-Null creates the bonds between the particles and removes itself from the recipe.

[Rice](/Rice.md "Rice")'s ability to create joints in real time is a result of Rice adding N-Null to its recipe every step. As a result, it reforms bonds constantly.

N-Null has not been observed to have any effect on materials other than the solids. As a pure element, N-Null converts itself to [True Null](/True%20Null.md "True Null").

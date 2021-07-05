![Powder in its normal state, and then at the point of ignition.](/images/Powder.jpg "Powder in its normal state, and then at the point of ignition.")
**Powder** is an explosive, powdery substance. It explodes violently when contacted by Hot. Powder is easily the most versatile and complicated material in the game, with no fewer than 9 separate [Parameters](/Parameters.md "Parameters") having an effect on it's behaviour. Carefully tuning these parameters allows you to create things like sand, dirt, mud, clay, salt, icing sugar, and whatever other fine-grained substance you can imagine, as well as giving very fine control over how Powder explodes.

### Uses

The default Powder settings create an explosion that is very violent but short-lived, making it good at cutting holes in things but not very good at pushing things like a cannon ball. Setting *powderExplosionCoefficient* and *powderExtinguishProbability* to lower numbers will make Powder last longer, push farther, and is less likely to "blast through" the walls containing it. Setting *powderExtinguishCoefficient* to 0 makes an angry swarm of bees. The explosive power of Powder is also strongly affected by *maxSpeed* and *standardDistance*.

Powder combined with [Elastic](/Elastic.md "Elastic") or Brittle + Elastic creates a strange material. It sits still until touched, then it will begin vibrating rapidly and can even tear itself apart. This is caused by an interaction with the *standardDistance*parameter, and is responsible for the [Powder-Snow Reaction](/Powder-Snow%20Reaction.md "Powder-Snow Reaction").

Adding Jet or Fuel to Powder allows you to see [Fire](/Fire%20%28shader%29.md "Fire (shader)") in the explosion, increasing its visual value.

With *powderExplosionCoefficient* set to 0 and with some tuning of *powderLightProbability* and *powderExtinguishProbability*, you can perfectly re-create Fuel but without the Fire animation.

Powder with *powderExplosionCoefficient* set to a low number and *powderExtinguishProbability* set to 0 creates a strange fluid that resembles plasma. It could also represent atoms vibrating, and *powderExplosionCoefficient* would roughly approximate temperature.

Powder's physical density is directly controlled by *standardDistance* and *powderSpringCoefficient*. Changing the density of the powder strongly changes it's explosive and bulk characteristics, such as whether it floats or sinks in Water and how it tumbles down a hill.

With some tuning, Powder can have many different behaviors.

[Category:Materials](/Category_Materials.md "Category:Materials")

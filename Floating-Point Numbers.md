[OE-Cake](/OE-Cake.md "OE-Cake") uses a number format called ["32-bit floating-point"](https://en.wikipedia.org/wiki/Single-precision_floating-point_format) to store the positions, velocities, and other properties of particles. In this article, the nature of floating point numbers and the implications this has on the physics of the game will be explained.

## What are floating-point numbers?

A floating-point number, or "float" for short, is a way numbers can be stored on a computer. Floating point numbers can have fractional values, and because computers have limited amounts of memory, they only have so much precision.

Floats will lose precision as they increase, and generally have 7 to 8 digits of accuracy before losing precision by default. However, there are different types of floats with different amounts of precision.

### What happens if a floating point number gets too big?

In integers (whole number values like 1, 2, 3...), an overflow happens when the integer value exceeds a maximum (like 65535) and wraps back down to 0. However, this does not happen for floats. Instead, floating-point overflows typically cause the value to jump to infinity or NaN (Not a Number). For an example of how this can affect [OE-Cake](/OE-Cake.md "OE-Cake"), see [Infinite Velocity Bug](/Infinite%20Velocity%20Bug.md "Infinite Velocity Bug").

![A typical level.](/images/User.jpg "fig:A typical level.")
The **User** element is an element that is controlled by the keyboard using the arrow keys. It is usually the centerpiece used in [Levels](/Levels.md "Levels") and is often mixed with other elements. The default material is User+Rigid.

### Uses

When [Gravity](/Gravity.md "Gravity") is enabled, User will "jump" with extra force whenever it is pressing "down" on a "floor" for it to jump off. The amount User jumps is changed with *usersMaxCharge* in the [Parameters](/Parameters.md "Parameters"), you can even turn it off. This works OK when you only have one piece of Users in the level, and no atmosphere. If you have another piece of User somewhere, either of them can trigger the "jump" reaction, and it's possible to break the jump function with some User that is always touching "down" on something. When User is surrounded by Gas or Water or another fluid, the "jump" function breaks and the User will rocket to the sky.

Though more difficult, User will still "jump" even when mixed with Gas, if it has a platform "below" it to push off. With Gas or without gravity, User can move freely in all four directions. User's speed and strength along the vertical and horizontal directions can be changed in the Parameters.

By modifying the *usersSpeedX/usersSpeedY* and *usersForceX/usersForceY* Parameters you can also create liquid or gaseous User that is always trying to move in a certain direction with a certain amount of force, which creates very interesting fluids. You can make Water that is extra "heavy" or "light" by having a tiny force pushing it up or down, affecting equilibrium. You can make a liquid that "falls up" with enough force, or Gas that is always blowing to one side. This effect will continue until you press a keyboard arrow key, and the *users* Parameter for that axis will be overridden by the keyboard and then return to zero when released.

![User jumping through an wall.
(Animated Gif)](/images/User%20Skipping%20Wall.gif "fig:User jumping through an wall. (Animated Gif)")
User can be mixed with Wall or Axis, allowing you to move these otherwise immutable materials. For example, you could hook a character to a piece of Wall+User with some String, and have a User-controlled character that tries to follow the Wall cursor as it moves. Setting the *usersSpeed* value pretty low allows you to very finely position pieces of User+Wall, which is extremely useful in attempting repairs on advanced creations or positioning parts with single-pixel accuracy.

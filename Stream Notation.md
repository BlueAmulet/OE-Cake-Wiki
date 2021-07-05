Stream Notation is a notation that can be used to write the behaviour of Streams created by [Inflow](/Inflow%20%28Element%29.md "Inflow (Element)").

## Base Components.

Stream Notation in it's basis is two components. The **Sides**, and the **Corners**. These two are the two main components of Stream Notation. Sides are contained in {curly brackets}, and Corners are contained in \[Square Brackets\]. Each side and Each corner is divided by commas ",". Each stream is separated by a space.

So in essence, all Inflow streams can be written with { , , , }\[ , , , \], althout the amount of commas can change.

## Stream Types

### Regular Streams

![Serial Stream.\|alt=](/images/Stream%20R%20serial2.png "fig:Serial Stream.|alt=")
Regular Streams are Streams which are well... regular. They repeat. In general they are shown with the letter R. So if you're not sure what exact kind of stream you're seeing, or even if you can't tell apart the individual streams but can tell it's regular on a whole side, then you can type R for the whole side. {r r r p3 r p4... can become {R... if you can't tell.

#### <big>Serial Streams</big>

Serial Streams are the most ordered of the Streams, and they're the most common. They're a continuous, unbroken chain of particles. They are shown with the symbol "r".

<big>Periodic Streams</big>![Periodc Stream with period 2. (p2 or p(10).)\|alt=](/images/Stream%20R%20periodic.png "fig:Periodc Stream with period 2. (p2 or p(10).)|alt=")Periodic Streams are another common Regular Stream. They're continuous like Serial Streams, but their particles only appear at some division of the serial frequency.

You can show periodic streams in two ways: Period Length and Period Order.

Period Order is the base of the two, but Period Length is used more commonly. Periodic Streams always begin with "p".

Period order shows the particles appearence order. The order is shown in (regular parentheses. If there's a 0, no particle, if there's a 1, there is a particle. For example, p(01001) would mean it removes the first, third and fourth particles in a serial stream, repeating every 5 particles.

Period Length is easier to use, and covers most cases. It's shown without parentheses and some number. It's easy to see if we compare it to Period Order.

If we don't know the period, or it's too hard to count, but we are sure it's periodic, we can use p without anything else.

-   p1 = p(1)
-   p2 = p(10)
-   p3 = p(100)
-   p4 = p(1000)
-   and so on.

  
<big>Diverging Serial Streams</big>![DS Stream with period 3. Notice how it's the separate but really close angles before repeating. This one would be written as r3.\|alt=](/images/Stream%20R%20divergingserial.png "fig:DS Stream with period 3. Notice how it's the separate but really close angles before repeating. This one would be written as r3.|alt=")Diverging Serial Streams are a special kind of Serial Stream that are periodic, but are Serial in their creation. They usually happen when Serial Streams are disturbed in some way. They come from the same inflow source.

Diverging Serial Streams are shown with "r", like Serial Streams, but have a number in front to show the disturbance period. Basically, this is the period at which the small variations repeat. If there is no repetition, and it simply varies randomly or we can't tell the disturbance period, we write r^ (r with a carat).

### Irregular Streams

Irregular Streams are Streams which don't repeat, but ***don't have to be chaotic.*** As we'll see later, there's Irregular Streams that aren't chaotic. But each stream doesn't really have an order, or if they do, it's really complicated. The same logic as Regular Streams, a side with unknown type but known class can be written as "C", you cannot write individual streams, because Irregular Streams don't have individual streams.

#### <big>Pattern Streams</big>

![Pattern Stream. Notice how it's too complicated to type out using Regular Stream notation, but it's still not chaotic.\|alt=](/images/Stream%20C%20pattern.png "fig:Pattern Stream. Notice how it's too complicated to type out using Regular Stream notation, but it's still not chaotic.|alt=")Pattern Streams are Streams which aren't Regular, but have a pattern. Although they're technically Regular, there's too many streams and too complicated of a Period Order to type out, and you don't need to. Be careful for big scale patters, those are Pattern streams too.

Pattern Stream can blur the lines between Regular and Irregular, but most of the time they're chaotic enough to not be able to be written as individual sides. But in technicality, all Pattern Streams are just a combination of Regular Streams, and all Combinations or even single streams are Pattern streams.

Pattern Streams are shown with the symbol "t". They apply to a whole side.

#### <big>Random Streams</big>

![Random Stream. Notice the particles touching, and how that disrupts the streams.\|alt=](/images/Stream%20C%20random.png "fig:Random Stream. Notice the particles touching, and how that disrupts the streams.|alt=")Random Streams are streams which are completely random. Since there's particle interaction (particles touch eachother), It's impossible to write whereas Pattern Streams were only ludicrously hard to write.

Random Streams are shown with x. They apply to a whole side.

## Syntax

Syntax is simple enough to understand. With examples, it will become more clear.

Here's the main steps.

-   Start from the top side. Begin from the lefternmost stream.
    -   If there's no top side, begin from the side that leans most to the top. If there's nothing like that either (so two equally angled sides), begin from the side facing the right.
-   Continue stream by stream or side by side, going clockwise.
-   When you're done, start the corners. Start from the Northeast corner.
-   Continue Clockwise.

### Structure

Here's the main rules of Stream Notation.

-   All of the sides of the inflow are written in {Curly Brackets}.
-   All of the corners of the inflow are written in \[Square Brackets\].
    -   For both, only at the beginning of the first side/corner and at the end of the last side/corner.
    -   If there's no corners, don't add the corner component, and start from the topmost stream that's also on the right side and go clockwise.
    -   If streams of the same type are repeating (for example {p2 p2 p2 p2}) can be simplified by using asterisks, showing how many times that particular type repeats. so {p2 p2 p2 p2} would become {p2\*4}.
    -   If all streams are the same, there's no need for any commas, write the type all streams are as it is, like {p2}\[r\] for example.
    -   If a side has no streams, we write an underscore "\_" instead.
-   Each side is divided by a comma ",".
-   Each corner is also divided by a comma ",".
-   Each stream is divided by a single space.
-   If the stream is irregular, add it to the whole side, since there will be no other streams on that side.
-   If you don't know the exact type of the stream, write it's class (R for regular, C for Irregular). If you don't know the class either, write "O".
    -   If you only know some parts of it, then type those only, but put the unknown part in parentheses.
-   If a stream has transitioned from one type to another, use > and type the first type on the left, and the second type on the right, if it's been changed 3 times or more, add a > for every change. (for example r touches r^ and becomes r^ on it's own, it is written r>r^)

## Syntax Examples

### Example One

<figure>
<img src="/images/Example%20rectangle1.png" width="300" />
</figure>

Take this Inflow rectangle. First, let's look at the emission. As you can see, it's all lines and because of this, it's all Regular. Now let's mark which ones are corners, and which ones are sides.
<img src="/images/Example%20rectangle2.png" title="fig:" width="300" />This is good, and will tell us which component to add to. Now we will try to identify the types. In here, we have serial streams, which appear as the denser streams, and then we have periodic streams, which appear as the weaker streams. Now these look like they appear with half the frequency. Since these aren't very complicated, we'll use the Period Length version.

So that means we have r and p2.
<img src="/images/Example%20rectange3.png" title="fig:" width="300" />Now that we have all of this information, we can begin constructing the notation itself.

1.  Let's begin from the Top side, and the lefternmost stream. Which is p2. Now we have {p2 so far, not very impressive but eh.
2.  Next let's continue the side, it's all p2 so we can write {p2 p2 p2 p2 . Now we had a rule where if there was multiple repeating streams of the same kind, we could add an asterisk. So let's do that to get {p2\*4 .
3.  Next let's do all the sides. Being careful to not include the corners.
    1.  The right side has r, p2 and r again, so we add the next side with a comma. We get {p2\*4, r p2 r .
    2.  Next we add the bottom side, the bottom side also has 4 p2's so we add p2\*4. We get {p2\*4, r p2 r, p2\*4 .
    3.  Finally, we add the left side. It's the same as the right side so we ad r p2 r again. We get {p2.4, r p2 r, p2\*4, r p2 r}
4.  Now it's time for the corners. Notice how all the corners have the same type of Stream? Well we had a rule saying that we didn't need to write the type 4 times. So we can simply write {p2\*4, r p2 r, p2\*4, r p2 r}\[r\]. And we're done.
    1.  we could write \[r,r,r,r\] too but why would you?

### Example Two

<img src="/images/Example%202rectangle1.png" title="fig:Example_2rectangle1.png" width="400" alt="Example_2rectangle1.png" />
Yikes, this one's pretty hard. Let's give it a go though. First let's mark the corners and sides again.
<img src="/images/Example%202rectangle2.png" title="fig:Example_2rectangle2.png" width="400" alt="Example_2rectangle2.png" />
There we go, now let's try our best to identify the streams. Don't worry, we don't have to get everything.
<img src="/images/Example%202rectangle3.png" title="fig:Example_2rectangle3.png" width="400" alt="Example_2rectangle3.png" />

Now let's begin the notation process.

1.  Let's start from the top again. We don't know what they are, they're pretty complicated. But they are regular. So we can just say R for the whole side. We now have {R .
2.  Let's now do the right side. It's clear that this is another pattern. We called patterns t, so we add t. We now have {R, t .
3.  The bottom is the same as the top. Now we have {R, t ,R .
4.  Now the left side. It's the same as the right site, it's a pattern. So we'll add a "t" to complete the sides. We now have {R, t, R, t} and have completed the sides.
5.  Now for the corners. They're all serial, so they get "r". And since all corners are "r", we can write a single r to represent that. we now have {R, t, R, t}\[r\].
    1.  Now the corners look like a pattern maybe, but that's not actually because of the Stream, it's rather the "t" sides disturbing the corner.

But we can still identify some streams.
<img src="/images/Example%202rectangle4.png" title="fig:Example_2rectangle4.png" width="400" alt="Example_2rectangle4.png" />We have massive room for improvement.

1.  First, let's get the original into here: {R, t, R, t}\[r\].
2.  Now let's add the Streams we know, in order.
    1.  We have two p2's at the start and the end. So we can have {p2\*2 (R) p2\*2, t, p2\*2 (R) p2.2, t}\[r\]
    2.  There's four streams in the center. When we do this we can add R to the end, or add it in between the terms we know to show the terms location. The second option is strongly preffered to avoid confusion. We add the p2's in the other center. We get {p2\*2 (R) p2 (R) p2 (R) p2\*2, t, p2\*2 (R) p2 (R) p2 (R) p2\*2, t}\[r\].
    3.  Finally we can add the two p2's in the center. We get {p2\*2 (R) p2 (R) p2\*2 (R) p2 (R) p2\*2, t, p2\*2 (R) p2\*2 (R) p2 (R) p2 (R) p2\*2, t}\[r\].

### Example Three

<img src="/images/Example%20circle1.png" title="fig:Example_circle1.png" width="450" alt="Example_circle1.png" />This is a circles, so we won't have corners, so no need for the corner component. And since there's no corners, we also won't use commas.
<img src="/images/Example%20circle2.png" title="fig:Example_circle2.png" width="450" alt="Example_circle2.png" />Now, let's begin.

1.  As you've heard in syntax, we start from the topmost right-half stream. And then we go clockwise, that's it.
2.  So we'll go {r^ r3 p2\*4 r3\*2 p2\*4 r>r^\*2 r r3\*3 r}
    1.  I forgot to add the "r" at the end, but you get it :)

### Example Four

<img src="/images/Example%20pacman1.png" title="fig:Example_pacman1.png" width="450" alt="Example_pacman1.png" />Now this is the hardest of them all, it's not sideless or cornerless, it's not a rectangle, and it has a lot of interaction. Let's break it down. Let's begin with the corners and sides.
<img src="/images/Example%20pacman2.png" title="fig:Example_pacman2.png" width="450" alt="Example_pacman2.png" />There we go. This is much nicer. Now let's begin marking the Streams.
<img src="/images/Example%20pacman3.png" title="fig:" width="450" />

1.  First, let's find the side to start. Since there's no top face, we start from the one that leans most to the top. Which is the arc of the circle. So we begin from there. We get {r^ r3 p2\*4 r3\*2 p2\*4 r\<r^\*2 r r3 .
2.  Next, we deal with the other side. Since the second side is blank we add an underscore to show it's blank. So we get {r^ r3 p2\*4 r3\*2 p2\*4 r\<r^\*2 r r3, \_ .
3.  And then with the third side. It has one random spray, so it's a random spray, we add x. We get {r^ r3 p2\*4 r3\*2 p2\*4 r\<r^\*2 r r3, \_, x}
4.  Then we add the corners, since corners are diffrent, we can't just type in one letter. We get {r^ r3 p2\*4 r3\*2 p2\*4 r\<r^\*2 r r3, \_, x}\[r,r>x,r>x\].
    1.  Now you might be wondering, why not r>x on the first corner? Well, while on the other two the change is unavoidable, all particles get disturbed in some way, but on the first corner, it's avoidable, most particles aren't actually disturbed.

## Observations

`This is the observations section, if you have an observation that's unique, you can add it here.`

-   The most common DSS is r3.
-   The most common Period Stream is p2
-   p2 usually appears in groups
-   one of the most common corner streams is \[r,r,r,r\] or \[r\].
-   it is possible to have an inflow without r
-   a lot of streams can change their notation when disturbed, it usually becomes more complex.
-   some shapes start out chaotic, but end stable.
-   inflow made with pencil will have streams at the bending points
    -   consider these corners.
-   a line of inflow will only have "r" on it's two corners.
-   a single dot of inflow will not create anything until disturbed with another particle.
-   all non-wall inflow is random

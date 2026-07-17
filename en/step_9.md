## Challenge: stack them up

Your game works! Right now, though, different fruit fall straight through each other. If you want them to pile up in a satisfying heap, you can make each fruit rest on top of fruit that isn't its match.

--- task ---

![the fruit sprite.](images/fruit.png)

In the `Fruit` sprite:

For each costume, add a check: if the clone is touching **either of the other two colours**, nudge it back up so it stacks instead of overlapping. It's the same trick you used for the floor — fall a little, then push back up.

Add this inside your `if (costume number) = (1)`{:class="block3control"} block, below the pop check:

```blocks3
when I start as a clone
switch costume to (pick random (1) to (3))
go to x: (mouse x) y: (115)
start sound (Pop v)
show
forever
change y by (-4)
if <touching (Floor v)?> then
change y by (4.1)
end
if <(costume [number v]) = (1)> then
if <touching color (#4e9a06)?> then
change y by (-4.2)
wait (0.2) seconds
start sound (Lo Gliss Tabla v)
delete this clone
end
if <<touching color (#ec1c2c)?> or <touching color (#edd51c)?>> then
change y by (4.1)
end
end
end
```

--- /task ---

--- task ---

Now do the same for your other two costumes, changing the two colours each time to name the **other** fruit.

tip: Each `if (costume number) = ()`{:class="block3control"} block should end up mentioning all three colours: one that deletes the fruit, and two that make it stack.


--- /task ---

Click the green flag and fill the box. Different fruit now stack up into a pile, and matching fruit still pop.

![fruit of different types piling up in a stack.](images/stacking.gif)

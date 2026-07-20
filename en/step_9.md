## Challenge: stack them up

If you want the fruit to pile up in a heap, you can make each fruit rest on top of fruit that isn't its match.

--- task ---

![the fruit sprite.](images/fruit.png)

For the first fruit costume, add an `if` to see if the fruit is `touching` **either of the other two colours**. Then `change the y` so it stacks in the same way as with the floor. 

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
wait (0.2) seconds
start sound (Lo Gliss Tabla v)
delete this clone
end
+if <<touching color (#ec1c2c)?> or <touching color (#edd51c)?>> then
change y by (4.1)
end
end
end
```

--- /task ---

--- task ---

Now do the same for your other two costumes, changing the two colours each time to name the **other** fruit.

--- /task ---

Click the green flag to see if different fruit now stack up into a pile, and matching fruit still disappear.

![fruit of different types piling up in a stack.](images/stacking.gif)

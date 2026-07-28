## Challenge: stack them up

In this step you can make the fruit stack up if it doesn't match.


--- task ---

![the fruit sprite.](images/fruit.png){:width="150"}

For the first fruit costume, add an `if`{:class="block3control"} to see if the fruit is `touching color`{:class="block3sensing"} **either of the other two colours**. Then `change y`{:class="block3motion"} so it stacks in the same way as with the floor. 

```blocks3
if <(costume [number v]) = (1)> then
if <touching color (#4e9a06)?> then
change y by (-4.2)
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

Make sure you add a new one of the touching color blocks for each extra fruit.

--- /task ---

**Test:** click the green flag to see if different fruit now stack up into a pile, and matching fruit still disappear.

![fruit of different types piling up in a stack.](images/stacking.gif){:width="450"}

## Make every fruit disappear

In this step, you'll make every fruit disappear when it matches.

--- task ---

![the fruit sprite.](images/fruit.png){:width="150"}

Add another `if`{:class="block3control"} block and move the `if`{:class="block3control"} with `touching colour`{:class="block3sensing"} into it. 

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
+if < > then
if <touching color (#4e9a06)?> then
change y by (-4.2)
wait (0.2) seconds
start sound (Lo Gliss Tabla v)
delete this clone
end
end
end
```

--- /task ---

--- task ---

![the fruit sprite.](images/fruit.png){:width="150"}

Use an `equals`{:class="block3operators"} and drag in the `costume number`{:class="block3looks"}. This will check if the costume number is `1`. 

```blocks3
forever
change y by (-4)
if <touching (Floor v)?> then
change y by (4.1)
end
+if <(costume [number v]) = (1)> then
if <touching color (#4e9a06)?> then
change y by (-4.2)
wait (0.2) seconds
start sound (Lo Gliss Tabla v)
delete this clone
end
end
end
```

--- /task ---

--- task ---

Right-click and **duplicate** the block, so you can add this for all the fruits. The new blocks should be under the last one, and inside the `forever`{:class="block3control"}.

![duplicating the costume check for each fruit.](images/duplicate-if.gif){:width="450"}

--- /task ---

--- task ---

Change the `equals`{:class="block3operators"} to `2` and use the eyedropper for the colour of your **second** costume. You can also choose a different sound if you want.

```blocks3
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
end
+if <(costume [number v]) = (2)> then
if <touching color (#ec1c2c)?> then
change y by (-4.2)
wait (0.2) seconds
start sound (Chomp v)
delete this clone
end
end
end
```

--- /task ---

--- task ---

Then duplicate it once more for your **third** fruit. Add `equals`{:class="block3operators"} to `3`, and eyedrop for that colour.

```blocks3
+if <(costume [number v]) = (3)> then
if <touching color (#edd51c)?> then
change y by (-4.2)
wait (0.2) seconds
start sound (Squish Pop v)
delete this clone
end
end
```
--- /task ---


> [!TIP]
>
> It's easy to lose track of the blocks. Right-click and choose **Add Comment** to label each one with its fruit's name.

![adding comments to label each costume check.](images/adding-comments.gif){:width="450"}

Click the green flag to **test**. Each fruit should disappear when they touch another of the same colour. 

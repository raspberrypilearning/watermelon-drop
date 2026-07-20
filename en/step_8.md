## Make every fruit disappear

Your fruit only disappear when they touch the green one — none of the other colours do anything yet.

In this step, you'll make every fruit disappear with its own kind.

--- task ---

![the fruit sprite.](images/fruit.png)

In the fruit sprite wrap these blocks into an `if`{:class="block3control"} to check the costume number is `1`. 

```blocks3
+if <(costume [number v]) = (1)> then
if <touching color (#4e9a06)?> then
wait (0.2) seconds
start sound (Lo Gliss Tabla v)
delete this clone
end
end
```

![duplicating the costume check for each fruit.](images/duplicate-if.gif)

--- /task ---

--- task ---

Right-click and **duplicate** the block.

--- /task ---

--- task ---

Change the costume number to `2` and use the eyedropper for the colour of your **second** costume. You can also choose a different sound.

Then duplicate it once more for your third fruit.

```blocks3
+if <(costume [number v]) = (2)> then
if <touching color (#ec1c2c)?> then
wait (0.2) seconds
start sound (Chomp v)
delete this clone
end
end
+if <(costume [number v]) = (3)> then
if <touching color (#edd51c)?> then
wait (0.2) seconds
start sound (Squish Pop v)
delete this clone
end
end
```

--- /task ---

**Tip:** it's easy to lose track of the blocks. Right-click and choose **Add Comment** to label each one with its fruit's name.

![adding comments to label each costume check.](images/adding-comments.gif)

Click the green flag to test. Now each fruit disappears when it touches another of the same colour. 

## Make the fruit disappear

Now for the interactive bit! 

In this step, use the `touching color`{:class="block3sensing"} to make fruit disappear if they touch each other.

--- task ---
 
![The fruit sprite.](images/fruit.png){:width="150"}

In the **paint editor**, change the outline of your **fruit sprite** to match the main fruit colour, or draw an outline in one colour all the way around the edge.

![Changing the colour of the fruit's outline so it is one solid colour.](images/solid-colour.gif){:width="450"}

--- /task ---

--- task ---

Add `if`{:class="block3control"} and `touching color`{:class="block3sensing"} inside the `forever`{:class="block3control"} loop.

```blocks3
when I start as a clone
go to x: (mouse x) y: (115)
start sound (Pop v)
show
forever
change y by (-4)
if <touching (Floor v)?> then
change y by (4.1)
end
+if <touching color ()?> then
end
end
```

--- /task ---

--- task ---

To get the exact colour, click the colour box in `touching color`{:class="block3sensing"} and choose the eyedropper to select from your fruit.

![Using the eyedropper to pick the fruit's colour for the touching-colour block.](images/eyedropper.gif){:width="450"}

--- /task ---


--- task ---

Add `change y`{:class="block3motion"} and `wait`{:class="block3control"} so that both the fruit move and wait a moment to detect the colours. 

```blocks3
forever
if <touching color (#4e9a06)?> then
+change y by (-4.2)
+wait (0.2) seconds
end
end
```

--- /task ---

--- task ---

Add a `start sound`{:class="block3sound"} block and choose a sound to go with your fruit. 

```blocks3
forever
if <touching color (#4e9a06)?> then
change y by (-4.2)
wait (0.2) seconds
+start sound (Lo Gliss Tabla v)
end
end
```

--- /task ---

--- task ---

Then make both clones disappear with `delete this clone`{:class="block3control"}.

```blocks3
forever
if <touching color (#4e9a06)?> then
change y by (-4.2)
wait (0.2) seconds
start sound (Lo Gliss Tabla v)
+delete this clone
end
end
```

--- /task ---

**Test:** Click the green flag and drop two fruit in the same place. When they touch, they should make a sound and disappear.

![Two watermelons touching and one disappearing.](images/pop.gif){:width="450"}


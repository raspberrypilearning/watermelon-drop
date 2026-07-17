## Pop by colour

Now for the heart of the game: when two of the same fruit touch, one of them should pop and disappear.

<!-- ============================================================
     AUTHOR TODO (Becca): REDO THE GIF IN THIS STEP.
     The blocks shown in the current gif are WRONG and will
     confuse learners — re-record it against the full script
     below before publishing.
     ============================================================ -->

--- task ---

![the fruit sprite.](images/fruit.png)

In the `Fruit` sprite:

First, make your fruit a single, solid colour so Scratch can spot when two are touching. In the paint editor, change the outline to match the middle — or draw a bold outline in one colour all the way around the edge.

![recolouring the fruit's outline so it is one solid colour.](images/solid-colour.gif)

--- /task ---

--- task ---

Inside the `forever`{:class="block3control"} loop of your clone script, add code so that when a clone is `touching color ()?`{:class="block3sensing"} — the colour of your fruit — it plays a sound and removes itself with `delete this clone`{:class="block3control"}.

> **Tip:** in game-making, this is called a **collision**. 

Click the colour box in the `touching color ()?`{:class="block3sensing"} block, choose the eyedropper, and click your fruit to pick its exact colour.

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
+if <touching color (#4e9a06)?> then
change y by (-4.2)
wait (0.2) seconds
start sound (Lo Gliss Tabla v)
delete this clone
end
end
```

![using the eyedropper to pick the fruit's colour for the touching-colour block.](images/eyedropper.gif)

--- /task ---

> The `wait (0.2) seconds`{:class="block3control"} matters: it only deletes **one** clone, so it gives the fruit already sitting there a moment to notice the collision too.

Click the green flag and drop two of the same fruit onto each other. When they touch, one pops and disappears.

![two watermelons touching and one popping.](images/pop.gif)

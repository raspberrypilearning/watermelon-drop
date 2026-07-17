## Clone the fruit

In this step, you'll make a copy — a **clone** — every time the player clicks.

--- task ---

![the fruit sprite.](images/fruit.png)

In the `Fruit` sprite:

Change your `when green flag clicked`{:class="block3events"} script. Instead of moving the fruit itself, `create clone of (myself v)`{:class="block3control"} while the mouse is held down, with a short `wait (0.1) seconds`{:class="block3control"} so you get separate fruit instead of hundreds at once.

Take the `go to x: () y: ()`{:class="block3motion"} block out of this script — the clone will use it next.

```blocks3
when green flag clicked
forever
if <mouse down?> then
create clone of (myself v)
wait (0.1) seconds
end
end
```

--- /task ---

--- task ---

Now tell each clone what to do when it appears. Add a `when I start as a clone`{:class="block3control"} script that sends the clone to the mouse pointer and plays a sound. Pick a `Pop` sound with `start sound ()`{:class="block3sound"}.

```blocks3
when I start as a clone
go to x: (mouse x) y: (115)
start sound (Pop v)
```

![a new fruit appearing each time you click.](images/clone.gif)

--- /task ---

Click the green flag, then click and hold. A new piece of fruit appears at the mouse pointer each time, with a pop.

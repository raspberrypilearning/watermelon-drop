## Clone the fruit

At the moment you only have one fruit. In this step, you'll make a **clone** — a copy — every time the player clicks, so you can drop lots of fruit.

--- task ---

Change your `when green flag clicked`{:class="block3events"} script. Instead of moving the fruit itself, make it `create clone of (myself v)`{:class="block3control"} each time the mouse is held down. Add a short `wait (0.1) seconds`{:class="block3control"} so you get separate fruit instead of hundreds at once.

Take the `go to x: () y: ()`{:class="block3motion"} block out of this script — the clone will use it in a moment.

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

Now tell each clone what to do when it appears. Add a `when I start as a clone`{:class="block3control"} script that sends the clone to the mouse pointer and plays a sound as it drops.

Add a `play sound () until done`{:class="block3sound"} — pick a `Pop` sound from the sound library.

```blocks3
when I start as a clone
go to x: (mouse x) y: (110)
play sound (Pop v)
```

--- /task ---

> Note: the pop sound belongs on every fruit from here on. Add it to your clones now so you don't forget it later.

Click the green flag, then click and hold. A new piece of fruit pops in at the mouse pointer each time.

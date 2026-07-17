## More challenges

You've made a complete fruit-dropping game. Here are some more ways to make it your own. Try any that appeal to you — each one is optional.

--- task ---

**Add a dropper.** Add a sprite at the top that follows the mouse pointer, so the player can see where the next fruit will land. The example game uses a cloud — but you could give yours eyes and a mouth to make it a character.

```blocks3
when green flag clicked
go to x: (-8) y: (159)
forever
set x to (mouse x)
end
```

![PLACEHOLDER PNG: the dropper sprite (a cloud with a face) at the top of the stage.](images/dropper.png)

--- /task ---

--- task ---

**Add a box or basket.** Draw a box or basket sprite for the fruit to fall into, and send it to the back so the fruit sit inside it.

```blocks3
when green flag clicked
go to x: (0) y: (0)
go to (back v) layer
```

--- /task ---

--- task ---

**Keep score.** Add a `score`{:class="block3variables"} variable, set it to `0`{:class="block3variables"} when the flag is clicked, and `change score by ()`{:class="block3variables"} just before each `delete this clone`{:class="block3control"}. Give different fruit different points!

```blocks3
change [score v] by (10)
delete this clone
```

--- /task ---

--- task ---

**Add a game over.** When a fruit ends up too high, the box has overflowed. In your clone's `forever`{:class="block3control"} loop, check its `y`{:class="block3motion"} position and `broadcast () and wait`{:class="block3events"} a `Game over` message.

```blocks3
if <(y position) > (111)> then
broadcast (Game over v) and wait
end
```

Then add a `Game over` sprite that hides at the start and shows when it gets the message:

```blocks3
when I receive (Game over v)
go to (front v) layer
show
play sound (Lose v) until done
stop (all v)
```

--- /task ---

--- task ---

**Add music.** Choose a backdrop for the stage, then loop a sound track so your game has a soundtrack.

```blocks3
when green flag clicked
forever
play sound (your track v) until done
end
```

--- /task ---

When you've finished, save your project. Well done — you've made your own Watermelon drop!

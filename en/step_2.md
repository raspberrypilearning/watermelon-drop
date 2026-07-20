## Add your first fruit

In this step, you'll add the first piece of fruit and make it follow the mouse pointer, ready to drop.

--- task ---

![the fruit sprite.](images/fruit.png)

Start a new Scratch project and delete the cat sprite.

Add a new sprite for your fruit — choose any fruit you like from the library, or an animal, or anything you want to see drop into the box. Use the paint tools to give it some character: a pair of eyes and a mouth. Resize it so a few could fit in a box.

![choosing a fruit sprite and drawing a face on it.](images/choose-fruit.gif)

--- /task ---

--- task ---

Add a `when green flag clicked`{:class="block3events"} block and a `go to x: () y: ()`{:class="block3motion"} block to place your fruit near the top of the stage.

```blocks3
when green flag clicked
go to x: (0) y: (115)
```

--- /task ---

--- task ---

Now make the fruit follow the mouse pointer. Wrap the `go to x: () y: ()`{:class="block3motion"} block in a `forever`{:class="block3control"} loop, and change its `x`{:class="block3motion"} to the `mouse x`{:class="block3sensing"} position.

```blocks3
when green flag clicked
+forever
go to x: (mouse x) y: (115)
end
```

--- /task ---

--- task ---

Finally, only move the fruit while the player is holding the mouse down. Put the `go to x: () y: ()`{:class="block3motion"} block inside an `if <mouse down?> then`{:class="block3control"} block.

```blocks3
when green flag clicked
forever
+if <mouse down?> then
go to x: (mouse x) y: (115)
end
end
```

![clicking to move the fruit along the top.](images/mouse-click.gif)

--- /task ---

Click the green flag, then click and hold near the top of the stage. Your fruit follows the mouse pointer left and right.

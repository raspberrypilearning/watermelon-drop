## Add your first fruit

In this step, you'll add the first piece of fruit and make it follow the mouse pointer, ready to drop.

--- task ---

[Start a new Scratch project](https://scratch.mit.edu/projects/editor/){:target="_blank"}.

--- /task ---

--- task ---

![the fruit sprite.](images/fruit.png)

Delete the cat sprite, then add a new sprite for your fruit — choose one from the library (or draw your own). It can be any fruit you like, an animal, or anything you want to see drop into the box. Use the paint tools to give it some character: a pair of eyes and a mouth. Resize it so a few could fit in a box.

![choosing a fruit sprite and drawing a face on it.](images/choose-fruit.gif)

--- /task ---

--- task ---

Position your fruit near the top of the stage, and under a `green flag`{:class="block3events"} add a `go to x: () y: ()`{:class="block3motion"} block.

```blocks3
when green flag clicked
go to x: (0) y: (115)
```

--- /task ---

--- task ---

Make the fruit follow the mouse pointer. 

Wrap the `go to x: y:`{:class="block3motion"} block in a `forever`{:class="block3control"} loop, and change its `x`{:class="block3motion"} to the `mouse x`{:class="block3sensing"} position.

```blocks3
when green flag clicked
+forever
go to x: (mouse x) y: (115)
end
```

--- /task ---

--- task ---

Only move the fruit while the mouse is clicked by putting the `go to x: y:`{:class="block3motion"} block inside an `if <mouse down?>`{:class="block3control"} block.

```blocks3
when green flag clicked
forever
+if <mouse down?> then
go to x: (mouse x) y: (115)
end
end
```

--- /task ---

**Test:** Click the green flag, then click on the stage. Your fruit follows the mouse pointer left and right, but stays at the same height.

![clicking to move the fruit along the top.](images/mouse-click.gif)

## Make the fruit sprite

In this step, you'll add the first piece of fruit and make it follow the mouse pointer.

--- task ---

Start a new Scratch project and delete the cat sprite.

Add a new sprite for your fruit. You can choose any fruit you like from the sprite library — or an animal, or anything you want to see drop into the box!

--- /task ---

--- task ---

Use the paint tools to give your sprite some character: add a pair of eyes and a mouth. Resize it so a few could fit in a box.

![PLACEHOLDER GIF: choosing a fruit sprite and drawing a face on it with the paint tools.](images/choose-fruit.gif)

--- /task ---

--- task ---

Now make your fruit follow the mouse pointer along the top of the screen, ready to drop.

Add a `when green flag clicked`{:class="block3events"} block and a `forever`{:class="block3control"} loop. Inside the loop, check whether the player is holding the mouse down, and if they are, send the fruit to the mouse pointer's `x`{:class="block3sensing"} position near the top of the screen.

```blocks3
when green flag clicked
forever
if <mouse down?> then
go to x: (mouse x) y: (110)
end
end
```

--- /task ---

Click the green flag, then click and hold anywhere near the top of the stage. Your fruit follows the mouse pointer left and right.

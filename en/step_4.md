## Drop them

In this step, you'll make the fruit drop down the screen.

--- task ---

![the fruit sprite.](images/fruit.png)

In the fruit sprite add a `forever`{:class="block3control"} loop in `when I start as a clone`{:class="block3control"} and make it fall by changing the `y`{:class="block3motion"} position.

```blocks3
when I start as a clone
go to x: (mouse x) y: (115)
start sound (Pop v)
+forever
change y by (-4)
end
```

--- /task ---

--- task ---

**Test:** click the green flag and try dropping some fruit. Your fruit should fall, but the original fruit shows at the top too. 

Add `hide` and `show`{:class="block3looks"} blocks to hide the original fruit, so only the falling clones show.

```blocks3
when I start as a clone
go to x: (mouse x) y: (115)
start sound (Pop v)
+show
forever
change y by (-4)
end
```

```blocks3
when green flag clicked
+hide
forever
if <mouse down?> then
create clone of (myself v)
wait (0.1) seconds
end
end
```

--- /task ---

Click the green flag and drop some fruit, check that each piece falls down the screen, and the original is hidden.

![the clones falling down the screen.](images/falling.gif)
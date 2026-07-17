## Make the fruit fall

Right now the fruit just sits at the top. In this step, you'll make each clone fall down the screen.

--- task ---

Add blocks to your `when I start as a clone`{:class="block3control"} script so the clone shows itself, then falls by changing its `y`{:class="block3motion"} position again and again.

```blocks3
when I start as a clone
go to x: (mouse x) y: (110)
play sound (Pop v)
+show
+forever
change y by (-4)
end
```

--- /task ---

Click the green flag and drop some fruit. The clones fall — but you'll also see the **original** fruit sitting at the top, not moving.

--- task ---

Hide the original fruit so only the falling clones show. Add a `hide`{:class="block3looks"} block to the start of your `when green flag clicked`{:class="block3events"} script.

The clone already has a `show`{:class="block3looks"} block, so each clone still appears as it drops.

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

Click the green flag and drop some fruit. Each piece falls down the screen and the original fruit is hidden.

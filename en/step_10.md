## Challenge: make your fruit stack

Your game works! Right now, though, different fruit fall straight through each other. If you want them to pile up in a satisfying heap, you can make each fruit rest on top of fruit that isn't its match.

--- task ---

For each costume, add a check: if the clone is touching **either of the other two colours**, nudge it back up so it stacks instead of overlapping. It's the same trick you used for the floor — fall a little, then push back up.

For your first fruit, add this inside its `if (costume number) = (1)`{:class="block3control"} block, below the merge check:

```blocks3
if <(costume [number v]) = (1)> then
if <touching color (#4e9a06)?> then
change y by (-4.2)
wait (0.2) seconds
play sound (Squish Pop v)
delete this clone
end
+if <<touching color (#ec1c2c)?> or <touching color (#edd51c)?>> then
change y by (4.1)
end
end
```

--- /task ---

--- task ---

Now copy that new `if`{:class="block3control"} into your other two costume checks. Each time, change the two colours so they name the **other** fruit — the ones that costume should *not* merge with.

> **Tip:** in game-making, this is called a **collision**. Each `if (costume number) = ()`{:class="block3control"} block should end up mentioning all three colours: one that deletes the fruit, and two that make it stack.

![PLACEHOLDER GIF: fruit of different types piling up in a stack.](images/stacking.gif)

--- /task ---

Click the green flag and fill the box. Different fruit now stack up into a pile, and matching fruit still merge.

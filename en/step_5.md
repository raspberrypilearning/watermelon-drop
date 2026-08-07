## Make them land

Add a floor and make the fruit land on it.

--- task ---

In the add sprite icon, choose **Paint** to draw a new sprite and name it **Floor**.

![The paint sprite from menu.](images/sprite-paint.png){:width="200"}

--- /task ---


--- task ---

Use the edit tools to draw a line or a solid rectangle across the middle of the paint area. This will be the floor your fruit rests on.

![Making a floor in paint.](images/floor-paint.png){:width="450"}

--- /task ---

--- task ---

![floor sprite](images/floor.png){:width="150"}

Move the **Floor** sprite to the bottom of the stage. 

Add a `green flag`{:class="block3events"} block, with a `set drag mode`{:class="block3sensing"}, and a `go to x: y:`{:class="block3motion"} block to set it where you positioned it.

```blocks3
when green flag clicked
set drag mode [not draggable v]
go to x: (0) y: (-125)
```

--- /task ---

--- task ---

![The fruit sprite.](images/fruit.png){:width="150"}

Click on the **fruit** sprite, add an `if`{:class="block3control"} block to check whether the clone is `touching`{:class="block3sensing"} the floor. If it touches the floor, it will move up by `changing`{:class="block3motion"} the **y**.

```blocks3
forever
change y by (-4)
+if <touching (Floor v)?> then
change y by (4.1)
end
end
```

> [!TIP]
>
> The fruit falls by 4 each time, then jumps back up by 4.1 when it touches the floor. Those two numbers almost cancel out, so the fruit looks like it is wobbling.
--- /task ---


**Test:** Click the green flag and check that the fruit falls and lands on the floor.

![Fruit dropping and coming to rest on the floor.](images/fall-floor.gif){:width="450"}

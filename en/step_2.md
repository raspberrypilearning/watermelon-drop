## Add your first fruit

In this step, you'll add the first piece of fruit and make it follow the mouse pointer, ready to drop.

> [!TASK]
>
> [Start a new Scratch project](https://scratch.mit.edu/projects/editor/){:target="_blank"}.

> [!TASK]
>
> Delete the cat sprite.
>
> ![Deleting the cat sprite with the trashcan.](images/delete-cat.png){:width="200"}


> [!TASK]
>
> Choose a new sprite for your fruit. You can choose one from the library or draw your own.
>
> ![The Choose a Sprite menu.](images/choose-sprite.png){:width="200"}

> [!TASK]
>
> Use the paint tools to give it some character: a pair of eyes and a mouth. Resize it so a few could fit on the stage.
>
> ![choosing a fruit sprite and drawing a face on it.](images/choose-fruit.gif){:width="450"}

> [!TASK]
>
> ![the fruit sprite.](images/fruit.png){:width="150"}
>
> >Position your fruit near the top of the stage. 
> >
> > Under the `green flag`{:class="block3events"}, add a `set drag mode`{:class="block3sensing"} block and choose **not draggable** from the drop-down menu so players can't drag it. Then add a `go to x: y:`{:class="block3motion"}.
> >
> ```blocks3
> when green flag clicked
> set drag mode [not draggable v]
> go to x: (0) y: (115)
> ```

> [!TASK]
>
> Make the fruit follow the mouse pointer. 
>
> Wrap the `go to x: y:`{:class="block3motion"} block in a `forever`{:class="block3control"} loop, and change its **x**{:class="block3motion"} to the `mouse x`{:class="block3sensing"} position.
>
> ```blocks3
> when green flag clicked
> set drag mode [not draggable v]
> +forever
> go to x: (mouse x) y: (115)
> end
> ```

> [!TASK]
>
> Only move the fruit while the mouse is held down. First, wrap the `go to x: y:`{:class="block3motion"} block in an `if () then`{:class="block3control"} block.
>
> ```blocks3
> when green flag clicked
> set drag mode [not draggable v]
> forever
> +if <> then
> go to x: (mouse x) y: (115)
> end
> end
> ```

> [!TASK]
>
> Now drop a `mouse down?`{:class="block3sensing"} block into the hexagon slot of the `if`{:class="block3control"} block.
>
> ```blocks3
> when green flag clicked
> set drag mode [not draggable v]
> forever
> +if <mouse down?> then
> go to x: (mouse x) y: (115)
> end
> end
> ```

**Test:** Click the green flag, then click on the stage. Your fruit follows the mouse pointer left and right, but stays at the same height.

![clicking to move the fruit along the top.](images/mouse-click.gif){:width="450"}

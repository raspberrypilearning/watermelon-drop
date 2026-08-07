## Drop them

In this step, you'll make the fruit drop down the screen.

> [!TASK]
>
> ![the fruit sprite.](images/fruit.png){:width="150"}
>
> Add a `forever`{:class="block3control"} loop in `when I start as a clone`{:class="block3control"} and make it fall by changing the `y`{:class="block3motion"} position.
>
> ```blocks3
> when I start as a clone
> go to x: (mouse x) y: (115)
> start sound (Pop v)
> +forever
> change y by (-4)
> end
> ```

**Test:** Click the green flag and try dropping some fruit. Your fruit should fall, but the original fruit should show at the top too. 

> [!TASK]
>
> Add `hide`{:class="block3looks"} and `show`{:class="block3looks"} blocks to make only the clones show.
>
> Hide the original fruit:
>
> ```blocks3
> when green flag clicked
> set drag mode [not draggable v]
> +hide
> forever
> if <mouse down?> then
> create clone of (myself v)
> wait (0.1) seconds
> end
> end
> ```
>
> And make the new clone show.
>
> ```blocks3
> when I start as a clone
> go to x: (mouse x) y: (115)
> start sound (Pop v)
> +show
> forever
> change y by (-4)
> end
> ```

**Test:** Click the green flag and drop some fruit. Check that each piece falls down the screen, and that the original fruit is hidden.

![The clones falling down the screen.](images/falling.gif){:width="450"}

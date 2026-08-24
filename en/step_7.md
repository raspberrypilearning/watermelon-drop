## Add more fruit

In this step, you'll add more fruit!

> [!TASK]
>
> ![the fruit sprite.](images/fruit.png){:width="150"}
>
> Click the **Costumes** tab of your fruit sprite.
>
> ![The costumes tab.](images/tab_costumes.png){:width="450"} 

> [!TASK]
>
> Add a new costume for each new kind of fruit you want. To keep it simple, try adding one or two more to start with.
>
> ![choose costume.](images/choose-costume.png){:width="200"} 

> [!TASK]
>
> Make sure the new fruit have a **solid outline of one colour** all the way around, just like your first fruit.
>
> ![adding a second and third fruit costume in the Costumes tab.](images/add-costumes.png){:width="450"}

> [!TIP]
>
> If your sprite came with extra costumes you don't want, delete them. Otherwise they'll turn up in the game too.

> [!TASK]
>
> Now add a `switch costume`{:class="block3looks"} and drag the `random`{:class="block3operators"} block. This will choose a random costume number each time so that a different fruit appears.
>
> ```blocks3
> when I start as a clone
> +switch costume to (pick random (1) to (3))
> go to x: (mouse x) y: (115)
> start sound (Pop v)
> show
> forever
> change y by (-4)
> if <touching (Floor v)?> then
> change y by (4.1)
> end
> if <touching color (#4e9a06)?> then
> change y by (-4.2)
> wait (0.2) seconds
> start sound (Lo Gliss Tabla v)
> delete this clone
> end
> end
> ```
>
> Fill in the random numbers for the number of costumes you have.

**Test:** Click the green flag and click the mouse to check if a random one of your fruit appears each time.

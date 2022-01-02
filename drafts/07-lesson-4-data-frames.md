# Lesson 4: Data Frames and More Functions

As you know, health tracker apps collect a lot more than just step counts. They also collect data on hours of sleep, distance walked, and heart rate.

We could store all of this information in separate vectors, and in fact that's what we are going to do.

To keep all of these vectors in one place, coders use data frames. Think of a data frame as a data table and a vector as a column in that table.

For our app, we've made a data frame with sample health data and named it `tracker`. Type its name in the window below to view it.

<iframe data-type="datacamp" id="df-1" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-data-frames-1.html" style="border: 0px #ffffff none;" width="100%"></iframe>

Note that each row represents the step count, heart rate, distance, and amount of sleep for a different day. For now, you don't have to know how to create a data frame. But it's useful, when you're coding,  to know how to use them.

To view one variable of a data frame, we use `$`. For example, you could type `df$var` to view a variable named `var` in a dataframe named `df`. What do you think `df` stands for?

Try viewing just the `heart_rate` variable from our data frame.

<iframe data-type="datacamp" id="df-2" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-data-frames-2.html" style="border: 0px #ffffff none;" width="100%"></iframe>

Well done! Next, let's try using a new function. Many functions are meant to work with data frames. So, they take at least two arguments:

* the data frame you are analyzing
* the column you want to focus on

Use the `arrange()` function to sort the data in order by `distance`. Separate arguments using a comma `,`.

<iframe data-type="datacamp" id="df-3" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-data-frames-3.html" style="border: 0px #ffffff none;" width="100%"></iframe>

Notice that since each row represents one day's data, all the data from that day (row) moves together when we rearrange the data frame.

What if we want to see the longest distance first? The default setting for `arrange()` is to sort data in ascending order. If we want to arrange distance from highest to lowest, we can use the `desc()` function.

Try using `arrange()` and `desc()` together to view the longest distance first.

<iframe data-type="datacamp" id="df-4" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-data-frames-4.html" style="border: 0px #ffffff none;" width="100%"></iframe>

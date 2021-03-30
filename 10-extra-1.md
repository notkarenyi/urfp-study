# Extra Practice 1

Great work so far! The `filter()` function works similarly to the `arrange()` function, except that instead of supplying a data frame and a column argument, we supply a data frame and a condition.

For example, the condition `heart_rate < 80` means that each row of the data will only be kept if the heart rate recorded for that day was less than 80.

Try filtering `tracker` for days where we walked less than 10,000 feet.

Let's combine everything we've learned so far. Select the `heart_rate` variable from `tracker`. What do you notice about it?

<iframe data-type="datacamp" id="extra-1-1" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-1-1.html" style="border: 0px #ffffff none;" width="100%"></iframe>

There seems to be a typo in one of the rows. We haven't learned how to change the data in a data frame, but sometimes coders choose to ignore data that is clearly wrong. Filter `tracker` in a way that removes extremely large values of `heart_rate`. 

Assign the result of this filtering to a new data frame named `tracker`. 

<iframe data-type="datacamp" id="extra-1-2" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-1-2.html" style="border: 0px #ffffff none;" width="100%"></iframe>

Notice that we overwrote the old `tracker` data frame, since we can't have two objects with the same name. This is how coders "save" their actions in R. If we hadn't saved our work, the next time we used `tracker`, we would find that it had reverted back to the original data frame!
# Extra Practice 3

How do we answer the question: what is the typical daily distance walked for the person who used this tracker app? Questions about typical values refer to the center of a distribution of data. 

One way to do this is to calculate the average, or the mean. The average is calculated by adding up all the values and dividing this sum by the total number of values. Fortunately, coders have the `mean()` function to do the work for them. The mean function takes one main argument: the data that you want to analyze.

Find the mean of `distance`. Does this correspond with the tallest peak that you noted in the previous exercise?

<iframe data-type="datacamp" id="extra-3-1" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-3-1.html" style="border: 0px #ffffff none;" width="100%"></iframe>


Another measure of center is the median. If we have n number of values in our data set, and we sort the data in ascending order, we can take the value at position `n / 2` as our median. This is the middle number in our data. 

Try using the `median()` function to find the median of `distance`.

<iframe data-type="datacamp" id="extra-3-2" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-3-2.html" style="border: 0px #ffffff none;" width="100%"></iframe>


The `sd()` function calculates the standard deviation of data. Standard deviation is a way of measuring the spread of data: are most values bunched up close around the mean, or are they scattered far away from the mean?

Calculate the standard deviation of `distance`. Do you walk a consistent amount every day, or does the distance walked vary greatly from day to day?

<iframe data-type="datacamp" id="extra-3-3" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-3-3.html" style="border: 0px #ffffff none;" width="100%"></iframe>


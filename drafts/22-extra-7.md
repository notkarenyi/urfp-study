# Extra Practice 7

Boxplots are a type of graph that simplifies data into five numbers. If you imagine that the numbers in our dataset were sorted from lowest to highest, then the five-number summary would include: 

* minimum, or smallest number
* maximum, or biggest number
* median, or middle number
* first quartile, which is located halfway between the minimum and the median
* third quartile, which is located halfway between the median and the maximum

Coders use the `gf_boxplot()` function like they use the `gf_scatterplot()` function: with two variables, in the format `y_var ~ x_var`. 

Run the code below to see what we mean.

<iframe data-type="datacamp" id="extra-7-1" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-7-1.html"></iframe>

In the example above, when we put the number `1` in place of one of the variables, we were able to use the `gf_boxplot()` function to view just one variable at a time (like `steps`). This is similar to the histogram functions we saw earlier, because histograms also view only one variable at a time. 

Now, create a scatterplot for `steps` using `1` in place of the `x` variable.

<iframe data-type="datacamp" id="extra-7-2" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-7-2.html"></iframe>

Now we're ready to see what the two functions look like on the same graph. We can combine functions using the pipe symbol: `%>%`. 

Create a layered boxplot and scatterplot for our `steps` data. Notice that they are different representations of the same underlying data.

<iframe data-type="datacamp" id="extra-7-3" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-7-3.html"></iframe>
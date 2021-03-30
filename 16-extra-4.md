# Scatterplots 

You might have noticed when we were creating histograms that the graphs of `heart_rate` and `distance` have similar shapes. Are they related? 

We can use scatterplots to examine relationships between two variables. When we say that two variables are related, we mean that one variable (the predictor) helps predict the value of the other variable (the outcome).

The function `gf_point` takes only two main arguments, just like the other `gf_*` functions. However, instead of the `~ variable` argument that you are familiar with, we now need to supply two variables, in the format `y_var ~ x_var`. You may be familiar with the concept of x variable and y variable from math class--we use the same concept in statistics graphs.

Use `gf_point()` to find out whether `heart_rate` and `distance` are related. 

<iframe data-type="datacamp" id="extra-4-1" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-4-1.html" style="border: 0px #ffffff none;" width="100%"></iframe>

Notice that the points seem to fall on a rough line: lower values of heart rate correspond to lower values of distance, and higher heart rate to longer distance. This makes sense, because your heart rate increases with prolonged periods of exertion. 

When points seem to fall on a line instead of being randomly spread out, this tells us the two variables are related.

Are `steps` and `sleep` related?

<iframe data-type="datacamp" id="extra-4-2" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-4-2.html" style="border: 0px #ffffff none;" width="100%"></iframe>

On this graph, we don't see much of a pattern in the data: everything is scattered haphazardly.

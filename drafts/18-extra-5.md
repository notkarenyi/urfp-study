# Histograms 

Earlier when we visualized data from `tracker`, we introduced the histogram. The idea behind a histogram is that data gets split up into equally sized "bins". Imagine that we took all our data for `heart_rate` and sorted it into bins: we had one for heart rates between 60 and 65 beats per minute, one for 65-70 bpm, and so on. 

The y axis represents the number of observations that we ended up with in each bin.

Make a histogram of `distance` using `gf_histogram()` to view the histogram again.

<iframe data-type="datacamp" id="extra-5-1" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-5-1.html" style="border: 0px #ffffff none;" width="100%"></iframe>


Some functions have additional arguments, other than the data frame and column of interest. Histograms allow you to adjust the number of bins you use, or alternatively, the percentage of values represented in each bin. The default number of bins is 30.

Create another histogram, using the `bins` argument to set a number of bins smaller than 5.

<iframe data-type="datacamp" id="extra-5-2" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-5-2.html" style="border: 0px #ffffff none;" width="100%"></iframe>

You can see that it's harder to discern patterns in the data because each bin contains a lot of data. When too many observations are in each bin, it's harder to see more subtle patterns within each bin.

In contrast, what happens if you set the number of bins to more than 500? (Stay at or below 1000 bins to reduce loading time.)

<iframe data-type="datacamp" id="extra-5-3" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-5-3.html" style="border: 0px #ffffff none;" width="100%"></iframe>

Most bins only have 1 entry, which is less useful for seeing trends in the data. There's big gaps between the bins that contain any data at all. This is an indication that we had too many bins.

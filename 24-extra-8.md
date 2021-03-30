# Extra Practice 8

You might have noticed that we haven't really worked with the `sleep` variable. Health tracker apps often ask you to round your estimated amount of sleep (even if they don't, we often round anyway). This has an interesting effect on our layered graphs.

Try layering a scatterplot of `sleep` over a boxplot, like we did before.

<iframe data-type="datacamp" id="extra-8-1" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-8-1.html"></iframe>

Weird&mdash;this data set has almost 30 days' worth of data, but we only see five points on our scatterplot. Are we missing some data?

Actually, because we rounded to the nearest quarter of an hour, there are only a few possible values for `sleep`. If we slept 8 hours on 10 different days, those data points would overlap on our graph, so that we can't see all the points at once.

In order to see all the points at once, coders can "jitter", or randomly move, the points on the graph. If a scatterplot was created by someone carefully placing the points where they are supposed to be, a jitterplot is what happens when we come along and shake things up.

Let's recreate our layered boxplot and scatterplot of `sleep`, using `gf_jitter()` instead of `gf_point()`.

<iframe data-type="datacamp" id="extra-8-2" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-8-2.html"></iframe>

Another option we could use to reveal points that are hidden behind each other is to use special arguments. 

Remember how we used the `bins` argument to adjust our histograms? `bins` is only for histograms, but all graphs can be adjusted using additional arguments called **aesthetics**.  For example, `alpha` controls transparency using values from `0` to `1`. `size` controls the size of the points.

Try using a combination of these to improve our scatterplot in our first scatterplot + boxplot graph. Why is this a better representation of our data?

<iframe data-type="datacamp" id="extra-8-3" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-8-3.html"></iframe>
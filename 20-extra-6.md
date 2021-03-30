# Extra Practice 6

Coders sometimes want to view not the raw counts of the observations in each bin (for example, heart rate was between 65-75 bpm on 5 days), but instead the proportion of the total data that are contained in that bin (for example, heart rate was between 65-75 bpm on 25% of the days). 

So rather than having "number of observations in this bin" on the y axis, we would have "number of observations in this bin divided by total number of observations from all bins". (This is a simplification, but basically that's what the graph represents.) 

This type of graph is called a **density histogram**.

Use `gf_dhistogram()` to create a density histogram of `sleep`.

<iframe data-type="datacamp" id="extra-6-1" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-6-1.html"></iframe>

**Density plots** are similar to density histograms, except there aren't really any bins. They show a smoother graph of essentially the same thing as a density histogram.

Sometimes it is useful for coders to view two representations of the same data at the same time. To use `gf_density()` and `gf_dhistogram()` together, use the conjunction `%>%`. This operator is called the pipe, and you can use it to simply stick one graph on top of another one.

<iframe data-type="datacamp" id="extra-6-2" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-extra-6-2.html"></iframe>

Now it's much easier to see the underlying shape of the data.
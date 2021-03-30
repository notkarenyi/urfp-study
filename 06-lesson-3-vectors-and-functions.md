# Lesson 3: Vectors and Functions

Functions are a new concept: think of them as commands we can use to accomplish certain tasks. There are 3 things you need to know about functions:

1. Every function has a name, followed by parentheses.
2. Every function takes 0 or more arguments, which go inside the parentheses.
3. Every function gives an output.

Functions are like little machines: you put some stuff in it, and depending on what you put in, something comes out.

Below, we've put an example using the `sum()` function. Try running the code to see what we mean!

<iframe data-type="datacamp" id="vectors-1" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-vectors-1.html" style="border: 0px #ffffff none;" width="100%"></iframe>

Great job! As you can probably see, the `sum()` function adds numbers together. You put numbers in, and it puts out the sum of those numbers.

Coders can use functions to solve lots of interesting problems. Here is one: instead of storing a single value in a variable, what if we wanted to store multiple values together?

For example, let's say we wanted to create a health tracker app. One thing you could track is the number of steps you've taken over the past three days. How could you store all those numbers in one variable?

That's what vectors are for! When we want to make a vector, we can use the `c()` function and feed it the arguments we want to store in the vector. In this case, `c` is the name of the function, and the output is a vector containing all the values we put into it. Remember, a vector is a variable that stores multiple values at once.

Try using `c()` to create a step count vector that stores the number of steps you walked for each of the past three days: on Monday you walked 1000 steps, on Tuesday you walked 700 steps, and on Wednesday you walked 8000 steps. Name the vector `steps`.

<iframe data-type="datacamp" id="vectors-2" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-vectors-2.html" style="border: 0px #ffffff none;" width="100%"></iframe>

Nice job, coder! Another useful function is length(). Use this to find the length of our vector.

<iframe data-type="datacamp" id="vectors-3" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-vectors-3.html" style="border: 0px #ffffff none;" width="100%"></iframe>

You're doing great! Let's try putting what we've learned together. Try using the `sum()` and `length()` function together to find the *mean* number of steps taken over the three days. Remember, the mean is the sum of all the values in the vector divided by the total number of values in the vector.

<iframe data-type="datacamp" id="vectors-4" height="350" src="https://uclatall.github.io/mtucker-coding-study/data-camp/dc-vectors-4.html" style="border: 0px #ffffff none;" width="100%"></iframe>

Great job! Let's move on to the next lesson.

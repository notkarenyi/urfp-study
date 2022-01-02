## CourseKata study

### Questions

* How are math anxiety (pre), math experience (pre), and math preparation (post) related?
* How are math anxiety (pre) and CS experience (pre) and math experience (pre) related?
* Change in mindset (pre and post)
* Relation of mindset to memorization attitude/expectation (pre and post)
* Relation of attending class to performance on exercises
* How are math experience and CS experience related to final grades? 
* How are math and CS experience related to attending class?
* Are the time spent in class, attending class, and time spent studying variables reliable? (Is there social pressure inflating scores?)
* Which problems in the textbook give students the most trouble, and why?
  * is looking at the book even productive? ie desirable difficulties
  * maybe we should look at tests instead
  * do students get things wrong because it is a learning process and they don't give as much thought as they could during a test, or because they are genuinely struggling?

### Variables

#### Pre-survey

* Value and expectancy are double validated questions

| prompt                                                       | code                        |
| ------------------------------------------------------------ | --------------------------- |
| Approximately how many hours per week do you work at paid employment? | work_hours                  |
| Be a role model for people in my community                   | college_bc_role_model       |
| Become an independent thinker                                | college_bc_thinker          |
| Do you commute more than 30 minutes each way to attend this school? | commuter                    |
| Expand my understanding of the world                         | college_bc_lrn_world        |
| Explore new interests                                        | college_bc_new_interests    |
| Give back to my community                                    | college_bc_community        |
| Have you had experience with computer programming before?    | cs_xp                       |
| Help my family out after I'm done with college               | college_bc_family           |
| How well have you done in mathematics courses you have taken in the past? | math_perform                |
| I am feeling very anxious about being able to master the material in this course. | course_anxiety              |
| I believe that I can be successful in this course.           | course_conf                 |
| I expect that this course will require a lot of memorization. | memorize                    |
| I know I can learn the material in this course.              | learn_conf                  |
| If you indicated in the prior question that you prefer to self-describe your gender, how do you describe yourself? | gender2                     |
| If you indicated in the prior question that you prefer to self-describe your racial/ethnic background, how do you describe yourself? | race2                       |
| In general, I tend to feel very anxious about mathematics.   | math_anxiety                |
| In this course, you will use R (a programming language) to analyze data.  How do you feel about this? | r_attitude                  |
| Is English your most proficient language?                    | ell                         |
| Learn more about my interests                                | college_bc_old_interests    |
| No matter how much math ability you have, you can always improve it. | growth_set                  |
| Provide a better life for my own children                    | college_bc_children         |
| Show that people with my background can do well              | college_bc_prove_background |
| The content of this course is important for me.              | content_important           |
| What best describes your gender?                             | gender                      |
| What best describes your racial/ethnic background?           | race                        |
| What I learn in this course will be useful in the future.    | course_useful               |
| What is the highest level of education completed by your mother? | mother_ed                   |
| What is your GPA at this school?                             | gpa                         |
| What is your year in school?                                 | year_school                 |
| When I think about this course, I'm concerned that... (write \not at all\ if you so feel) | concerns                    |
| Which of the following courses have you successfully completed? (Check all that apply) | past_courses                |
| Which of the following describes you?                        | student_type                |
| Write a brief biography of your experiences learning mathematics over the years.  Where possible, please provide specific examples.  Write at least 150 but no more than 300 words. | math_xp_long                |
| You can learn new things, but you can't really change your basic math ability. | fixed_set                   |
|                                                              | college_motive              |

#### Post-survey

| prompt                                                       | code                 |
| ------------------------------------------------------------ | -------------------- |
| Did you usually attend class?                                | attendance           |
| Did you wait until the last minute to do your homework?      | procrastinate        |
| I had the math preparation needed to succeed in this course. | math_prepared        |
| I learned a lot from this course.                            | amt_learned          |
| I think other instructors should use this book for teaching statistics. | book_attitude        |
| I think statistics is interesting and enjoyable.             | stats_interest       |
| In this course, you used R (a programming language) to analyze data.How do you feel about this now? | r_attitude           |
| No matter how much math ability you have, you can always improve it. | growth_set           |
| R coding exercises                                           | exercises            |
| The content of this course is important for me.              | content_important    |
| The online textbook                                          | book_study           |
| This course required a lot of memorization.                  | memorize             |
| This course required deep thinking and understanding of concepts. | conceptual           |
| This course was challenging.                                 | difficult            |
| Time spent in class                                          | class_time           |
| Time studying with other students                            | group_study          |
| Understanding the content of this course is more important to me than getter good grades. | content_vs_grade     |
| Use R to analyze a new dataset                               | r_conf               |
| What advice would you give to future students who want to do well in this course? | advice               |
| What I learn in this course will be useful in the future.    | course_useful        |
| Why? [attendance]                                            | Why? [attendance]    |
| Why? [procrastinate]                                         | Why? [procrastinate] |
| You can learn new things, but you can't really change your basic math ability. | fixed_set            |

#### Other

| construct                            | operationalization                                           |
| ------------------------------------ | ------------------------------------------------------------ |
| Attempts per exercise                | `group_by(item) %>% summarize(sum(attempt))`                 |
| Items attempted overall              | `sum(attempts)`                                              |
| Points on exercises                  | `sum(points_earned)`                                         |
| Points per chapter                   | `group_by(chapter) %>% summarize(points_earned)`             |
| Time spent on each chapter           |                                                              |
| Time spent total                     |                                                              |
| Points on practice quizzes           | `filter(str_detect(item, "Practice")) %>% sum(points_earned)` |
| Practice quizzes attempted           | `filter(str_detect(item, "Practice")) %>% sum(attempt)`      |
| Total time spent watching videos     |                                                              |
| Percentage of videos watched         |                                                              |
| Patterns completing practice quizzes |                                                              |
| Patterns watching videos             |                                                              |
| Word count for chapter summaries     |                                                              |

### Design

* Will replication be in the same study as the extension, or different?
* Presurvey is after experiment to avoid priming
* How will we get participants?

  * class credit, requirement
* What kind of materials?

  * DataCamp exercises with different intros

  * what kind of exercises? it should be interesting enough to be plausibly used as an introduction to coding that might by itself make people more interested in CS

  * we could have a control group that is given a computer game or other neutral activity during the time period. they could be given a similar prompt, except without anything indicating that they code during the experiment. 


```
Thank you for participating in this study. We will first give you an introduction to computer science, then ask you to complete a series of tasks. When you are ready, click Next to continue.

---

Introduction

Computer programmers perform all kinds of tasks, from running simulations to creating websites. Just like human languages, there are many programming languages, and each one is used by different groups of people. Unlike human languages, however, programming languages are usually built to accomplish specific purposes. Today we will introduce you to a programming language built for analyzing data, called R. 

The following pages will contain programming tasks that are designed to help you learn to be a programmer. Please try your best on each task, as this will result in deeper learning.

---

What is the difference between human languages and programming languages?

Human languages have less words, and programming languages have more words.
Human languages are not meant to accomplish specific purposes, but programming languages are.
Human languages are difficult to learn, but programming languages are actually quite simple.
Human languages were invented by people, and programming languages were not.

---

[Exercises]

---

Would you like to continue learning how to be a programmer, or would you like to watch a video solution for the remaining problems/a video about famous computer programmers?

---
Post-Survey

What is your major?

What race do you identify with?

White (Caucasian)
Black or African-American
Asian or Pacific Islander
Latinx or Hispanic
Native American or Alaska Native
Other
Prefer not to say

What gender do you identify with?

Female
Male
Other
Prefer not to say or I don't know

How interested are you in computer programming?

How likely would it be for you to enroll in a programming course before you graduate?
```

* cost concerns--we may only have the funds/resources to do comparison groups and not control

* what can realistically be included in the exercises? should the difficult problems be impossible, or just moderately difficult? easy and hard for each topic

  * start with data types and operators
  * if statements: 

  ```R
  # If statements are used to run code ONLY IF a certain condition is met. For example, the following code runs ONLY IF the sky is blue:
  
  if (sky == "blue") {
      umbrellas = "closed"
  }
      
  # Notice that when we are comparing values, we have to use `==` instead of `=`! This is because we used `=` for assigning values to variables, and we don't want to use the same operator for two different purposes. Otherwise, R would get confused.
      
  # Create a 
  ```

  * variables: 
    * can be difficult to grasp concept of manipulating things in a variable

  ```R
  #Variables are used to store information. For example, if we are making a user profile, we might want to store someone's name. We do this by assigning a variable name to a value, like this:
  
  name <- "Ichabod Crane"
  
  #Try it yourself! Create a variable named 'fav_color' and assign it to your favorite color. (If your code is not accepted, double check that you are following the format in the example.)
  ```

  * functions

  ```R
  #Functions are often used to store blocks of code that you need to use multiple times in a program. Based on your knowledge of coding, what is the output of the last line of the following code?
  
  myFun <- function (x, y) {
  	if (y > x) {
          log(x)
      } else {
          print("Wrong")
      }
  }
  
  myFun(12, 4)
  ```

  * recursion
  * a progression of questions for building a Magic 8 Ball (would this be too interesting? should we do a progression that isn't as much of a narrative or cliff-hanger?):

  ```R
  # Variable types
  
  # Certain types of variables hold certain types of values.
  
  ---
  
  # What if we wanted to store multiple values in one place? For example, maybe you wanted to create a grocery list, and you don't want to assign each value to a separate variable. Programmers use vectors to do just that. To create a vector, they use the `c()` function, like so:
  
  myVector = c(1, 2, 3)
  
  # Try creating your own vector called `groceries` and use it to store three things you like to eat. Don't forget to add quotes around the strings!
  
  ---
  
  # Now that you've learned about if statements, variables, and for loops, let's combine them into something interesting.
  
  # First, try combining the next three items into a vector:
  
  "Yes" "No" "Maybe"
  
  ---
  
  # Next, we will 
  ```

  * a progression of questions for creating an exchange rate calculator function:

  ```R
  # Great! Now let's try doing something with math. If 1 dollar is equal to 105 yen, how many yen is 5 dollars? (Hint: use the `dollars` variable to calculate the number of yen)
  
  dollars <- 5
  yen <- 
  
  ---
  
  # Nice! It's time to introduce you to 
  
  
  ```

  

* Or maybe the difficult ones are just misleading--how do we do that?

  * maybe tricking would be different emotions

```R
#Using your knowledge of coding, predict the output of the following code.

1st_president = "George Washington"
print(1st_president)
```

```R
#'If' statements, or conditional statements, are used to run a block a code 'if and only if' a condition is filled. For example, the following code inside the 'if' statement runs only if the variable 'age' is greater than 21:

#creating a variable to use later
age = 22

if (age > 21) {
    print("You are allowed to buy alcohol!")
}

#Try filling in the following condition to let people into their account only if the 'password' variable is equal to '123':

password = 123

if (WRITE CONDITION HERE) {
    print("You're in!")
}
```

* Do we need to encourage students in any way to continue the coding activities? should we worry about demand characteristics?
  * should we tell students why they got things wrong in the difficult exercises, or allow them the option to skip ahead? this could be an additional factor

```
Great! You can now choose to continue exploring being a programmer for the remaining time, or choose to watch a video about Bill Gates for the remaining time. 

(If you choose to continue programming, we will still give you a chance to switch to the video after each round.)

Continue?
Yes/No
```

* Some difficult questions from the book (<75% correct):

```R
# Assign 5 to num and 10 to NUM
num <-
NUM <-

# Now write the code to print out the number 10
```

```R
# Write code to save `my.vector * 100` back into `my.vector`

my.vector <-
```

```R
# Write some code that will store the answer to the question, "is the first element in the vector many.hellos "hi"? in an R object called firstIsHi
```

* ![image-20201106173554259](C:\Users\notka\AppData\Roaming\Typora\typora-user-images\image-20201106173554259.png)
* ![image-20201106173643142](C:\Users\notka\AppData\Roaming\Typora\typora-user-images\image-20201106173643142.png)
* Should we include free response prompts to have students internalize/practice R?
* Here is a sample of a possible progression of stats-type questions:

```R
# A data frame is just a data table. It stores rows of observations, and each column is a variable. 

#For example, in the following data frame, Harry, Hermione, and Ron each get their own row. Each column stores a different variable, like "fav_color" or "height".



```

```R
Random Sampling
A population includes all individuals we are interested in studying. For example, a study of monarch butterfly migration would have a population of all monarch butterflies. A study of people suffering from Alzheimer's would have a population of all people with Alzheimer's.

For a sample to be random, every object in the population must have an equal probability of being selected for the study. In practice, this is a hard standard to reach. But if we can’t have a truly random sample, we can at least try to feel confident that our sample is representative of the population we are trying to learn about.

For example, let’s say we want to measure how people from different countries rate their feelings of well-being. Which people should we ask? People from cities? Rural areas? Poor? Rich? What ages? Even though it might be difficult to select a truly random sample from the population, we might want to make sure that there are enough people in different age brackets, different socioeconomic status (SES), and different regions to be representative of that country.

Sampling Variation
Every sample we take—especially if they are small samples—will vary. That is, samples will be different from one another. In addition, no sample will be perfectly representative of the population. This variation is referred to sampling variation or sampling error. Similar to measurement error, sampling error can either be biased or unbiased.

For example, we’ve created a data frame called fakepop (for fake population) that has a single variable called number and 1,000 rows or cases. We set it up so that there are, in the variable fakepop$number, 100 0s, 100 1s, 100 2s, 100 3s, and so on for the numbers 0 to 9. Here is a graph (called a histogram) that helps you see that there are 100 of each digit in this fake population.
```

* We have to include a debriefing at the end, or else people might seriously become discouraged from learning to code.

```
Thank you for participating in this experiment.

This study attempts to explore reasons why people may be encouraged or discouraged to learn coding. As part of our methods, the last two exercises were rigged to be extremely difficult, and you were not expected to be able to get them right. 

Please don't be discouraged from exploring computer programming in the future! Real courses will give you the tools you need to succeed at the above exercises, at a much more manageable pace.
```

* Measures for mechanisms

  * For decreasing perceived risk/cost associated with engaging in activities:
  * For leading students to develop more inclusive beliefs about who can be involved in computer science:
* Controls:
  * "I'm gonna step away" or alternate recording modes
* datacamp-light
  * How to hide solutions?
* Hard concepts:
  * saving variables
  * variables vs values (what is a variable? why can we change it? how is it changed?)
  * factor()
  * nesting functions
  * 2.7
    * filtering/operations
    * NA
    * cleaning data and errors
    * in general, combining concepts is HARD
  * 2.8
    * ntile()
  * 3.2
    * concept of measurement error vs mistake
  * 3.4-3.5
    * density histograms vs regular histograms vs density plot
  * 3.8
    * tally()
  * 4.8
    * ntile()
    * which type of graph to apply to which type of data

### URFP/my thing

* Could we do half of the people where they are either placed with a peer or with a confederate? Then, we could see if having the presence of a peer who shares some aspect of your identity (eg gender, race) could have an impact on perceived performance, 
  * would this ruin statistical analyses or would it be ok if we just averaged over everything?
* We could also study whether framing information as identity-related ("Computer scientists use variables...") versus passive ("variables are used...")
* Textbook representation - syllabi? instructor, peer role models, environment, language
  * Framing science as an activity vs identity
  * Coming up with questions
  * Existing models with health behavior change and implicit belief and nudging
* We could do an additional factor of peer role models & identification
  * idk if this is ethically weird, but attributing the same quote of perseverance to differently gendered/racially associated names may have an effect on identity and risk orientation/calculation?
  * Although it's not perfect that people do automatically assign race and gender based on names, it does happen
  * What about gender-neutral names?

```
"When I first took CS 30 at UCLA, I'd never had any coding experience. I actually loved it, even though it was hard. Now I'm taking the whole CS 30 series!"
- Ben Friedan, UCLA Cognitive Science major

"When I first took CS 30 at UCLA, I'd never had any coding experience. I actually loved it, even though it was hard. Now I'm taking the whole CS 30 series!"
- Jordan Siegler, UCLA Cognitive Science major

"When I first took CS 30 at UCLA, I'd never had any coding experience. I actually loved it, even though it was hard. Now I'm taking the whole CS 30 series!"
- Val Garcia, UCLA Cognitive Science major
```



* Find scales for asking about computer science
* Stanford SPARQtools and other repositories of scales
* Write pre-survey questions on a MD
* Data analysis questions
* And some general programming
* Think about coding responses to open-ended questions

## Additional sources

* [Vicki Mays](maysv@nicco.sscnet.ucla.edu)
* [This Person Does Not Exist/GAN](https://thispersondoesnotexist.com/)
* [Cloze Drag and Drop answer type](https://authorguide.learnosity.com/hc/en-us/articles/360000439858-Cloze-Drag-Drop)
* 


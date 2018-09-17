# 431 Fall 2018 Class 07: 2018-09-18

## Today's Materials

- The slides are available [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class07/431_class-07-slides_2018.pdf) and [in R Markdown](https://raw.githubusercontent.com/THOMASELOVE/431-2018/master/slides/class07/431_class-07-slides_2018.Rmd).
- Class 7 audio files will be available after class.

## Announcements

1. Last time, we discussed Chapters 5, 9, 10 and 13 from Jeff Leek's *Elements of Data Analytic Style*. Some of that conversation is [captured here](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class07/LEEK.md).

2. I posted a **revised** [Homework 2 Answer Sketch](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework2) on 2018-09-15, after a student alerted me to a typo or two, and I realized I'd used older versions of tidyverse approaches for some of the graphs and summaries in what I'd posted initially.

3. Here's a hint for Question 7 on [Homework 3](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework3), which is due Friday 2018-09-21 at 12 noon.

- The problem many people have is building the data set of simulated values that you'll need in order to do some plotting. I decided to do this in a single tibble I called `q7_data`.
- If you're stuck, first try building a single set of Normally distributed random numbers with mean 100 and standard deviation 10, enough to cover all of the data you will need (and no more), and placing all of those values into one variable. 
- Then build a "group" variable which has four different labels (perhaps "Sample25", "Sample75", "Sample150" and "Sample225"), each of which is repeated the appropriate number of times. (So, for instance, you have 25 rows with "Sample25" and then 75 with "Sample75" and so forth.)
- The goal is for your data set to have the values you want to plot in one variable, and the "groups" which identify which sample each value is associated with, in another variable.
- My answer sketch includes the code `q7_data <- data_frame(value = big.sample, grp = big.grp)`.

4. There is a Minute Paper After Class 7. Please complete it by Wednesday 2018-09-19 at noon. Thank you.


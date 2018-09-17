# 431 Fall 2018 Class 07: 2018-09-18

## Today's Materials

- The slides are available [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class07/431_class-07-slides_2018.pdf) and [in R Markdown](https://raw.githubusercontent.com/THOMASELOVE/431-2018/master/slides/class07/431_class-07-slides_2018.Rmd).
- Class 7 audio files will be available after class.

## Announcements

1. Last time, we discussed Chapters 5, 9, 10 and 13 from Jeff Leek's *Elements of Data Analytic Style*. Some of that conversation is [captured here](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class07/LEEK.md).

2. I posted a **revised** [Homework 2 Answer Sketch](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework2) on 2018-09-15, after a student alerted me to a typo or two, and I realized I'd used older versions of tidyverse approaches for some of the graphs and summaries in what I'd posted initially.

3. There is a [Minute Paper After Class 7](http://bit.ly/431-2018-minute07) at http://bit.ly/431-2018-minute07. Please complete it by Wednesday 2018-09-19 at noon. Thank you.

## Hints for Homework 3

Here are two hints for [Homework 3](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework3), which is due Friday 2018-09-21 at 12 noon.

### Hint One: Get off to a smart start. 

Create a new project in a clean directory (like HW3) you've created, and copy the downloaded LBWunicef.csv file to that directory. Then, within the project in R Studio, your R Markdown file should begin with the YAML header, like this:

    ---
    title: "YOUR_NAME-hw3"
    author: "YOUR NAME"
    date: "`r Sys.Date()`"
    output:
        html_document:
            toc: yes
            code_folding: show
    ---

That should be followed by a setup chunk, and note that I use width 70 for HTML and width 60 if I'm building PDF:

    ```{r setup, message = FALSE}
    knitr::opts_chunk$set(comment=NA)
    options(width = 70)
    ```

And then a packages chunk, where I will also turn messages off in my output by adding message = FALSE after the comma in the chunk header:

    ```{r packages, message = FALSE}
    library(magrittr); library(tidyverse)
    ```

Note that:

- The only packages I loaded (with `library`) to do Homework 3 were `magrittr` and the `tidyverse`. I wouldn't recommend you load any others. 
- The labels for each chunk (like `setup` and `packages` here) are optional, but if you use them (and it's nice to do so) then they should not include spaces or periods and they must each be unique.

Then, you need to read in the `LBWunicef.csv` data into R, and place it into an R tibble. You should have downloaded the file at the start of the semester from the [Data and Code page](https://github.com/THOMASELOVE/431-2018-data). Make sure you have the `LBWunicef.csv` file in the same directory as your R Project for Homework 3, so that you see the file in your Files tab in R Studio. Then you need to get the data from that .csv file into R, and place it in a tibble. 

```{r}
hw3_data <- read.csv("LBWunicef.csv") %>% tbl_df
```

Then the data you need to do Questions 1-5 should be in the hw3_data tibble.

### Hint Two: Finish strong in Question 7.

The problem many people have with question 7 is building the data set of simulated values that you'll need in order to do some plotting. I decided to do this in a single tibble I called `q7_data`.

- The goal is for your data set to have the values you want to plot in one variable, and the "groups" which identify which sample each value is associated with, in another variable.
- When creating a set of random numbers, treat it as critically important that you first specify a seed for the random number selection using the `set.seed()` function.
- If you're stuck, first try building a single set of Normally distributed random numbers with mean 100 and standard deviation 10, enough to cover all of the data you will need (and no more), and placing all of those values into one variable.  I did this in a variable called `big.sample`, and I used the `rnorm` functuion to help me do this.
- Then build a "group" variable which has four different labels (perhaps "Sample25", "Sample75", "Sample150" and "Sample225"), each of which is repeated the appropriate number of times. (So, for instance, you have 25 rows with "Sample25" and then 75 with "Sample75" and so forth.) I did this in a variable called `big.grp`. I made use of the `rep` function to build this up.
- My answer sketch includes the code `q7_data <- data_frame(value = big.sample, grp = big.grp)`.



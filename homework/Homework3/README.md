# 431 Homework 3 Main Page

Homework 3 is due at noon on Friday 2018-09-21. It contains seven questions.

- Homework 3 [instructions are here](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework3/431-2018-hw3.md).

Any assignment received more than 60 minutes after the deadline is considered late. **Don't be late.**

## Homework 3 Answer Sketch is now fixed, and posted above.

Available in two flavors, PDF and R Markdown. Sorry about the delay.

## Hints for Homework 3

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

    ```{r read_data}
    hw3_data <- read.csv("LBWunicef.csv") %>% tbl_df
    ```

This should place the data you need to do Questions 1-5 should be in the hw3_data tibble.

### Hint Two: Finish strong in Question 7.

The problem many people have with question 7 is building the data set of simulated values that you'll need in order to do some plotting. I decided to do this in a single tibble I called `q7_data`.

- The goal is for your data set to have the values you want to plot in one variable, and the "groups" which identify which sample each value is associated with, in another variable.
- When creating a set of random numbers, treat it as critically important that you first specify a seed for the random number selection using the `set.seed()` function.
- If you're stuck, first try building a single set of Normally distributed random numbers with mean 100 and standard deviation 10, enough to cover all of the data you will need (and no more), and placing all of those values into one variable.  I did this in a variable called `big.sample`, and I used the `rnorm` functuion to help me do this.
- Then build a "group" variable which has four different labels (perhaps "Sample25", "Sample75", "Sample150" and "Sample225"), each of which is repeated the appropriate number of times. (So, for instance, you have 25 rows with "Sample25" and then 75 with "Sample75" and so forth.) I did this in a variable called `big.grp`. I made use of the `rep` function to build this up.
- My answer sketch includes the code `q7_data <- data_frame(value = big.sample, grp = big.grp)`.


## Steps to a Successful Homework

Here are the steps I would take to do the homework, after I read [the instructions](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework3/431-2018-hw3.md), and after I'd read the Introduction and Chapter 1 of Nate Silver's *The Signal and the Noise*.

1. Create a new directory called something like `431HW3`, specifically for this homework assignment.
2. Get the `LBWunicef.csv` data file from our [Data and Code page](https://github.com/THOMASELOVE/431-2018-data) into the `431HW3` directory you have created.
3. Open R Studio, and create a new R Project in this existing `431HW3` directory. 
4. Either create a new R Markdown file from scratch, or use one of the provided templates for an earlier assignment or for general work. Edit in R Studio to get what you want, and then be sure to save it using your actual name in the file name.
5. Knit the file in R Studio to create an HTML file, which should have your actual name in it, not something like `YOURNAME-hw3.html`
6. Review the HTML file closely, and make changes to the R Markdown file and re-knit until you are satisfied.
7. Write the response to the essay question as part of your R Markdown file. Leave blank lines between paragraphs to help us read your work. 
8. Submit your final R Markdown file and your final HTML file to us via [Canvas](https://canvas.case.edu), by the deadline, which again is noon Friday 2018-09-21.

## General Tips on Homework Submission

1. Submit HTML and R Markdown, without zipping the files together.
2. Use complete sentences, and proper English grammar, syntax and spelling. To use R Studio's spell-checker, hit F7.
3. Avoid printing things we don't need to see (like data frames) to judge your work.
4. Place empty lines before and after each code chunk.
5. Name every chunk, with no characters other than letters, numbers and underscores. No repetition!
6. Use headings to indicate the question being solved. Then leave a blank line before continuing with text.
7. Avoid repeating Dr. Love's questions verbatim.
8. When available, use the template, don't fight it.

# Material to Come

- The Answer Sketch is now posted. We don't post answer sketches for essay questions.
- Later, once the homework is graded, we'll post details on how you can get your grade on the assignment, as well as a more detailed grading rubric.

The main site for the course is https://github.com/THOMASELOVE/431-2018

# 431 Fall 2018 Class 17: 2018-10-30

## Today's Materials

- The slides are available [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class17/431_class-17-slides_2018.pdf) and [in R Markdown](https://github.com/THOMASELOVE/THOMASELOVE/431-2018/master/slides/class17/431_class-17-slides_2018.Rmd), above.
- Class 17 audio files will be posted above after class.

## Deliverables Coming Soon

- The [Minute Paper after Class 17](http://bit.ly/431-2018-minute17) is due at noon Wednesday 2018-10-31. Please attend to this.
- You have a new package (`janitor`) to install before Thursday. Also, you should update your packages. Details below.
- [Project Task D](https://thomaselove.github.io/431-2018-project/taskD.html) and [Project Task E](https://thomaselove.github.io/431-2018-project/taskE.html) are each due at noon this Friday 2018-11-02. 
    - For Task D (the Survey Comparison Plan), you'll fill out the Google Form at http://bit.ly/431-2018-survey-comparison-plan-taskD using the codebook at http://bit.ly/431-2018-survey-data-codebook.
    - For Task E (completing the actual Survey), you'll fill out the Survey itself at http://bit.ly/431-2018-survey
- [Homework 6](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework6/431-2018-hw6.md) is due (submit to [Canvas](https://canvas.case.edu/) by noon on Friday 2018-11-09.

The [Course Calendar](https://github.com/THOMASELOVE/431-2018/blob/master/calendar.md) is the final word on all deadlines.

## On the Course Project Survey, due Friday at NOON

You will complete two Google Forms by noon on Friday 2018-11-02. These are Task D ([the Survey Comparison Plan](http://bit.ly/431-2018-survey-comparison-plan-taskD)) and Task E ([actually taking the Survey](http://bit.ly/431-2018-survey)).

- You will receive access to the Survey data before class next Tuesday 2018-11-06. It will include at least three and perhaps more files, which you will then need to **merge** in order to obtain an appropriate data set.
    - We'll discuss merging briefly (but sufficiently for your project study 1 tasks) in Class 19, next Tuesday.
- The [Survey Codebook](http://bit.ly/431-2018-survey-data-codebook) specifies the item responses and calculated scales that will be provided.
    - Dr. Love will add missing values to selected items, to ramp up the management requirements.
        - For Project Study 1 (the survey) you will need to deal with missing values via simple imputation. We will discuss this before Thanksgiving.
        - For Project Study 2 (your data) you will deal with missing values by filtering out cases with missing values, unless Dr. Love has required you to do otherwise.
        - Many (if not most) of you will also need to deal with other data management issues (like, for instance, turning a quantitative response into a categorical one, or calculating a summary like BMI from height and weight) in your project study 1 analyses.
    - Some items were planned to have 0-100 responses, but the survey asks you to respond on a 0-10 scale. Dr. Love will fuzz up your results by adding noise so that the resulting scale is 0-100. How?
        - Multiply your response (0-10) by 10, obtaining a value between 0 and 100, and call that **a**.
        - Randomly draw an integer from a uniform distribution (probably on [-8, 8], but we may change that) and call that **b**. 
        - **a + b** is intended as your reported response, but that could be anything from -8 to 108, so we will truncate. Any values below 0 will be listed as 0 and any values above 100 listed as 100 in the data you will receive, and analyze.

## The Sleep and Mammals Example

- An [Extra Example](https://github.com/THOMASELOVE/431-2018/blob/master/quizzes/quiz01/extra.md) about Sleep and Mammals is available for you now. This example reviews some of the key work we did in Part A of the course. It uses the msleep data set, which is part of the ggplot2 package. It was originally used as a bonus assignment for some students to improve their grade on Quiz 1.
- I've now posted an [Answer Sketch for the Extra Example](https://github.com/THOMASELOVE/431-2018/blob/master/quizzes/quiz01/extra_A.pdf). I encourage you to look this over before Quiz 2. Hint, hint.

## Things in Today's Slides

- Today we're going to learn another way to bootstrap, with `slipper`. Visit https://github.com/jtleek/slipper for details.
- In today's slides, we make reference to [this cartoon from XKCD](https://xkcd.com/882/) entitled "Significant".

## A New R Package I'm adding to [our list](https://github.com/THOMASELOVE/431-2018/blob/master/software/packages.md): `janitor`

- [The `janitor` package](https://github.com/sfirke/janitor) in R, developed by Samuel Firke, is amazing. [Here is an overview](http://sfirke.github.io/janitor/articles/janitor.html) and we'll start using these tools on Thursday.
    - `clean_names()` handles problematic variable names and is something I expect you'll all get value from in your Project work.
    - fix dates stored as serial numbers with `excel_numeric_to_date()`
    - `tabyl()` is a tidyverse-oriented replacement for `table()`. It counts combinations of one, two, or three variables, and then can be formatted with a suite of `adorn_*` functions to look just how you want, and results in a tibble that can be piped right into knitr::kable() in an R Markdown report.
    - exploring Likert-scale factor levels with `top_levels()`
    - directionally-consistent rounding behavior with `round_half_up()`
- Install the `janitor` package by clicking on the Packages tab and hit Install, then type in janitor as the package you want to install. Now should be a good time to update your Packages in R, too (there's a new version of ggplot2, for instance.) To do so, click on the Packages tab and hit Update.

## Visualization of the Day: As the US Election heats up ...

- FiveThirtyEight's forecasts for ...
    - the 435 elections for the [U.S. House of Representatives](https://projects.fivethirtyeight.com/2018-midterm-election-forecast/house/), 
    - the 35 elections for the [U.S. Senate](https://projects.fivethirtyeight.com/2018-midterm-election-forecast/senate/), 
    - and the 36 elections for [Governor](https://projects.fivethirtyeight.com/2018-midterm-election-forecast/governor/) being held this Fall.
- You may also be interested in FiveThirtyEight's [Summary of the Latest Polls](https://projects.fivethirtyeight.com/polls/), if you want to see more of the "raw" data.


## REPEATING: Announcements sent via email last Friday 2018-10-26...

1. I have completed building the codebook / data description document for the project survey. It is a Google Sheet that I have posted at http://bit.ly/431-2018-survey-data-codebook. Log into Google via CWRU to see it. 
    - The Sheet lists every item and every scale I will provide to you for analyses, and specifies the item numbers (and names) you will need to complete Project Task D.
    - You will need that codebook in order to successfully complete the Project Task D (Survey Comparison Plan) form, which you'll find at http://bit.ly/431-2018-survey-comparison-plan-taskD. 
    - Those of you who responded to that form before 2018-10-27 will need to revise your work in light of the many small changes I made to item numbers in building the new codebook. I am very sorry for this inconvenience. The good news is that only a few items have had a meaningful change in their location in the survey, but you'll need to check your work and make all necessary adjustments before the deadline for Task D. 
    - The Project Task D deadline is Friday 2018-11-02 at noon.

2. [Here is the actual survey](http://bit.ly/431-2018-survey) that you will take to satisfy Project Task E. Remember that completing the survey is due at the same time as Task D: noon on Friday 2018-11-02. 
    - I think there are 156 items. Scroll to the end of the survey and answer the final question (your name) and then submit if you want to stop work partway through but return later where you stopped.

3. My summaries of all 49 project proposals [are now available](https://github.com/THOMASELOVE/431-2018-project/blob/master/OKtaskA.md). Please take a look.

4. Homework:

- The Homework 5 answer sketch [is now available](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework5). Grades and a rubric will likely be available on Thursday 2018-11-01.
- Homework 6 [is available now](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework6/431-2018-hw6.md). That assignment is due 2018-11-09 at noon. 
- Homework 7 [is also now available](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework7/431-2018-hw7.md) and is due 2018-11-16 at noon.

5. Canvas and the various Google Forms should now be up to date in terms of deadlines for remaining Project Tasks and Homeworks. Remember that the Course Calendar page at https://github.com/THOMASELOVE/431-2018/blob/master/calendar.md is the final word on everything.

6. The audio files for Class 16 are now posted to the [Class 16 README](https://github.com/THOMASELOVE/431-2018/tree/master/slides/class16) page.

## One Last Thing

- Take a look at Geoffrey Skelley and Rachael Dottle's work on the 2018 Election at FiveThirtyEight entitled "[What If Only Men Voted? Only Women? Only Nonwhite Voters?](https://fivethirtyeight.com/features/what-if-only-men-voted-only-women-only-nonwhite-voters/)" posted on 2018-10-26. 


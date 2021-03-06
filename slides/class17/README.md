# 431 Fall 2018 Class 17: 2018-10-30

## Today's Materials

- The slides are available [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class17/431_class-17-slides_2018.pdf) and [in R Markdown](https://github.com/THOMASELOVE/THOMASELOVE/431-2018/master/slides/class17/431_class-17-slides_2018.Rmd), above.
- Class 17 audio files are posted in the usual place.

## Deliverables Coming Soon

- The [Minute Paper after Class 17](http://bit.ly/431-2018-minute17) is due at noon Wednesday 2018-10-31. Please attend to this.
- You have a new package (`janitor`) to install before Thursday. Also, you should update your packages. Details below.
- [Project Task D](https://thomaselove.github.io/431-2018-project/taskD.html) and [Project Task E](https://thomaselove.github.io/431-2018-project/taskE.html) are each due at noon this Friday 2018-11-02. 
    - For Task D (the Survey Comparison Plan), you'll fill out the Google Form at http://bit.ly/431-2018-survey-comparison-plan-taskD using the codebook at http://bit.ly/431-2018-survey-data-codebook.
    - For Task E (completing the actual Survey), you'll fill out the Survey itself at http://bit.ly/431-2018-survey
- [Homework 6](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework6/431-2018-hw6.md) is due (submit to [Canvas](https://canvas.case.edu/) by noon on Friday 2018-11-09.

The [Course Calendar](https://github.com/THOMASELOVE/431-2018/blob/master/calendar.md) is the final word on all deadlines.

## Course Project Update: Tasks D and E are due at noon Friday

You will complete two Google Forms by noon on Friday 2018-11-02. These are Task D ([the Survey Comparison Plan](http://bit.ly/431-2018-survey-comparison-plan-taskD)) and Task E ([actually taking the Survey](http://bit.ly/431-2018-survey)). 

- At 8:30 AM on 2018-10-30, we have 23/49 responses to Task D, and 22/49 responses to Task E, not all of which are complete responses yet.

### Frequently Asked Questions About Task D (The Comparison Plan)

- In specifying the comparison plan, how do you want us to specify which items we're using? 
    - With the Item Number as provided in the [Survey Codebook](http://bit.ly/431-2018-survey-data-codebook). So if you were planning to use the item "For how long, in months, have you lived in Northeast Ohio?" which will have variable name `neohio_011`, you would type the item number, which is 11.
- In specifying your comparison plan, can you use a categorical item with more than 6 categories in the tasks which require fewer categories? 
    - Yes. You'll just have to collapse some of the levels of the factor in question so that you have an appropriate number of categories. Dr. Love will assume that you plan to do this if he sees you list such a variable in your plan.
    - When collapsing, I typically just use `fct_recode()` from the `tidyverse`. The goal is for each of the categories in your collapsed variable to have a minimum of 5 observations, but that may be a challenge. If the categorical variable is ordinal, then don't collapse levels that aren't next to each other. (For instance, if the categories are Excellent, Very Good, Good, Fair and Poor, you might collapse Fair and Poor together, but don't collapse Excellent and Fair together.)
- In specifying your comparison plan, can you use a quantitative (continuous) item as a categorical item? 
    - Yes. You'll just need to split the quantitative variable into a factor with two or more levels. Dr. Love will assume that you plan to do this if he sees you list such a variable in your plan.
    - For instance, you could split the responses into three subgroups by age, with the youngest third in one level, the middle third in another, and finally the oldest third in another. If you do this, make sure that your factor levels are ordered and labeled sensibly. The `cut2` function from the `Hmisc` package can be helpful here if you want the computer to determine the levels for you. If you want to pick them yourself, I suggest you look at the `fct_collapse` and `fct_recode` functions in the `tidyverse`.
- How will Dr. Love review my Plan in Task D?
    - He will verify that every time you've specified an analysis, it could make sense to do it in the way you specify, assuming you will collapse levels if needed, and create factors from quantities if needed.
    - If Dr. Love sees you list something that doesn't make sense, you'll have to redo that part of the Task, until he is satisfied.

**Note** The [Project Instructions](https://thomaselove.github.io/431-2018-project/), especially for Tasks F and G, were revised on 2018-10-29 to clarify these and other points.

### What Data Will I Receive after the Survey is Finished?

- You will receive access to the Survey data before class next Tuesday 2018-11-06. It will include at least three and perhaps more files, which you will then need to **merge** in order to obtain an appropriate data set.
    - We'll discuss merging briefly (but sufficiently for your project study 1 tasks) in Class 19, next Tuesday.
- The [Survey Codebook](http://bit.ly/431-2018-survey-data-codebook) specifies the item responses and calculated scales that will be provided.
    - Dr. Love will add missing values to selected items, to ramp up the management requirements.
        - For Project Study 1 (the survey) you will deal with missing values via simple imputation. 
        - For Project Study 2 (your data) you will deal with missingness as follows:
            1. Filter out all rows who have missing values on the **outcome** you will predict in your regression model.
            2. For predictor variables you plan to use, you will use simple imputation to deal with missingness.
        - We will discuss simple imputation strategies for the project before Thanksgiving.
        - Many (if not most) of you will also need to deal with other data management issues (like, for instance, turning a quantitative response into a categorical one, or calculating a summary like BMI from height and weight) in your project study 1 analyses.
    - Some items were planned to have 0-100 responses, but the survey asks you to respond on a 0-10 scale. Dr. Love will fuzz up your results by adding noise so that the resulting scale is 0-100. How?
        - Multiply your response (0-10) by 10, obtaining a value between 0 and 100, and call that **a**.
        - Randomly draw an integer from a uniform distribution (probably on [-8, 8], but we may change that) and call that **b**. 
        - **a + b** is the new response, but could fall anywhere in [-8, 108], so any values below 0 will be listed as 0 and any values above 100 will be listed as 100 in the data you will receive and analyze.

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

## Registering for Courses This Spring

- If you are planning to take 432, no problem. I will permit you in as soon as the registrar asks me to do so. I hope you all will join us - it's definitely the better of the two courses (431 and 432) if past students are to be believed, but that's a biased sample.
- If you are interested in taking 500 (Observational Studies) this Spring at the same time as 432, then we should talk. Generally, it's not recommended, and if you can sensibly wait a year to let the 432 ideas wash over you first, you'll be much happier. But if it's "now or never" for 500 in your case, I want to be sure you enter the course with your eyes open, and I'll want to know a bit more about your background than I do now, so that requires a 10-15 minute meeting in person. Email me with your availability on Tuesdays/Thursdays and we'll get that scheduled. Last year's [500 syllabus is available](https://thomaselove.github.io/500-syllabus/) but some things about the course are changing, substantially.

## I gave a talk at noon today about Better Health Partnership

If you're interested, the materials for the talk are at https://github.com/THOMASELOVE/mph-2018-10-30

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


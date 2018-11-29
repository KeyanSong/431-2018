# 431 Fall 2018 Class 24: 2018-11-29

## Today's Materials

- The slides for Class 24 are now available [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class24/431_class-24-slides_2018.pdf) and [in R Markdown](https://github.com/THOMASELOVE/THOMASELOVE/431-2018/master/slides/class24/431_class-24-slides_2018.Rmd).
- Class 24 audio files will be posted after class.

## Homework 8

- [Homework 8](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework8) is due at noon on Friday 2018-11-30. Dr. Love posted a hint for Question 6 and some specifications on how we'll grade the essay in Question 1 to the [revised instructions for Homework 8](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework8/431-2018-hw8.md) on 2018-11-17.
- **HINT** A student asked about the `betaplasma` variable in Homework 8, specifically noticing that one of the observations is 0, which is implausible, and troubling from a transformation perspective, since that is the outcome. Any of the following four approaches is OK with us:
    1. Drop the observation with `betaplasma` = 0, which is subject ID `S-1065`, I believe.
    2. Keep the observation with `betaplasma` = 0 but add 1 to all of the `betaplasma` values before considering transformations.
    3. Impute a new, more plausible, `betaplasma` value for the observation with `betaplasma` = 0. If you do this, we suggest you replace the `0` with the new value `10`.
    4. Keep the observation with `betaplasma` = 0 but put it in the test set, rather than the training set, so that it doesn't come into play when you are making a transformation decision. I did this with a split into 240 observations in the training set using the seed `431008`.

## Minute Paper Feedback is at http://bit.ly/431-2018-minute23-response

Please take a look. I separated the comments into Project Things and Everything Else. About 3/4 of the class seems to feel like they are in good shape (6 or higher on the 1-10 scale) on both Project 1 and Project 2, and that's great.

## Project Task F

Almost everyone is done, and that's great. You're done if you have an OK from me on Canvas, and a non-zero grade there.

### Some common issues I saw in Task F

1. **Binary Variables with 1/2 coding and Don't Know/Refused** If you have a variable like "Ever told you had a heart attack?" with a Yes/No response, you may find it is coded as 1 = Yes, 2 = No, and perhaps 7 = Don't Know, 9 = Refused, etc. What to do?
    - For **any** variable, treat Don't Know, Refused as missing values - convert them all to NA.
        - `dataset <- dataset %>% mutate(myvar = fct_recode(factor(myvar), NULL = "7", NULL = "9"))`
    - Change the coding of 1 = Yes, 2 = No. You have two options. You could make the values Yes and No.
        - `dataset <- dataset %>% mutate(myvar = fct_recode(factor(myvar), "Yes" = "1", "No" = "2"))` 
    - Or you could or convert the 1-2 coding to 1-0. Note that if X = 1 for yes and 2 for No, then 2-X will be 1 for yes, 0 for no.
        - `dataset <- dataset %>% mutate(myvar = 2 - myvar)`
    - 1/0 is a perfectly reasonable choice for a variable if Yes = 1 and No = 0.
    - If you have a variable like `sex`, you should have a better name for it if you're turning it into a 1/0 variable, for instance:
        - `dataset <- dataset %>% mutate(male = 2 - sex)` if `sex` is 1 for Male and 2 for Female, so that male = 1 for Male, = 0 for female.
2. **If you can, include a meaningful name as a variable in your data.** For example, if your rows describe countries, have a variable called "Country" - even though you will not use this as a predictor, it's very helpful for identifying outliers, etc.
3. Suppose you're studying the number of cigarettes a person smokes, and the survey results have some people who answered per week, and others who answered per month. You can assume a month is four weeks, and convert the results, so that 10 per week = 40 per month, so that you can combine things.
4. If you have a time variable, convert it to minutes (instead of hours and minutes - so that our class is 75 minutes long, rather than 1:15 long) to include it in models. Same idea for height if you have it in feet and inches, convert it to just inches (I am 75 inches, not 6 feet 3 inches.)
5. If you have a variable with more than a few categories (certainly more than 6), then strongly consider collapsing it to a smaller number of categories. Income is a particular issue. Suppose you have 20 income categories, described as, for example: 1 = < $10,000, 2 = 10,000 - 14,999, 3 = 15,000 - 19,999 etc.
    - One option is to make this a factor, but collapse down to categories that place the data into Low, Middle and High groups of roughly equal size. Usually, that's what I would do in a 431 project.
    - Another approach would be to select a random value within the specified range for each subject, and turn the variable into a quantitative one. There's a little more work to do this, but it does produce a quantitative estimate, and if you code it so that by changing a set.seed you get a new set of values, that can help with robustness checks. Something to consider in 432.

## Remaining Deliverables

After Homework 8, the remaining deadlines for the course are:
- The Minute Paper after Class 25 will be posted on Tuesday and due at noon Wednesday 2018-12-05.
- Quiz 2 will be released to you by noon on Friday, 2018-12-07.
- The [Project Presentation (Task H) Schedule](http://bit.ly/431-2018-project-schedule) specifies your time and date (12-10, 12-11 or 12-13).
- Quiz 2 is due on Tuesday 2018-12-11 at noon.
- Project Task G (the Portfolio) is due Thursday 2018-12-13 at noon, regardless of when you give your presentation.
- The [Homework Grading Appeals form](https://goo.gl/forms/G4ZZ1Fge1ZkQVKzy2) is also due Thursday 2018-12-13 at noon, if you want to make an appeal. See the last section of the [Syllabus](https://thomaselove.github.io/2018-431-syllabus/) for more details.
- After you give your presentation, we hope you will fill out a [Course Evaluation](https://webapps.case.edu/courseevals/) from CWRU by their 2018-12-19 deadline.

## Getting Help

- **Office Hours** TA office hours continue through Friday 2018-12-07. `431-help` will be open until I finish with projects on Thursday 2017-12-13. If you need to meet with a TA outside of office hours, arrange that through 431-help.
- If you are having trouble with R, and asking for help at 431-help, we need to first replicate your problem in order to solve it. So...
    1. Send your **entire** R Markdown file. All of it. Not pieces of it. All of it.
    2. Send a **screenshot** of the error message you are receiving, AND specify the line number where things break down if you can in your email. Or ask a specific and detailed question - as specific and detailed as you can make it.
    3. If this is about "your data" **send the data** set(s) that your R Markdown calls. If this is about the class survey data, we have that. But we (431-help) don't have your data.
    4. Please don't wait until you've been struggling with a problem so long that you feel frustrated or feel the need to tell us how long that's been to garner our sympathy. Struggle for 15 minutes with the demonstration files, then Google or search the course notes for at most another 15 minutes, then email us, is a reasonable workflow. Coding is hard enough with help.
    5. **Don't wait** until the last day. If you need instant help, we can rarely provide that, and never when you need it most, as it turns out. Somehow, the world will conspire to guarantee that we are  unavailable at the exact moment when you need an incredibly fast response. So don't need one. I warn you that I am unavailable on the evenings of Mon 12-10 and Tue 12-11.

## Highlights from *The Signal and the Noise*

I wanted to say a little about Chapter 9 (Rage Against the Machines), which is about computer chess. 

- Chess is all over the news, thanks to the dramatics in London over the past few weeks, where Magnus Carlsen retained his World Chess Championship. Oliver Roeder has been all over the story [in a series of articles at FiveThirtyEight](https://fivethirtyeight.com/tag/chess/).
- I found the material about how computers "think" to be particularly interesting here, although I think the most general takeaway I can give you from the chapter has to do with the general belief that if you see something really surprising from a prediction model or forecasting engine, you should go in with a strong prior that you've got a "bug".
- Jonah Sinick, in summarizing his thoughts on the chapter, [had this nice comment](https://www.lesswrong.com/posts/rGj2K8vu5qQCTWCar/some-highlights-from-nate-silver-s-the-signal-and-the-noise):

> Our use of prediction heuristics makes us vulnerable to opponents who are aware of the heuristics that we're using and who can therefore act in unexpected ways that we're not prepared for.

- Finally, perhaps you know something about Amazon's [Mechanical Turk](https://www.mturk.com/)? If not, you might be interested.

## Visualization of the Day

[Why Do People Visit the Emergency Room?](https://flowingdata.com/2016/02/09/why-people-visit-the-emergency-room/) by Nathan Yau again.

## Today's Main Example

Today's main example uses a new data set I've built including information from several parts of the [NHANES National Youth Fitness Survey](https://www.cdc.gov/nchs/nnyfs/index.htm), which was conducted in 2012. Back in Part A, we studied a different data set from the same source, and the data are also discussed in [Chapter 7 of the Course Notes](https://thomaselove.github.io/2018-431-book/NYFS-Study.html).

## One Last Thing

- David Robinson has a [great YouTube series of Tidy Tuesday screencasts](https://www.youtube.com/channel/UCeiiqmVK07qhY-wvg3IZiZQ) and I'll also provide [the link to the Tidy Tuesday project](https://github.com/rfordatascience/tidytuesday). Watch a real data scientist at work on an interesting data set he's never seen before.

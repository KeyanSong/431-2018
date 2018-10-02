# 431 Fall 2018 Class 12: 2018-10-04

## Today's Materials

- The slides are now available [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class12/431_class-12-slides_2018.pdf) and [in R Markdown](https://raw.githubusercontent.com/THOMASELOVE/431-2018/master/slides/class12/431_class-12-slides_2018.Rmd).
- Class 12 audio files will be posted above as soon as they are available.

## The Quiz is coming today

[Quiz 1](https://github.com/THOMASELOVE/431-2018/tree/master/quizzes) will be released to you by noon Friday 2018-10-05 and is due at 7 PM on Monday 2018-10-08 (Columbus Day). Note the change to **7 PM** instead of noon for the deadline. This means 7 PM on the nose, and not 8 PM, or even 7:01 PM. 

- We will post the link for Quiz 1 at the Quizzes page, and also right here, in this space.

## Coming Soon (or soonish)

1. Finish reading Leek's *Elements of Data Analytic Style* by 2018-10-11.
2. [Project Task A and Task B](https://thomaselove.github.io/431-2018-project/) are due at noon on 2018-10-12. 
3. You should now have read through Chapter 5 of Silver's *The Signal and the Noise*. By 2018-10-24, we'll expect you to have read through Chapter 11.
4. [Homework 5](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework5) is due 2018-10-19.
5. [Project Task C and Task D](https://thomaselove.github.io/431-2018-project/) are due at noon on 2018-10-23.

## General Announcements

1. Homework 4 Grades and Rubric will be posted soon.

2. Thanks to those of you who completed the [Minute Paper after Class 11](http://bit.ly/431-2018-minute11). Response is forthcoming.

3. Links from today's class:

- We'll start today's main work with a close look at the FiveThirtyEight [House Forecasting Model](https://projects.fivethirtyeight.com/2018-midterm-election-forecast/house/) for the upcoming U.S. Election.
    - If you are interested in this stuff, you will probably like the [FiveThirtyEight Politics podcast](https://fivethirtyeight.com/tag/politics-podcast/), especially its "Model Talk" episodes, like [Our Forecast Is 7,000 Lines Of Code](https://fivethirtyeight.com/features/politics-podcast-our-forecast-is-7000-lines-of-code/) from 2018-09-20.
- For more on `dplyr` and its key verbs, you should be reading Wickham and Grolemund's [R for Data Science](http://r4ds.had.co.nz/)
- The `printer.csv` data set used in today's example called "The Printer Case" is available above, and on the Data and Code page.
- The PDF version of "The Printer Case" is also available above.

# One Last Thing

# The remaining material is Repeated from Class 11's README

## A Promotional Announcement 
    
A few folks from the class came to see me in **Sweeney Todd** this weekend. Thank you for doing that. If you're interested, the show runs for the next two weekends on Friday and Saturday evenings and Sunday afternoons, and tickets are available at https://www.eventbrite.com/e/sweeney-todd-tickets-37253162211. We expect sellouts for the evening performances, so if you're interested, we strongly recommend you buy your tickets in advance.

## Project Tasks A and B reminders and comments (repeated from Class 11 README)

- [Task A](https://thomaselove.github.io/431-2018-project/taskA.html) requires your group to:
    - [develop and propose 2-3 research questions for Study 1](https://thomaselove.github.io/431-2018-project/taskA.html#research-questions) (the class survey)
        - Remember that we attempted a first pass at this in the brainstorming activity in Class 10. Results below.
    - [propose 6-10 "homemade" survey questions for Study 1](https://thomaselove.github.io/431-2018-project/taskA.html#specifying-survey-questions) that relate to your research questions, and
        - Remember that we attempted a first pass at this in the brainstorming activity in Class 10. Results below.
    - [propose a "scale" for Study 1](https://thomaselove.github.io/431-2018-project/taskA.html#specifying-a-scale) that also relates to your research questions
        - One past group identified a set of locations in Northeast Ohio that people might enjoy, and asked people to check a box whether or not they'd been to each location. This was nice, and we may include it again this year. The summary for the scale was simply a count of the number of locations each person had visited (actually, this led to a categorical outcome, as well.) You can find this scale as item 13 in [the 2016 survey](https://github.com/THOMASELOVE/431-2018-project/blob/master/oldsurveys/2016_431_class_survey.pdf).
        - Another past group adapted a Ten-Item Personality Inventory (which you'll find as items 70a through 70j in [the 2016 survey](https://github.com/THOMASELOVE/431-2018-project/blob/master/oldsurveys/2016_431_class_survey.pdf). Here's their [source for the original TIPI scale](https://gosling.psy.utexas.edu/scales-weve-developed/ten-item-personality-measure-tipi/). This scale led to the calculation of five different outcomes, actually, including measures of extroversion and of agreeableness.
    - **Note** You will have a 20-30 minute work session on the Group part of Task A in class on Thursday 2018-10-05.
- [Task A](https://thomaselove.github.io/431-2018-project/taskA.html) also requires you, as an individual, to:
    - develop and propose a meaningful summary of your ideas and research question for Study 2 (Your Data).
    - identify and present a detailed description of a data set that is likely to lead to an answer to the research question you proposed for Study 2, and that is appropriate for use in the project.
- [Task B](https://thomaselove.github.io/431-2018-project/taskB.html) simply requires you to complete the Google Form for project presentation sign up that is linked at http://bit.ly/431-2018-project-signup-taskB
    
### The Brainstorming Activity, from Class 10

Largely Unedited Results of the [Group Study 1 Brainstorming Activity From Class 10](http://bit.ly/431-2018-class10-brainstorm-feedback) are available now at http://bit.ly/431-2018-class10-brainstorm-feedback.

- The key takeaway is that none of the ten groups successfully wrote a research question, so I'll need to provide more guidance on that. 
- At the moment, what I have for you is contained in [section 2.2.1 (Research Questions)](https://thomaselove.github.io/431-2018-project/taskA.html#research-questions) of the Course Project Instructions. I can also provide several examples of good research questions written last year by student groups, both for Study 1 and Study 2.
    
### A Few Examples of Research Questions That Worked Out Well in the Past

1. For Study 1, your research questions will need to compare two or more exposure groups on a quantitative outcome (in one case) and on a categorical outcome (in another case). 
    - "Do messy people tend to have higher levels of self-described creativity than organized people?"
    - "Is whether you voted in the last presidential election strongly associated with your level of interest in the current election?"
    - "Does being in a committed romantic relationship result in higher self-esteem compared to not being in a committed romantic relationship?"
    - "Do conscientious people spend more time every week engaged in activities, such as exercise, thought to promote health and well-being compared to others?"
    - "Do graduate students who routinely pack their lunch have a lower BMI than graduate students who routinely purchase their lunch?"
    - "Do individuals who spend a lot of time on social media each day have more or less social anxiety than those who do not?" 
2. For Study 2, your research questions will need to fit within the confines of a regression model, where a quantitative outcome is predicted using a series of at least four predictor variables. In many cases, a key predictor will be of primary interest, with other predictors serving to "adjust" away noise and generate fairer comparisons.
    - "Is the presence of cardiovascular risk factors, specifically elevated hemoglobin A1c, predictive of cognitive impairment as defined by the Digit Symbol Substitution Test in patients over the age of 60 years, after adjusting for age, education, and depression?"
    - "What is the effect of thyroid dysfunction on LDL level after adjusting for age, sex, and level of physical activity in the population of patients at XXXXXXXX location who are 40 years-old and above?"
    - "Do conscientiousness and openness predict more conservative or liberal attitudes about government spending and whether and how much wasteful spending exists, after accounting for age, income and professional status?"
    - "Does overweight or obesity (defined by body mass index) predict insulin resistance (measured by the homeostasis model assessment of insulin resistance (HOMA-IR)) in young adults with first-time acute coronary syndrome after adjusting for age, sex, race/ethnicity and severity of (several comorbid conditions)?"


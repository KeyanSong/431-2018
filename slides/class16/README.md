# 431 Fall 2018 Class 16: 2018-10-25

**Welcome back!**

## Today's Materials

- The slides are available [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class16/431_class-16-slides_2018.pdf) and [in R Markdown](https://github.com/THOMASELOVE/THOMASELOVE/431-2018/master/slides/class16/431_class-16-slides_2018.Rmd), above.
- Class 16 audio files will be posted above after class.

## Deliverables and Scheduling: The [Course Calendar](https://github.com/THOMASELOVE/431-2018/blob/master/calendar.md) is now correct.

Many changes have happened and the [Course Calendar](https://github.com/THOMASELOVE/431-2018/blob/master/calendar.md) is the final word again. *Not all changes are currently captured in the rest of the web site, but I'm working on that. If you see something confusing, please let me know.*

- The main goal of the changes is to make it so that the work is spread out more effectively through the rest of the term, and so that you have a more regular schedule of activities. You have something due this Friday, and something else due on each of the next three Fridays. That gets us up to Thanksgiving break. 

In short, here's what's happened:

1. **Quizzes**. There will now be only two Quizzes this semester, instead of the originally planned three.
    - You've already taken Quiz 1. 
        - Those who were [assigned some extra work](https://github.com/THOMASELOVE/431-2018/blob/master/quizzes/quiz01/extra.md) remember to get that in by tomorrow (2018-10-26) at noon.
    - Quiz 2 will cover the entire course, and will be in your hands by noon on Friday 2018-12-07, and will be due at noon on Tuesday 2018-12-11, giving you an extra 24 hours over the original plan. Remember, Project Presentations begin on Monday 2018-12-10.
    - Quiz 2 will be about the same length as Quiz 1, in terms of the length of time we expect it to take you to complete, and it will use the same technology (Google Form) for you to submit your work.
    - Your overall Quiz grade in the course will be calculated in two ways. Whichever yields the higher score will be the grade I incorporate into the process for determining your final Course grade.
        - weighing Quiz 1 as 40% of your Quiz grade, and Quiz 2 as 60% of your Quiz grade, or
        - weighing Quiz 1 as 33% of your Quiz grade, and Quiz 2 as 67% of your Quiz grade.

2. **Homework**. There will still be a total of 8 homework assignments this semester.
    - [Homework 5](https://github.com/THOMASELOVE/431-2018/tree/master/homework) is still due tomorrow (Friday 2018-10-26) at noon. It is now the only thing due tomorrow. See below for some useful hints regarding this Homework.
    - [Homework 6](https://github.com/THOMASELOVE/431-2018/tree/master/homework) will be revised (shortened) a bit soon, and that new version will be due on Friday 2018-11-09 at noon.
    - [Homework 7](https://github.com/THOMASELOVE/431-2018/tree/master/homework) will appear online soon, and will be due on Friday 2018-11-16 at noon.
    - [Homework 8](https://github.com/THOMASELOVE/431-2018/tree/master/homework) will appear online soon, and will be due on Friday 2018-11-30 at noon.
    - [Homework Regrading Requests](https://goo.gl/forms/G4ZZ1Fge1ZkQVKzy2) are unchanged, and still due at noon on Thursday 2018-12-13.

3. **Reading**. 
    - You will need to finish reading Nate Silver's *The Signal and the Noise* by November 27 (our first class after Thanksgiving), but we won't discuss the book in class in any substantial way before then, although several essays in homework assignments between now and then require you to have read various chapters in the book. 
    - By now, you should have already finished reading Jeff Leek's *Elements of Data Analytic Style*.

4. **Minute Papers**
    - Minute Papers return next week. 
    - I anticipate that we'll have 4-5 more Minute Papers over the course of the semester, to be due at noon on Wednesday **10-31**, **11-07**, **11-14**, *11-28 (maybe)* and **12-05**. Each, as always, will be provided to you the day before they are due.

5. **Project**.
    - The Course Project Survey will go live by noon on Monday 2018-10-29. It will be posted to http://bit.ly/431-2018-survey.
    - [Project Task D](https://thomaselove.github.io/431-2018-project/taskD.html) (the Survey Comparison Plan form) **and** [Project Task E](https://thomaselove.github.io/431-2018-project/taskE.html) (actually Completing the Survey) will each be due at noon on Friday 2018-11-02.
        - The Task D form is at http://bit.ly/431-2018-survey-comparison-plan-taskD. 
            - You'll need to identify items for the survey based on their final numbers, as posted in the actual survey at http://bit.ly/431-2018-survey. To the extent possible, we will use the same numbers as in the [Draft Survey](http://bit.ly/431-2018-draft-project-survey).
        - Task E requires you to fill out the actual Course Survey, which will appear before noon on Monday 2018-10-29 at http://bit.ly/431-2018-survey. 
            - This will take a while, since there are about 150 items on the Survey, and you need to answer them all.
            - Like a quiz, it will be possible to save your work partway through and return to the Survey. It is not important to take the entire survey in one sitting.
    - [Project Task F](https://thomaselove.github.io/431-2018-project/taskF.html) (Sharing your Study 2 Data) will be due at noon on 2018-11-28 (Wednesday after Thanksgiving).
    - The Project Portfolio (Task G) and Project Presentation (Task H) are not changed in any way.
        - The Schedule of Project Presentations is at http://bit.ly/431-2018-project-schedule. 
        - The Project Portfolio is still due for all students at noon on Thursday 2018-12-13.

## Hint 1 for Homework 5 (and also for Project Study 1) / On the value of Pairing Samples

Questions 7 and 8 involve two studies. One of those studies uses paired (or matched) samples (as we discussed in Class 15), the other independent samples (which we'll discuss today) to compare two population means. 

- The study that uses paired samples has a clear link between the samples so that each observation in one group is uniquely linked to a single observation in the other group, so that taking paired differences makes sense. This is determined even before you collect the actual data - it is a characteristic of the study design, not the observed data.
- When assessing the study that uses paired samples, you'll need to address question g, which asks about whether pairing helped to reduce nuisance variation. To help quantify your answer here, you're going to want to understand the correlation (the Pearson correlation) between the samples. 
    - We measure the amount of variation accounted for by the pairing as a proportion using R-squared, you'll recall. A large value of R-squared will indicate a situation where the pairing helps a lot, and a small one will indicate that pairing only helps a little.
    - If the correlation *r* is small and positive, perhaps less than 0.2 or so, so that the *r-squared* value when predicting one sample given the other would also be quite small, then that would indicate that pairing will be of only minimal help in reducing nuisance variation. This would suggest that an analysis using paired samples (i.e. the appropriate analysis) would only be a little different from an analysis using independent samples (even though an independent samples analysis would not be correct.)
    - If the correlation is positive and large, the pairing will be more helpful, and the difference between the assessment of the difference in means obtained using the (correct) paired samples analysis and the (incorrect) independent samples analysis will likely be larger, as a result.
    - Regardless of the observed correlation coefficient, the decision about whether to pair the samples or not is made before any data are collected, based on the study's design (specifically whether the observations are in fact matched/paired by the way the data are collected.) As a result, even if the correlation turns out to be negative, if the samples are paired, that is how we'll analyze them.

## Hint 2 for Homework 5 (and also for your Project Study 1 or 2) / Wide vs. Long Data Formatting

You may find that your data in Homework 5 Question 7 or Question 8 isn't set up in exactly the format you wish it was. That is to say, you may have data that is in wide format when you wish it was in long format, or, conversely, that it is long when you wish it was wide. R has a solution for this within the tidyverse, and we will demonstrate the use today (in class) of the `gather` function to turn long data into wide and the `spread` function to turn wide data into long. 

- In addition to today's discussion in class, you probably want to look at the Tidy Data chapter of [R for Data Science](https://r4ds.had.co.nz/), in particular the section on [Spreading and Gathering](https://r4ds.had.co.nz/tidy-data.html#spreading-and-gathering).
- If you're having trouble remembering which function (gather or spread) does which operation, [you might consider this "spread butter and gather leaves" analogy](https://twitter.com/WeAreRLadies/status/1054742083607642112) from the good folks at @WeAreRLadies.

## Course Project Progress

- **Task A** (The Proposal). Almost everyone is done. 
    - Summaries of the project proposals [are available here](https://github.com/THOMASELOVE/431-2018-project/blob/master/OKtaskA.md). Please take a look at what your colleagues are doing, and make sure that my description of your proposal is accurate.
    - A few quick comments that I haven't (yet) had time to add to the instructions for next year.
        - I want to warn people away from hierarchical, multi-level data. That's not what we need.
        - I want to warn people away from Kaggle, and from the Pima Indians database and several other well-worn options.
        - I want to make NHANES use a more detailed thing, since a lot of people wind up there, and make some suggestions regarding good alternatives to NHANES.
        - I want to warn people away from assuming I know anything about wet lab biology work or genomics.
        - I want to better emphasize the key things that people need to provide me with, perhaps with a template for what the data description should look like. 
        - There's still confusion for too many people about what a quantitative outcome is.
        - I need to provide a "magic phrase" which will re-assure me about the sharability of, for example, data collected in a lab that is not available to the public.
        - I would like to tell you more about resources at CWRU and online to improve your writing.
        - I would like to make a checklist or rubric for the Study 2 proposal so you can self-evaluate.
- **Task B** is done. The [Schedule of Presentations is available here](http://bit.ly/431-2018-project-schedule)). 
- **Task C** (Survey Editing) is done.
    - The Draft Survey is posted at http://bit.ly/431-2018-draft-project-survey. We'll discuss the changes I've made, if we have time, but since I doubt we'll have time, the main thing is to poll you on seven specific issues.
        1. Does anyone have a good synonym for "politically engaged" we might use?
        2. In defining "red meat", does pork count? According to the FDA, yes, because it contains more myoglobin than chicken or fish.
        3. What does "using electronic media" entail? I think it means everything that you consume electronically - the internet, television, books, magazines, games, social media, whatever, including time spent on a computer and time spent on a tablet or phone.
        4. Is there anyone who cannot define their employment status as either (a) Not employed, (b) Employed part-time, (c) Employed full-time? 
        5. In determining whether you are employed FT/PT or not, would you count time spent in TA or GA activities for which you are not paid directly, but which are conditions of your continuing student status as employment activities?
        6. Would you count thesis activities you are required to do as part of your program but are not paid for as employment?
        7. Does anyone have a powerful objection to any of the new items on the [last page of the draft](http://bit.ly/431-2018-draft-project-survey) being added to the survey?
        
- Next up: **Task D** (Survey Comparison Plan) and **Task E** (Actually Doing the Survey) are each due next Friday 2018-11-02.
- **Study 2**: If your data set has more than 6,000 observations (after applying inclusion/exclusion filters and filtering to complete cases on the variables that you are considering for your model) I strongly encourage you to take a sample (probably at random) of 6,000 and then use 4,000 of those as the training sample for your modeling and the remaining 2,000 as a test sample.


## General Announcements

1. As of 2018-10-19, [Github now displays R Markdown files verbatim](https://yihui.name/en/2018/10/rmd-github/), without rendering them (imperfectly) into Markdown. This is actually good news. It should be easier to see the details of things like how chunk labels work, and you won't have to go to the raw version of the files to see what they should look like.

## Visualization of the Day

[How The Red Sox And Dodgers Made It To The World Series, In One Chart](https://fivethirtyeight.com/features/how-the-red-sox-and-dodgers-made-it-to-the-world-series-in-one-chart/) from Gus Wezerek and Sara Ziegler at FiveThirtyEight. 

![](https://fivethirtyeight.com/wp-content/uploads/2018/10/ziegler-wezerek_WSPATH_1023.png?w=1024)

Updated predictions for the World Series are [at this link](https://projects.fivethirtyeight.com/2018-mlb-predictions/?ex_cid=endlink).

## The Hardest-to-Look-At-Without-Screaming Picture of the Week

was clearly won by the [Harvard Business Review](https://hbr.org/2018/10/which-data-skills-do-you-actually-need-this-2x2-matrix-will-tell-you) in its example of how to plot data skills on a 2x2 learning matrix. To be fair, there's reason to think this is more of a communication problem than a real assessment of the issues involved.

![](https://hbr.org/resources/images/article_assets/2018/10/W181004_LITTLEWOOD_ANEXAMPLE-1.png). 

[Some of the comments](https://hbr.org/2018/10/which-data-skills-do-you-actually-need-this-2x2-matrix-will-tell-you#comment-section) are delightful, like this one from John Snyder. 

"Here's the gist of their 2x2 matrix:
Hard to learn but useful: BUZZWORDS!
Easy to learn and useful: OLD BUZZWORDS!
Hard to learn and not useful: Actual data analysis
Easy to learn and not useful: Boring but important"

A few of the many, many reactions that are littering my social media feeds:

- [Vicki Boykis](https://twitter.com/vboykis/status/1054408259149299712) "Everyone, it appears we have finally found it, the truly magical company where no data cleaning, statistics, or data warehousing need to ever occur. Someone please take me to this Paradise."
- [Stuart Buck](https://twitter.com/StuartBuck1/status/1054469995776884737) "This Harvard Business Review chart seems to have been made by someone who didn't know what most of the terms meant."
- [Daniela Witten](https://twitter.com/daniela_witten/status/1054537089503637509) "Whenever someone makes a plot like this, a kitten dies."
- [Ladbroke](https://twitter.com/ladbroke/status/1054562099412852736) "I'm surprised blockchain isn't on there, frankly."
- [Kim Weeden](https://twitter.com/WeedenKim/status/1054520735711027200) "Spreadsheeting: the business alternative to excelling."
- [David Mimno](http://mimno.org/Matrix/) allows you to generate your own example of plotting random points on a 2x2 learning matrix.


## One Last Thing

- Nate Silver (2018-10-19) on "Election Update: Democrats’ Unprecedented Fundraising Edge Is Scary For Republicans ... And Our Model" is a great read [over at FiveThirtyEight](https://fivethirtyeight.com/features/election-update-the-democrats-unprecedented-fundraising-edge-is-scary-for-republicans-and-for-our-model/).
    - Here's the money quote: "... (In the House races, the) Democrat has raised an average of 65 percent of the money in districts rated as competitive (meaning, rated as "toss-up", "leaning" or "likely") by the Cook Political Report. In all previous years in our database, **no party had averaged more than 56 percent** of the money in these competitive districts."
    - That link includes an excellent two-minute video looking at the Senate forecast, and Nevada in particular.

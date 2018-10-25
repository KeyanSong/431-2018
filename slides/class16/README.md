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
    - You've all completed Quiz 1 already. Those of you who were assigned some extra work need to get that in by 
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

3. **Reading**. 
    - You will need to finish reading Nate Silver's *The Signal and the Noise* by November 27 (our first class after Thanksgiving), but we won't discuss the book in class in any substantial way before then, although several essays in homework assignments between now and then require you to have read various chapters in the book. 
    - By now, you should have already finished reading Jeff Leek's *Elements of Data Analytic Style*.

4. **Minute Papers**

Minute Papers return next week. I anticipate at least four more Minute Papers over the course of the semester, to be due at noon on Wednesday 10-31, 11-07, 11-14, 11-28 (maybe) and 12-05. Each, as always, will be provided to you the day before they are due.

5. **Project**.
    - The Course Project Survey will go live on Monday 2018-10-29. It will be posted to http://bit.ly/431-2018-survey when available.
    - [Project Task D](https://thomaselove.github.io/431-2018-project/taskD.html) (the Survey Comparison Plan form) **and** [Project Task E](https://thomaselove.github.io/431-2018-project/taskE.html) (actually Completing the Survey) will now be due at the same time, which is noon on Friday 2018-11-02.
        - The Task D form is at http://bit.ly/431-2018-survey-comparison-plan-taskD. 
            - You'll need to identify items for the survey based on their final numbers, which will be available when the actual survey is posted at http://bit.ly/431-2018-survey. To the extent that it is possible, we will keep the numbers the same as those used in the [Draft Survey](http://bit.ly/431-2018-draft-project-survey).
        - Task E will require you to fill out the actual Course Survey, which, again, will appear on Monday 2018-10-29 at http://bit.ly/431-2018-survey. This will take a while, since there are about 150 items on the Survey, and you will need to complete them all.
    - [Project Task F](https://thomaselove.github.io/431-2018-project/taskF.html) (Sharing your Study 2 Data) will be due at noon on Wednesday after Thanksgiving, specifically 2018-11-28.
    - The Project Portfolio (Task G) and Project Presentation (Task H) are not changed in any way.
        - The Schedule of Project Presentations is at http://bit.ly/431-2018-project-schedule. Your presentation is on December 10, 11 or 13, as originally scheduled.
        - The Project Portfolio is still due for all students at noon on 2018-12-13.


## A Hint for Homework 5 / On the value of Pairing Samples

Questions 7 and 8 involve two studies. One of those studies uses paired (or matched) samples (as we discussed in Class 15), the other independent samples (which we'll discuss today) to compare two population means. 

- The study that uses paired samples has a clear link between the samples so that each observation in one group is uniquely linked to a single observation in the other group, so that taking paired differences makes sense. This is determined even before you collect the actual data - it is a characteristic of the study design, not the observed data.
- When assessing the study that uses paired samples, you'll need to address question g, which asks about whether pairing helped to reduce nuisance variation. To help quantify your answer here, you're going to want to understand the correlation (the Pearson correlation) between the samples. 
    - We measure the amount of variation accounted for by the pairing as a proportion using R-squared, you'll recall. A large value of R-squared will indicate a situation where the pairing helps a lot, and a small one will indicate that pairing only helps a little.
    - If the correlation *r* is small and positive, perhaps less than 0.2 or so, so that the *r-squared* value when predicting one sample given the other would also be quite small, then that would indicate that pairing will be of only minimal help in reducing nuisance variation. This would suggest that an analysis using paired samples (i.e. the appropriate analysis) would only be a little different from an analysis using independent samples (even though an independent samples analysis would not be correct.)
    - If the correlation is positive and large, the pairing will be more helpful, and the difference between the assessment of the difference in means obtained using the (correct) paired samples analysis and the (incorrect) independent samples analysis will likely be larger, as a result.
    - Regardless of the observed correlation coefficient, the decision about whether to pair the samples or not is made before any data are collected, based on the study's design (specifically whether the observations are in fact matched/paired by the way the data are collected.) As a result, even if the correlation turns out to be negative, if the samples are paired, that is how we'll analyze them.

## Progress on the Course Project

Everyone has completed Project Task B. Almost everyone has completed Project Tasks A and C. Thank you.

- The Draft Survey is posted at http://bit.ly/431-2018-draft-project-survey. We'll discuss the changes I've made to this, along with some specific issues we need to make a decision on, today.

## General Announcements

1. As of 2018-10-19, [Github now displays R Markdown files verbatim](https://yihui.name/en/2018/10/rmd-github/), without rendering them (imperfectly) into Markdown. This is actually good news. It should be easier to see the details of things like how chunk labels work, and you won't have to go to the raw version of the files to see what they should look like.


# 431 Fall 2018 Class 21: 2018-11-13

## Today's Materials

- The slides for Class 21 are available [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class21/431_class-21-slides_2018.pdf) and [in R Markdown](https://github.com/THOMASELOVE/THOMASELOVE/431-2018/master/slides/class21/431_class-21-slides_2018.Rmd).
- Class 21 audio files will be posted as soon as they are available.

## Remaining Pre-Thanksgiving Deliverables

- The Minute Paper after Class 21 is at http://bit.ly/431-2018-minute21. Please complete it by noon on Wednesday 2018-11-14.
- [Homework 7](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework6/431-2018-hw7.md) is due to [Canvas](https://canvas.case.edu/) by noon on Friday 2018-11-16. There are 9 questions.
    - Before today's Class 21, you should have been able to do Questions 6-9.
    - After today's Class 21, you should be able to do all nine questions.

## Homework 6

- The answer sketch for HW 6 is now posted, [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework6/431-2018-hw6sketch.pdf) and [R Markdown](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework6/431-2018-hw6sketch.Rmd).
- The rubric and grades should be available by 2018-11-15.

## Homework 8 will be posted ASAP. It is due 2018-11-30.

- You'll find it at https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework8 as soon as I post it.

## The International Prize in Statistics

Occasionally described as the equivalent of the Nobel Prize, the [International Prize in Statistics](http://statprize.org/) recognizes a major achievement in the field of statistics, and this year's prize was awarded in recognition of Brad Efron, and the bootstrap. Quoting the press release from the American Statistical Association:

> This novel method for assessing the uncertainty of scientific results, developed by Efron in 1977, has transformed our ability to use and understand data and had a major impact on science. 

### The Bootstrap, Simplified (from [statprize.org](http://statprize.org/))

> Suppose you want to know the average household income in your city. You can't afford a complete census, so you randomly sample 100 households, record the 100 incomes and take their average, say $29,308. That sounds precise, but you would like some estimate of how accurate it really is. A straightforward, but impractical, approach would be to take several more random samples of 100 households, compute the average each time and see how much the averages differed from each other.

> The bootstrap lets you approximate this impractical approach using only the original sample's data. A bootstrap data set is a random sample of size 100 drawn from the original 100 incomes. You can imagine writing each of the original incomes on a slip of paper, putting the slips into a hat and randomly drawing a slip out. Record the number, put the slip back into the hat and repeat this process 99 more times. The result would be a bootstrap data set, and we can make as many bootstrap data sets as we wish, each time taking their average. Let's say we do 250 of them, giving 250 bootstrap averages. The variability of the 250 averages is the bootstrap estimate of accuracy for the original estimate $29,308.

> The same idea can be applied to find the accuracy of any statistic, say the median income instead of the average or, perhaps, something much more complicated, which makes the bootstrap ideal for the often elaborate statistical methods of modern scientific practice.

## Project Updates

### Study 1

Remaining steps I would take (were I you) for Project Study 1 are:

1. Make decisions about how you will revise each of your six Analyses. Follow Dr. Love's [suggestions and comments on your Survey Comparison Plan materials from Task D](https://github.com/THOMASELOVE/431-2018-project/blob/master/survey-results/plan-comments.md), and then be sure that for each Analysis where you've changed something, you verify the things specified for the affected Analyses in the [section on Getting the Revisions Right](https://github.com/THOMASELOVE/431-2018-project/blob/master/survey-results/plan-comments.md#getting-the-revisions-right). 

2. Begin your actual work with the [Study 1 Demonstration Project](https://github.com/THOMASELOVE/431-2018-project/tree/master/demo_study1), which I **updated** slightly on 2018-11-12. Open the R Markdown file, and begin editing it. Your goal should be to have achieved the elements in Sections 1-5 of the [Study 1 Demonstration Project](https://github.com/THOMASELOVE/431-2018-project/tree/master/demo_study1) as soon as possible, and have a final, clean codebook. Once you've done that, the actual analyses in Sections 6-12 are pretty straightforward.

    - Use a template like the one used in the [Study 1 Demonstration Project](https://github.com/THOMASELOVE/431-2018-project/tree/master/demo_study1). The specific template I use is called `readthedown` format. 
    - Other template options include the `material` format, and the `html_clean` format, also available in the `rmdformats` package, and [described at this Github site](https://github.com/juba/rmdformats). 
    - I recommend `readthedown`, personally, because I like some of its idiosyncracies, and I have had less trouble working with it than the others in my own work. I use `readthedown` in both the Study 1 and Study 2 demonstration projects, and suggest you use it in both of your projects that you submit in the portfolio for Task G. There are better tools, but I think `readthedown` is a good place to be at the end of 431. (I'm aiming for us all to be building [Radix websites](https://rstudio.github.io/radix/) in 432, I think.)
    - The key element of these approaches is the use of an attractively formatted (and dynamic) table of contents to help organize what we want to see, and to facilitate jumping around as I ask questions during your presentation, and during my evaluation of your work.

3. You need to replace the data work throughout the [Study 1 Demonstration Project](https://github.com/THOMASELOVE/431-2018-project/tree/master/demo_study1) with the details from our 2018 data and your planned analyses.

    - This includes (but is not limited to) the required merging and combination of all five data sets, [as discussed and demonstrated here](https://github.com/THOMASELOVE/431-2018-project/blob/master/survey-results/surv2018_combining-datasets.md). Everyone needs to combine all five data sets to complete the project, although you will prune down the variables to your specific analytic data set at the end of section 2 (from the [Study 1 Demonstration Project](https://github.com/THOMASELOVE/431-2018-project/tree/master/demo_study1)), and then work only with those variables in sections 3-12.
    - This also includes the use of simple imputation, to deal with missingness (if it exists) in the variables you have selected for your analyses. [Imputation instructions and a demonstration are available here](https://github.com/THOMASELOVE/431-2018-project/blob/master/survey-results/impute_example.md).

4. Review the **updated** [Task G](https://thomaselove.github.io/431-2018-project/taskG.html) and [Task H](https://thomaselove.github.io/431-2018-project/taskH.html) instructions to be sure that you have completed all necessary analyses for Project Study 1, and that you have a clear understanding of the things you'll need to do in your presentation regarding Study 1.

    - We covered all materials you would need to do Analyses 1, 4, 5 and 6 prior to Class 21.
    - During class 21, we will cover Analysis 2, and during class 22, we will cover Analysis 3.

#### Some Tips

1. **Naming Things** is hard. But don't make it harder on yourself by picking a very generic name (like `survey` for the data you will use. Even `sur431` is better than that, since `survey` is an important package name in R.
2. **Getting Started in the RIGHT WAY** The biggest problem people struggle with is that packages fight each other for function names (like `select`). To avoid this, load every package you plan to use before you load the tidyverse. 
3. This also means calling `source("Love-boost.R")` **prior** to the loading of packages, as opposed to after it, as I have now corrected the [Study 1 Demonstration Project](https://github.com/THOMASELOVE/431-2018-project/tree/master/demo_study1) to do. Be sure to make that change - **I will be looking to see that you have done this properly**. I expect most to begin section 2 of their Project with an initial setup that looks something like this...

```
## Load Love-boost then the packages
source("Love-boost.R")

library(knitr); library(rmdformats); library(magrittr)
library(skimr); library(Hmisc); library(Epi); library(vcd)
library(tidyverse) 

## Global options

options(max.print="75")
opts_chunk$set(comment=NA,
               message=FALSE,
               warning=FALSE)
opts_knit$set(width=75)

## Skim options (leave out histograms)

skimr::skim_with(numeric = list(hist = NULL),
                 integer = list(hist = NULL))
```

4. The other thing I will absolutely be looking for is whether or not you remember to change the name of your project and the author to you. If yours says "431 Project Study 1 Demonstration" or says that the author is "Thomas E. Love" change that **NOW** so that you don't forget. "431 Project Study 1" is a boring but reasonable name for your work. But "431 Project Study 1 Demonstration" flags you as someone who didn't pay attention to details. Don't be in that situation.
5. Finally, for heaven’s sake, **DO NOT** use my words included in the demonstration project in your project for either Study 1 or Study 2. Rewrite **everything** other than perhaps the headings to make it your own, and make it relevant to your situation. Do not repeat my instructions back at me.

### Study 2

1. Today we'll discuss the projects by people whose family names start with S-Z in the [Approved Project Proposals](https://github.com/THOMASELOVE/431-2018-project/blob/master/OKtaskA.md#s-v).

2. **The Demo Project is now available.** As of 2018-11-12, the [Project Study 2 Demonstration page](https://github.com/THOMASELOVE/431-2018-project/blob/master/demo_study2/README.md) is complete.  We will discuss the material on that page in Class 22. Get the R Markdown and HTML files that I created for the Study 2 project at http://bit.ly/431-2018-demo-study2.

3. Don't forget that [Task F](https://thomaselove.github.io/431-2018-project/taskF.html) (Sharing Study 2 Data), is due at noon on Wednesday 2018-11-28, after the Thanksgiving break.

## Like `favstats` from the `mosaic` package?

Then say hello to `inspect`. The `inspect` function (also within `mosaic`) provides a way to get results that are like `favstats` but for an entire data frame. It does one thing, but pretty well. I'll demonstrate today, and I've used it now in the just-completed [Project Study 2 Demonstration](https://github.com/THOMASELOVE/431-2018-project/blob/master/demo_study2/README.md).

## R Studio preview version is updated again

If you want to try out R Studio version 1.2.1114 (or later), you can do so by getting [the R Studio preview version](https://www.rstudio.com/products/rstudio/download/preview/). The main version is still 1.1.463, as of 2018-11-12. 

- 1.2 is exciting and [adds a lot of nice features](https://www.rstudio.com/products/rstudio/download/preview-release-notes/), exactly **NONE** of which you will need or use in 431.

## Visualization of the Day/Week/Month/Year/Milennium?

[A Timeline of Earth's Average Temperature, since the Last Ice Age Glaciation](https://xkcd.com/1732/) from [XKCD](https://xkcd.com/)

![](https://imgs.xkcd.com/comics/earth_temperature_timeline.png)

## One Last Thing: RYouWithMe, A New Resource from R-Ladies Sydney

[RYouWithMe](https://rladiessydney.org/ryouwithme) is a new series of online learning resources for using R, oriented towards R beginners and providing a solid foundation of R skills. Their [first "unit" - called Basic Basics](https://rladiessydney.org/post/2018/11/05/basicbasics/) is now available! It contains three lessons:

1. [An opinionated tour of RStudio](https://rladiessydney.org/post/2018/11/05/basicbasics-1/)
2. [Installing and loading packages](https://rladiessydney.org/post/2018/11/05/basicbasics-2/)
3. [Getting data into RStudio](https://rladiessydney.org/post/2018/11/05/basicbasics-3/)

There are plans to roll out four additional units, on data wrangling, visualization, the R language, and R Markdown, by the end of the year. If you find these helpful, let us know!

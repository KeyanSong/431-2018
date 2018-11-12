# 431 Fall 2018 Class 22: 2018-11-15

## Today's Materials

- The slides for Class 22 are available [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class22/431_class-22-slides_2018.pdf) and [in R Markdown](https://github.com/THOMASELOVE/THOMASELOVE/431-2018/master/slides/class22/431_class-22-slides_2018.Rmd).
- Class 22 audio files will be posted as soon as they are available.

## Remaining Pre-Thanksgiving Deliverables

- [Homework 7](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework6/431-2018-hw7.md) is due to [Canvas](https://canvas.case.edu/) by noon on Friday 2018-11-16. There are 9 questions, and you should be able to do them all.

## Coming ASAP

- Minute Paper after Class 21 results.
- Project Study 2 Demonstration
- Homework 8
- Thanksgiving Break

## Project Updates

### Study 1

Remaining steps I would take (were I you) for Project Study 1 are:

1. Make decisions about how you will revise each of your six Analyses. Follow Dr. Love's [suggestions and comments on your Survey Comparison Plan materials from Task D](https://github.com/THOMASELOVE/431-2018-project/blob/master/survey-results/plan-comments.md), and then be sure that for each Analysis where you've changed something, you verify the things specified for the affected Analyses in the [section on Getting the Revisions Right](https://github.com/THOMASELOVE/431-2018-project/blob/master/survey-results/plan-comments.md#getting-the-revisions-right). 

2. Begin your actual work with the [Study 1 Demonstration Project](https://github.com/THOMASELOVE/431-2018-project/tree/master/demo_study1). Open the R Markdown file, and begin editing it. Your goal should be to have achieved the elements in Sections 1-5 of the [Study 1 Demonstration Project](https://github.com/THOMASELOVE/431-2018-project/tree/master/demo_study1) as soon as possible, and have a final, clean codebook. Once you've done that, the actual analyses in sections 6-12 are pretty straightforward.

    - Use the template I used in the [Study 1 Demonstration Project](https://github.com/THOMASELOVE/431-2018-project/tree/master/demo_study1), or something similar that also provides a dynamic table of contents which is visible at all times.

3. You need to replace the data work throughout the [Study 1 Demonstration Project](https://github.com/THOMASELOVE/431-2018-project/tree/master/demo_study1) with the details from our 2018 data and your planned analyses.

    - This includes (but is not limited to):the required merging and combination of all five data sets, [as discussed and demonstrated here](https://github.com/THOMASELOVE/431-2018-project/blob/master/survey-results/surv2018_combining-datasets.md). Everyone needs to combine all five data sets to complete the project, although you will prune down the variables to your specific analytic data set at the end of section 2 (from the [Study 1 Demonstration Project](https://github.com/THOMASELOVE/431-2018-project/tree/master/demo_study1)), and then work only with those variables in sections 3-12.
    - This also includes the use of simple imputation, to deal with missingness (if it exists) in the variables you have selected for your analyses. [Imputation instructions and a demonstration are available here](https://github.com/THOMASELOVE/431-2018-project/blob/master/survey-results/impute_example.md).

4. Review the Task G and Task H instructions to be sure that you have completed all necessary analyses for Project Study 1, and that you have a clear understanding of the things you'll need to do in your presentation.

- We covered all materials you would need to do Analyses 1, 2, 4, 5 and 6 before today's class.
- During class 22, we will cover Analysis 3.

#### Some Tips

1. **Naming Things** is hard. But don't make it harder on yourself by picking a very generic name (like `survey` for the data you will use. Even `sur431` is better than that, since `survey` is an important package name in R.
2. **Getting Started in the RIGHT WAY** The biggest problem people struggle with is that packages fight each other for function names (like `select`). To avoid this, load every package you plan to use before you load the tidyverse. 
3. This also means calling `source("Love-boost.R")` **prior** to the loading of packages, as opposed to after it, as I did it in the [Study 1 Demonstration Project](https://github.com/THOMASELOVE/431-2018-project/tree/master/demo_study1). Be sure to make that change - **I will be looking to see that you have done this properly**. I expect most to begin section 2 of their Project with an initial setup that looks like this...

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

### Study 2

The Project Study 2 Demonstration page will be available in time for our discussion in Class 22 (Thursday 2018-11-15).

- Don't forget that [Task F](https://thomaselove.github.io/431-2018-project/taskF.html) (Sharing Study 2 Data), is due at noon on Wednesday 2018-11-28, after the Thanksgiving break.

## Visualization of the Day

## One Last Thing

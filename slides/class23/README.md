# 431 Fall 2018 Class 23: 2018-11-27

## Today's Materials

- The slides for Class 23 are now available [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class23/431_class-23-slides_2018.pdf) and [in R Markdown](https://github.com/THOMASELOVE/THOMASELOVE/431-2018/master/slides/class23/431_class-23-slides_2018.Rmd).
- Class 23 audio files will appear above after class.

## Today's Main Example

Today, we'll be working with a new data set from the WOMAN-ETAC trial, of the effect of tranexamic acid on coagulation and fibrinolysis in adult women with postpartum hemorrhage. The women's blood samples were measured at baseline, and then again 30 minutes after the first dose of either tranexamic acid or placebo and then measured again at follow-up (death, discharge from hospital, or 42 days, whichever comes first.) The WOMAN-ETAC study involves women delivering at the University College Hospital, Ibadan, in Nigeria.

The WOMAN-ETAC trial is a substudy of the WOMAN trial. The main result of [the WOMAN trial, as reported in a 2017 Open Access article in The Lancet](https://www.thelancet.com/journals/lancet/article/PIIS0140-6736(17)30638-4/fulltext) was that:

> ... (TXA) reduces death due to bleeding in women with post-partum haemorrhage with no adverse effects. When used as a treatment for postpartum haemorrhage, tranexamic acid should be given as soon as possible after bleeding onset.

- Here are a few key terms you might want to know:
    - Hemorrhage = substantial bleeding, usually from a ruptured blood vessel
    - Postpartum = after vaginal delivery or cesarean section delivery of a baby
    - Coagulation = the process of blood changing to a solid or semi-solid state, forming a clot
    - Fibrinolysis = enzyme breakdown in blood clots (prevents clots from growing and becoming problematic)
    - Tranexamic Acid (abbreviated TXA) - medication used to prevent or treat excessive blood loss (in this case, it was injected)
    - D-dimer concentration = a D-dimer is a small protein fragment present in the blood after a clot breaks down. It is determined through a blood test, measured in mg/liter. Higher levels indicate more trouble.
    - Prothrombin time, the INR (International Normalized Ratio) and the Activated Partial Thromboplastin time are assays which evaluate coagulation. Each measure is used to describe the clotting tendency of blood. (In the real study, these are secondary outcomes).
- The data are available through the FREEBIRD project at https://ctu-app.lshtm.ac.uk/freebird/ (registration required) and were posted there by researchers at the London School of Hygiene and Tropical Medicine on 2018-07-27.
- I'll also provide [the PubMed link to the paper describing the WOMAN-ETAC study design](https://www.ncbi.nlm.nih.gov/pubmed/28317031) for your reference.
- Today, we'll use data from 95 women in the WOMAN - ETAC substudy to focus on 8 key modeling and analytic steps that you'll be doing in many regression analyses, especially in Homework 8 and in Project Study 2.

## Homework 7 Materials

- Homework 7's [answer sketch](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework7) and [grading rubric](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework7) are now available.
- Grades for Homework 7 are in the usual place, at http://bit.ly/431-2018-hw-grades.

## Remaining Course Deliverables

- Project [Task F](https://thomaselove.github.io/431-2018-project/taskF.html) (Sharing Study 2 Data), is due at noon on Wednesday 2018-11-28.
- [Homework 8](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework8) is due at noon on Friday 2018-11-30. Dr. Love posted a hint for Question 6 and some specifications on how we'll grade the essay in Question 1 to the [revised instructions for Homework 8](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework8/431-2018-hw8.md) on 2018-11-17.

## The Project Study 1 Template

Dr. Love emailed you a template for Project Study 1 on 2018-11-17. It is also available as an [R Markdown file here](https://github.com/THOMASELOVE/431-2018-project/blob/master/study1template/431-project-study1_template.Rmd). 

- The template has some nice features, including tabs and chapter separations by headings, and it should import the data properly, freeing you to start pruning the big data set down to what you actually need. 
- The template assumes you have an R project directory for project study 1 containing this R Markdown file, the five data sets, and the `Love-boost.R` script, [all of which are posted here](https://github.com/THOMASELOVE/431-2018-project/tree/master/study1template).
- If you want to see what the HTML file looks like that the template creates, it is [posted at this RPubs site](http://rpubs.com/TELOVE/Project-study1-template-431-2018).

## Simple Exploratory Data Analysis in one line of code?

Check out [this blog post by Laura Ellis](https://www.littlemissdata.com/blog/simple-eda). In it, she describes several useful tools for initial data analysis. One of the most interesting to me (and to Laura) is a function in the `DataExplorer` package called `create_report()`, which provides an extensive data profile of your data frame in a single command, including "basic statistics, structure, missing data, distribution visualizations, correlation matrix and principal component analysis for your data frame"!

So, in our case, I installed the `DataExplorer` package, and then ran the following commands:

```
library(DataExplorer)
create_report(etac431)
```

and [the result can be seen here](http://htmlpreview.github.io/?https://github.com/THOMASELOVE/431-2018/blob/master/slides/class23/431_2018_Data_Profile_Report_ETAC.html).

## What is a Successful Data Analysis?

[What is a successful data analysis?](https://simplystatistics.org/2018/04/17/what-is-a-successful-data-analysis/) Roger Peng suggests ...

> A data analysis is successful if the audience to which it is presented accepts the results.

At the end of the piece, he writes something which resonates with me a lot, especially as I think about evaluating your projects next month.

> Good communication with an audience can often play a much bigger role in success than whether you used a linear model or quadratic model. Trust between an analyst and audience is critical when an analyst must make choices about what to present and what to omit. Admitting that human nature plays a role in data analysis success is difficult because humans are highly subjective, inconsistent, and difficult to quantify. However, I think doing so gives us a better understanding about how to judge the quality of data analyses and how to improve them in the future.

## Visualization of the Day

Nathan Yau gives us "[A Day in the Life of Americans](https://flowingdata.com/2015/12/15/a-day-in-the-life-of-americans/)"

## One Last Thing

- The `tidymodels` meta-package [is a thing](https://github.com/tidymodels/tidymodels). I'm hoping to learn more about it soon.

# 431 Fall 2018 Class 11: 2018-10-02

## Today's Materials

- The slides will be available above [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class11/431_class-11-slides_2018.pdf) and [in R Markdown](https://raw.githubusercontent.com/THOMASELOVE/431-2018/master/slides/class11/431_class-11-slides_2018.Rmd).
- Class 11 audio files will be posted above as soon as they are available.
- This is the last session of Part A of the Course. We will begin Part B on Thursday, 2018-10-04.

## Announcements

1. [Quiz 1](https://github.com/THOMASELOVE/431-2018/tree/master/quizzes) will be released to you by noon Friday 2018-10-05 and is due at 7 PM on Monday 2018-10-08 (Columbus Day). Note the change to **7 PM** instead of noon for the deadline. This means 7 PM on the nose, and not 8 PM, or even 7:01 PM.

2. [Homework 5](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework5) is not due for a while - it's 2018-10-19.

3. The [Answer Sketch for Homework 4](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework4) is available. We expect to get the Homework 4 grades and rubric posted on Thursday 2018-10-04.

4. A Few R Markdown Coding and Style Issues I want to make sure you've caught onto:

- Always leave a blank line between chunks and text.
- Separate paragraphs in your text with blank lines.
- Do not load the `datasets` package. It is part of the basic material. 
- In general, don't load packages for which you will only use a single function, especially if you're not using that function multiple times.
- Always load the tidyverse last in your list of packages, and don't use a semi-colon after the final package you load.
- Always leave a space between the # and the header name, so `# Question 1`, not `#Question 1`.
- Never have a chunk name that includes a space. Use underscore _ if you like to separate words, so, as an example a chunk named `{r Pearson_correlation}` is fine, but `{r Pearson correlation}` isn't.
- When building a ggplot, be sure to specify the tibble first, and then the aesthetics. Every time.
- A better choice than `theme(legend.position = "none")` is `guides(color = FALSE)` if you're trying to remove a legend about `color`.

5. Largely Unedited Results of the [Group Study 1 Brainstorming Activity From Class 10](http://bit.ly/431-2018-class10-brainstorm-feedback) are available now at http://bit.ly/431-2018-class10-brainstorm-feedback. We'll discuss this further on Thursday.

6. Links from today's class:

- [What Alcohol People Around the World Drink](http://flowingdata.com/projects/2016/alcohol-world/) from flowingdata.com
- [WHO Global Health Observatory Indicator Metadata Registry](http://apps.who.int/gho/data/node.wrapper.imr?x-id=462) for Alcohol
- [How to share data with a statistician](https://github.com/jtleek/datasharing) from Jeff Leek's group at Johns Hopkins.
- Hadley Wickham from 2010 on [Tidy data & tidy tools](https://vimeo.com/33727555) at the NYC Open Statistical Computing Meetup
- A.S.C. Ehrenberg's paper on data presentation "[The Problem of Numeracy](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class11/Ehrenberg_1981_pw_The_Problem_of_Numeracy.pdf)" from *The American Statistician* is well worth your time, despite being written in 1981. It is password-protected.
- If we have time, we may spend a few minutes talking about election forecasting, and communicating the results of a forecast effectively, in the context of the [2018 House forecast at FiveThirtyEight.com](https://projects.fivethirtyeight.com/2018-midterm-election-forecast/house/?ex_cid=midterms-header). If we don't get to this today, we'll do it first thing in Class 12.

7. **In-Class Table**: During today's session, we'll be working in small groups to improve a table. A [copy of that table is posted above (as the Class 11 supplementary table) in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class11/431_2018_class-11-supplementary-table.pdf). You can look at either the first or second page - they are equivalent for our purposes.

# A Promotional Announcement

A few folks from the class came to see me in **Sweeney Todd** this weekend. Thank you for doing that. If you're interested, the show runs for the next two weekends on Friday and Saturday evenings and Sunday afternoons, and tickets are available at https://www.eventbrite.com/e/sweeney-todd-tickets-37253162211. We expect sellouts for the evening performances, so if you're interested, we strongly recommend you buy your tickets in advance.

# One Last Thing

There is a new set of massive open online courses from the Johns Hopkins University Data Science Lab called [Chromebook Data Science](http://jhudatascience.org/chromebookdatascience/). This is for anyone with a web browser and an internet connection (and nothing else) to learn a meaningful amount about Data Science. Here's a [blog post at Simply Statistics](https://simplystatistics.org/2018/10/01/chromebook-data-science-an-online-data-science-program-for-anyone-with-a-web-browser/) laying out some of the goals. Very exciting.

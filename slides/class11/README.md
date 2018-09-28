# 431 Fall 2018 Class 11: 2018-10-02

## Today's Materials

- The slides will be available above [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class11/431_class-11-slides_2018.pdf) and [in R Markdown](https://raw.githubusercontent.com/THOMASELOVE/431-2018/master/slides/class11/431_class-11-slides_2018.Rmd).
- Class 11 audio files will be posted above as soon as they are available.

## Announcements

1. [Quiz 1](https://github.com/THOMASELOVE/431-2018/tree/master/quizzes) will be released to you by noon Friday 2018-10-05 and is due at noon on Monday 2018-10-08 (Columbus Day).

2. [Homework 5] is due 2018-10-19.

3. [Answer Sketch for Homework 4] is now posted.

4. A Few R Markdown Coding Issues I want to make sure you've caught onto:

- Always leave a blank line between chunks.
- Do not load the datasets package. It is part of the basic material. And ALWAYS load the tidyverse last, and don't use a semi-colon after the final package you load.
- Always leave a space between the # and the header name, so # Question 1
- Never have a chunk name that includes a space. Use underscore _ if you like to separate words, so {r Pearson_correlation} is fine, but {r Pearson correlation} isn't.
- When building a ggplot, be sure to specify the tibble first, and then the aesthetics.
- A better choice than `theme(legend.position = "none")` is `guides(color = FALSE)` if you're trying to remove a legend about `color`.

5. [Reactions to the Group Activity From Last Time] are coming.

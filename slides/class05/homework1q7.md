# Your Questions from HW 1, Question 7

This document contains Questions of Potentially General Interest posed by students responding to Homework 1 Question 7, and my answers to those questions. Some of the questions were edited to collapse ideas from more than one student.

Question 7 was:

> Ask one question of Dr. Love about this course (ideally one that you haven’t asked us already) that interests you.
> It can be a question about the syllabus, the readings, the project, the homework assignments, the course notes, anything big or small, but it shouldn’t be a fact that you can find already in the Course Syllabus.

## About the Materials / Web Site

1. The front page at https://github.com/THOMASELOVE/431-2018 contains links to the Syllabus, the Course Notes, to the Homework, to the Calendar, and to the instructions for Software, the Quizzes, the Project, and the daily Slides. It also lists the office hours for the TAs and all of our contact information. Everything is linked on that page that I can think of.
2. In response to a request from a student, TA office hours are also posted now in the Course Syllabus and (as always) they are also at the bottom of the Course Calendar page.

## How do you use Markdown to make things other than HTML documents? What about the slides you show us in class - how do we make those?

In 431, we'll stick to HTML for assignments, but I'm sure that some of you will build Word and/or PDF versions of your work, too, for other purposes and for the project. All of the R Markdown code for the class slides is available to you, in addition to the PDF result. There are several different formats available in R Markdown, including the beamer PDF style I use for our slides. Look at [this Gallery of options](https://rmarkdown.rstudio.com/gallery.html) for some ideas and next steps.

## Can we use something (like Python, Matlab, SAS, whatever) to do our work for class?

Nope. Everything needs to be done in R and R Markdown in 431 and 432.

## What does “factor” do when defining the aesthetics of a ggplot?

R defines several types of variables, including “numeric”, "character" variable and a "factor" variable, for instance. Factors are used to work with categorical variables that have a fixed and known set of possible values. To learn more, I encourage you to read the [Factors chapter in R For Data Science](http://r4ds.had.co.nz/factors.html).

## Will we create code to analyze data from electronic health records?

Not directly, no, though we will work regularly with data that came from EHRs, especially in 432. But this isn’t a course in bioinformatics. Pulling data from an EHR involves a series of steps we won’t be discussing in order to identify and ingest the data. Once that’s done, though, the tidyverse is well-suited to handle some “big data” tasks, although sometimes the “data_table” approach [introduced here](https://cran.r-project.org/web/packages/data.table/vignettes/datatable-intro.html) is more attractive with really big samples.

## I am working on preparing some tables to present some demographic, medical history and functionality testing results of our patients at baseline for a manuscript. Would this be something that I would be able to code and organize/format in R and then put it into our manuscript draft?

I certainly hope so, although some tricks and tools will appear in 431 and others in 432. But that’s the idea.

## I’m interested in knowing how you take a spreadsheet of your own data and pull it into R to manipulate.

Look at the last section of the [Getting Started in R document at our software page](https://github.com/THOMASELOVE/431-2018/blob/master/software/431-getting-started-with-R.pdf).

## How do you know what packages you need when starting an analysis?

Well, you always need the tidyverse, so that’s a safe bet. When doing an analysis, I wind up adding things to the list of packages as I figure out that I need them.

## Questions about Deliverables

### Is the presentation of our final project in front of the class or only Dr. Love?

Just me.

### When should I start working on the project?

Most people will start in the final week of September. There's no real reason to start sooner, but I wouldn't let it slide past October 1.

### Will our quizzes be more about interpretation of results or about generation of results/writing code?

Those choices don’t cover everything I’ll assess, and some items of course touch on both, but I’d say more of the former.

## Questions about What I Like

### What is the most satisfying part of teaching 431?

When a student has a positive experience in the course project and gives a thorough and thoughtful presentation. Especially if they happen to be more enthusiastic (at the end of the semester) than they thought (at the beginning) that they would be. You didn’t ask, but the biggest pain point is grading.

### What is your favorite program to code in, and which do you feel is most beneficial for data science and related work?

I use R, almost exclusively, for all of my data work. I am a big fan of it. I’m teaching you the tools I have actually found to be the most useful. The reason we use R in this course in this way is because that’s what I wanted to do.

My favorite part of R is the tidyverse. The tidyverse is used by (at least) millions of people worldwide, and Hadley and Garrett's book on the subject: R for Data Science, has been downloaded an incredible number of times, despite which the printed version of the book is a best seller - rated in the top 1300 books for sale on Amazon.

### Why did I choose this career?

- I wanted to be a scientist (like my father) and I wanted to be a teacher (like my mother.) I liked sports statistics and math and music in high school, and thought I would become a mathematician, but when I got to college, I didn’t like the stuff that people seemed to do with a Mathematics PhD because it was too divorced from applications (and I was only good at some of it.) If I could choose my coursework again, I’d have taken economics, too. I thought it wasn’t important because I’m not motivated (much) by money. That was dumb. 
- If I could have been anything, it wouldn’t have been very far from what I do now, but I think my applied work would have focused more on education and less on health, and I'd have liked to do this work with more undergraduate students to work with. While I love doing theater and sports as hobbies, I never wanted to pursue either as a career, and I realized early on that I didn't have the skills or temperament necessary to be an athlete or an actor full-time.

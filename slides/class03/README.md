# 431 Fall 2018 Class 03: 2018-09-04

## Today's Slides

Class 3 slides are available in [PDF format](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class03/431_class-03-slides_2018.pdf), as well as in [R Markdown](https://raw.githubusercontent.com/THOMASELOVE/431-2018/master/slides/class03/431_class-03-slides_2018.Rmd).

Class 3 audio files will appear above, after class.

- The Getting Started in R document is available in [R Markdown](https://raw.githubusercontent.com/THOMASELOVE/431-2018/master/slides/class03/431-getting-started-with-R.Rmd) and as [a PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class03/431-getting-started-with-R.pdf), and can also be [viewed in HTML](http://htmlpreview.github.io/?https://github.com/THOMASELOVE/431-2018/blob/master/slides/class03/431-getting-started-with-R.html).
- Today, we'll do some live coding. Useful files for that include:
    - A .csv file of the [2018 day 1 survey data](https://raw.githubusercontent.com/THOMASELOVE/431-2018-data/master/surveyday1_2018.csv)
    - An R Markdown template called [YOURNAME-hw1.Rmd](https://raw.githubusercontent.com/THOMASELOVE/431-2018/master/slides/class03/YOURNAME-hw1.Rmd) that I'll use as my starting point for live coding.
    - An R Markdown file called [class3-pre.Rmd](https://raw.githubusercontent.com/THOMASELOVE/431-2018/master/slides/class03/class3-pre.Rmd): my pre-class version, to save you the typing.
        - You can also see [the HTML result of knitting this class3-pre file here](http://htmlpreview.github.io/?https://github.com/THOMASELOVE/431-2018/blob/master/slides/class03/class3-pre.html).
    - I'll also post the version I build live, to be called **class3live.Rmd**, after class.

## Deliverables Coming Soon

- By Wednesday at Noon
    - Complete the [Minute Paper After Class 03](http://bit.ly/431-2018-minute03) at http://bit.ly/431-2018-minute03. Log into Google via CWRU to do so.
- Before Thursday' class
    - Read Chapters 5, 9, 10 and 13 of Jeff Leek's [The Elements of Data Analytic Style](https://leanpub.com/datastyle).
- [Homework 1](https://github.com/THOMASELOVE/431-2018/tree/master/homework/Homework1) is due on Friday 2018-09-07 at Noon. Submit your R Markdown and HTML files via Canvas. 
    - We treat work that arrives before 1 PM as on time. 
    - Work after that is late. **Don't be late**. It is **far, far** better to be incomplete than late for homework in this class.
- You need the [course software](https://github.com/THOMASELOVE/431-2018/tree/master/software) up and running on your computer now. 
    - This means you have R, R Studio, the necessary R Packages, **and** the data for 431 working properly. 
    - If you're still having trouble after class, contact a teaching assistant or Dr. Love (perhaps through **431-help**), as you'll need this working to do the homework assignment.
- Dr. Love is available in/near this classroom or in his office (Wood WG 82-L) for 15 minutes before and 30 minutes after every class.

## Today's Announcements

### Materials added to our [Data and Code](https://github.com/THOMASELOVE/431-2018-data) page

- I've added the age-love-analysis [R Markdown file](https://raw.githubusercontent.com/THOMASELOVE/431-2018/master/slides/class02/age-love-analysis.Rmd) used to generate the materials included in the [slides for Class 2](https://github.com/THOMASELOVE/431-2018/edit/master/slides/class02), and if you want to see [the HTML result, here it is](http://htmlpreview.github.io/?https://github.com/THOMASELOVE/431-2018/blob/master/slides/class03/age-love-analysis.html).
- I've edited the `YOURNAME-hw1.Rmd` file to correct a couple of typos. Thanks to the student who pointed them out, and thus earned herself some class participation credit. Please help us **kill typos**, by emailing 431-help (or Dr. Love directly) when you find them.

### Get help at any time by emailing **431-help at case dot edu**.

1. Apply the 15-minute rule. If you can't solve a problem in 15 minutes, **ask for help** either from us or from Google.
    - You are **absolutely supposed** to use Google and the TAs (and Dr. Love) to improve your code.

2. When asking for help with an R problem from **431-help at case dot edu**, we ask you to try to make it easier for us to help you. Specifically...

- attach a copy of the R Markdown file you are working on,
- include a screenshot or copy-and-paste listing of the error you are generating, if that's the problem.
- attach a copy of the data set (if it's not about a homework assignment or other data set that we gave you),
- attach a copy of the HTML result (if you can create it), and

With the R Markdown file, and a detailed explanation of the problem you see, we can often solve the problem in an email. Without the R Markdown file, we can rarely do anything except ask more questions.

3. When you get a response from one of us on **431-help at case dot edu** you'll notice we REPLY ALL so that all of the TAs (and Dr. Love) can see the result. If you need to respond, please fight your usual urge and **REPLY ALL** as well so that we can all still help. You want to be sure that `431-help at case dot edu` is in the list of recipients of each of your emails, even though replies will come from individuals.

### Teaching Assistant Office Hours

Teaching Assistant Office Hours are held in WG-56 (Computing Lab) or WG-67 (Student Lounge) on the ground floor of the Wood building, so be sure to look in both places. TA office hours started this morning, and continue Wednesday at noon. 

- You'll find the complete schedule on the bottom of the [Course Calendar](https://github.com/THOMASELOVE/431-2018/blob/master/calendar.md), and remember to contact us at **431-help at case dot edu** if you have questions at other times.

### Datacamp

Thanks to the roughly 70% of you who've now signed up for our class on Datacamp. Please let us know if you have any questions. For suggested courses, please [visit the Datacamp section of the Syllabus](https://thomaselove.github.io/2018-431-syllabus/datacamp.html), and if you've found any courses particularly useful, we'd love to hear about it.

### Professor Love is giving a research talk (together with Dr. Shari Bolen) on Friday morning

The talk is entitled "Racial and Ethnic Approaches to Community Health Grant: Hypertension Implementation in 9 Safety Net Clinics" and is from 9 to 10:30 AM in Room R219 at the Rammelkamp building on the campus of MetroHealth Medical Center. For more information, ask Dr. Love, or visit http://chrp.org/events/

## One Last Thing

- Do you know about the [R Studio Cheat Sheets](https://www.rstudio.com/resources/cheatsheets/)?

The main web site for this course is https://github.com/THOMASELOVE/431-2018.

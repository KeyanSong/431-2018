# 431 Fall 2018 Class 19: 2018-11-06

## Today's Materials

- The slides for Class 19 are available [in PDF](https://github.com/THOMASELOVE/431-2018/blob/master/slides/class19/431_class-19-slides_2018.pdf) and [in R Markdown](https://github.com/THOMASELOVE/THOMASELOVE/431-2018/master/slides/class19/431_class-19-slides_2018.Rmd), above.
- Class 19 audio files are posted above.

## Upcoming Deliverables from the [Course Calendar](https://github.com/THOMASELOVE/431-2018/blob/master/calendar.md)

- Please complete this [Minute Paper after Class 19](http://bit.ly/431-2018-minute19) by noon on Wednesday 2018-11-07. Thank you.
- [Homework 6](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework6/431-2018-hw6.md) is due to [Canvas](https://canvas.case.edu/) by noon on Friday 2018-11-09.
  - After today's Class 19, we anticipate you will be able to do Questions 2-4 more easily. You should already be comfortable with Questions 1 and 5-7.
- [Homework 7](https://github.com/THOMASELOVE/431-2018/blob/master/homework/Homework7/431-2018-hw7.md) is due to [Canvas](https://canvas.case.edu/) by noon on Friday 2018-11-16.
  - Homework 7 has nine questions. You should be able to do questions 6-9 now. Questions 1-5 will need to wait until we have discussed the Analysis of Variance and some related issues.
- The next project-specific deliverable is [Task F](https://thomaselove.github.io/431-2018-project/taskF.html) (Sharing Study 2 Data), which is due at noon on Wednesday 2018-11-28, after the Thanksgiving break.

## Project Updates

This was a [busy weekend](https://github.com/THOMASELOVE/431-2018-project/tree/master/survey-results).

1. Dr. Love has now reviewed and commented on your Survey Comparison Plan materials (from Task D). 
2. Dr. Love has also prepared the data files you will need to actually do Project Study 1.
3. He has also prepared materials to help you merge and combine data sets for the Project.
4. He has also prepared materials to help you do simple imputation for any missing data in the Project.

See the details on all four of these things at [this link](https://github.com/THOMASELOVE/431-2018-project/tree/master/survey-results).

## Election Day

There's a lot of exciting stuff to read...

### At FiveThirtyEight, I particularly enjoyed...

- The [Election Day and Night Live Blog](https://fivethirtyeight.com/live-blog/2018-election-results-coverage/) is up and running now.
- Nate Silver's ["Democrats Aren't Certain to Take the House, but They're Pretty Clear Favorites"](https://fivethirtyeight.com/features/final-election-update-democrats-arent-certain-to-take-the-house-but-theyre-pretty-clear-favorites/)
- Nathaniel Rakich's ["How To Watch the Midterms: An Hour-By-Hour Guide"](https://fivethirtyeight.com/features/2018-election-polls-close/) 
- FiveThirtyEight Politics Podcast had several interesting episodes. I recommend:
  - ["The Midterms Are Here"](https://fivethirtyeight.com/features/politics-podcast-the-midterms-are-here) from 2018-11-05.
  - ["Model Talk: How To Judge Our Forecasts](https://fivethirtyeight.com/features/politics-podcast-how-to-judge-our-forecasts/) from 2018-11-02.
- We'll check in again on the Ohio [Governor's Race and other Midterm Election forecasts](https://projects.fivethirtyeight.com/2018-midterm-election-forecast/governor/) at FiveThirtyEight. As of 11:06 AM on 2018-11-06...

FiveThirtyEight Model | Lite (polls only) | Classic (add fundamentals) | Deluxe (add experts' ratings)
-------------------------: | :--------------------: | :--------------------: | :--------------------:
Chance Cordray (D) elected | 2 times in 3 (66.5%) | 3 times in 5 (59.5%) | 5 times in 8 (61.9%)

- We might also glance at the [Latest Polls](https://projects.fivethirtyeight.com/polls/) at FiveThirtyEight, too.
  - Looking at the [Generic Congressional Ballot polls](https://projects.fivethirtyeight.com/congress-generic-ballot-polls/) is particularly interesting to me.
  
## Some Statistical Content: Comparing Proportions in a 2x2 Table, and the role of the Independence Model

**What is the chance (according to FiveThirtyEight) that the most common forecast scenario (House winner: Democrats, Senate winner: Republicans) will happen?**

- As of 11:06 AM on 2018-11-06, the FiveThirtyEight Classic forecast for the House gives Democrats an 87.9% chance of winning the House.

Proportions | House winner: Dem  | House winner: Rep | Total
----------: | ---------: | -------: | -------:
Senate winner: Dem | ? | ? | -
Senate winner: Rep | ? | ? | -
Total              | .879 | .121 | 1.0

Or, if the election were held 1,000 times, we could write this as:

Counts | House winner: Dem  | House winner: Rep | Total
----------: | ---------: | -------: | -------:
Senate winner: Dem | ? | ? | -
Senate winner: Rep | ? | ? | -
Total              | 879 | 121 | 1000



- As of 11:06 AM on 2018-11-06, the FiveThirtyEight Classic forecast for the House gives Republicans an 80.9% chance of winning (keeping) the Senate.

Counts | House winner: Dem  | House winner: Rep | Total
----------: | ---------: | -------: | --------:
Senate winner: Dem | ? | ? | 191
Senate winner: Rep | ? | ? | 809
Total | - | - | 1000

**Are these results independent of each other, or are they (associated/correlated)?** 

- If the results were independent, that would imply that the Democrats would have an 87.9% chance of winning the House, regardless of what happens in the Senate.

So, we'd have a table like this, under the assumption of independence:

Counts | House winner: Dem  | House winner: Rep | Total
----------: | ---------: | -------: | -------:
Senate winner: Dem | (191 x 879)/1000 = 168 | (191 x 121)/1000 = 23 | 191
Senate winner: Rep | (809 x 879)/1000 = **711** | (809 x 121)/1000 = 98 | 809
Total              | 879 | 121 | 1000

So under the assumption of independence, what do the forecasts suggest about the probability of a Democratic House *and* a Republican Senate in 2019?

- But the FiveThirtyEight simulations actually show that the chances of the Democrats winning the Senate but losing the House are very, very small. Suppose they were 1/1000. Then we have:

Counts | House winner: Dem  | House winner: Rep | Total
----------: | ---------: | -------: | -------:
Senate winner: Dem | ? | 1 | 191
Senate winner: Rep | ? | ? | 809
Total              | 879 | 121 | 1000

We could then derive the other results, by subtraction...

Counts | House winner: Dem  | House winner: Rep | Total
----------: | ---------: | -------: | -------:
Senate winner: Dem | 190 | 001 | 191
Senate winner: Rep | **689** | 120  | 809
Total              | 879 | 121 | 1000

Under these assumptions, what do the 538 forecasts suggest about the chances of a Democratic House *and* a Republican Senate in 2019?

**Post-class note**: In posting [538's final set of forecasts](https://fivethirtyeight.com/features/our-final-forecast-in-the-senate-house-and-gubernatorial-races/) (using the deluxe model, and some different assumptions) Nathaniel Rakich did this work, as well, and so their actual estimate is 67.9%, rather than 68.9% of House Dem, Senate Rep in 2019. That post is "[Our Final Forecast In The Senate, House And Gubernatorial Races](https://fivethirtyeight.com/features/our-final-forecast-in-the-senate-house-and-gubernatorial-races/)".

### Some Other Sites...

- This evening, you may want to visit [The Needle](https://www.nytimes.com/2018/11/05/upshot/needle-election-night-2018-midterms.html) and related live election forecasts at [The Upshot](https://www.nytimes.com/section/upshot), from *The New York Times*.

![](https://static01.nyt.com/images/2018/11/05/upshot/needle-3-by/needle-3-by-jumbo.png?quality=90&auto=webp)

- [XKCD has an interesting map "2018 Midterm Challengers"](https://xkcd.com/2067/), and also "[Election Night](https://xkcd.com/2068/)" below...

![](https://imgs.xkcd.com/comics/election_night.png)

- The [CBS News / YouGov House Model](https://today.yougov.com/topics/politics/articles-reports/2018/11/04/cbs-newsyougov-house-model-democrats-225-republica) which uses multilevel regression and post-stratification (Mr. P for short), which is a technique that a lot of statisticians are excited about. 
- [CNN provides its own Forecast](https://www.cnn.com/election/2018/forecast), too, built by a team of data scientists led by Harry Enten (formerly of FiveThirtyEight). There are [some descriptions of their methodology](https://www.cnn.com/2018/10/12/politics/the-forecast-methodology/index.html), and some interesting graphics.
- The Washington Post is providing timely [Midterm Election Updates](https://www.washingtonpost.com/politics/2018/live-updates/midterms/midterm-election-updates), too. 
  - You might be interested in Jordan Heller's ["Ohio ballot initiative on drug penalties is motivating voters in Cleveland"](https://www.washingtonpost.com/politics/2018/live-updates/midterms/midterm-election-updates/ohio-ballot-initiative-on-drug-penalties-is-motivating-voters-in-cleveland/?utm_term=.9c3a2631e8d7) piece from last night, for example.
- If you like Fox News, they have [midterm power rankings](https://www.foxnews.com/midterms-2018) which rate elections in a more traditional way. I'm not sure whether a model is driving this, or not.
- The [MIT Election Data and Science Lab has an R package for accessing data on U.S. elections](https://github.com/MEDSL/elections), focused on data from the 2016 election.

## My Personal Thoughts

To quote [Harry Enten](https://twitter.com/ForecasterEnten/status/1059848288759898112):

> People want soothsayers. That's not what I or anyone vaguely in my profession are. We are there to tell you the most likely outcome and the chance of that occurring.

1. Statisticians want to understand the world's path in clear terms, too, just like everyone else. In fact, we REALLY REALLY want to do that. For many of us, that's part of the reason why we got interested in statistics in the first place, back when it wasn't so cool.
2. But our training and our experiences in working with surveys/polls/data push us inexorably in the direction of humility when faced with difficult questions like how humans will behave.

Personally, I identify with the people who want more people / lots of people / all the people to participate in the process - both of electing people and of writing and thinking about how to forecast elections, and what election results mean for all of us. One of the reasons my job is worth doing is that I spend meaningful time most days trying to help people get a better grasp of uncertainty, and learn how to think about it effectively, rather than being paralyzed. I hope that you find the time to vote today (unless, of course, like me, you voted already) and to be kind and assume the best of your fellow voters, regardless of the results. I aim to do that myself.

## One Last Thing

Rafael Irizarry wrote a provocative blog post on 2018-11-01 called ["The role of academia in data science education"](https://simplystatistics.org/2018/11/01/the-role-of-academia-in-data-science-education/) which I found interesting. I would very much enjoy finding the time to ponder this sort of thing more deeply.

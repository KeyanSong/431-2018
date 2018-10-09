# An Extra Example for Part A: Sleep and Mammals

This example reviews some of the key work we did in Part A of the course. It uses the `msleep` data set, which is part of the `ggplot2` package. Use the help file for that data set or visit http://ggplot2.tidyverse.org/reference/msleep.html to assist in understanding the data.

**For those of you who have been assigned this task**, you need to complete it successfully by **2018-10-26 at Noon**. 

- In order to receive bonus credit on Quiz 1, you must answer at least 9 of the 10 questions correctly. 
- Submit the work via Canvas in the Quiz 1 Bonus assignment, which is available only to those of you who have been sent to this page by Dr. Love. 
- If you submit the work before **2018-10-24 at Noon**, the TAs will grade it and return it to you for revision if you score less than 9/10. 
- You can discuss this bonus assignment with Dr. Love and the TAs in person or via `431-help` but do not discuss it with your colleagues.
- Good luck!

1. Identify the number of rows and number of variables in the `msleep` data set.
2. Specify the variable with the largest number of missing values. How many values are missing?
3. Identify the mammal who remains `awake` the longest, per day. What is the Z score for this mammal?
4. Display your R code to create a data set (called `sleep2`) from `msleep` which contains the variables `name`, `order`, `vore`, `sleep_cycle` and `sleep_rem` for those animals who have no missing values in any of those four variables, then convert the `vore` information into a factor. 
5. According to the `order` variable, how many Primates (see the `order` variable) exist in your `sleep2` data set?
6. Draw a plot to compare the `sleep_rem` levels by `vore` group using your `sleep2` data. What do you conclude?
7. Produce R code using the `%>%` pipe to produce a table which answers these two questions for the `sleep2` data: [a] Which `vore` group has the largest mean `sleep_rem` level? [b] Which `vore` group has the largest mean `sleep_cycle`? 
8. Now, return to the original `msleep` data for questions 8-10. Build a scatterplot of `brainwt` and `bodywt`, first using the raw data and then using a logarithmic scale for each variable. 
9. Fit a linear model to the scatterplot you drew in part 8 for which a linear model seems more appropriate, and specify and describe (in a sentence of two) both the fitted least squares equation *and* the Pearson correlation coefficient.
10. Identify the mammal in your model (in part 9) with the largest (in absolute value) regression residual. 

**Note to others who may have stumbled onto this page**: Some people in the class were assigned the task of completing this example as a result of their performance on Quiz 1. When they have completed that process, we will produce an answer sketch for this material, and publicize it to everyone.

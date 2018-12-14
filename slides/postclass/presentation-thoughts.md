# Thoughts on the 431 Project Presentations for Fall 2018

## Percentage of Time Spent on Data Prep

I asked each of the 47 students who completed their presentations this week what percentage of their time with the data was spent in cleaning and management, rather than analysis.

![](https://github.com/THOMASELOVE/431-2018/blob/master/slides/postclass/datapreppct.png)

Min | Q1 | Median | Q3 | Max | Mean | SD 
:-: | :-: | :-: | :-: | :-: | :-: | :-:
10 | 27.5 | 55 | 70 | 90 | 49.89 | 23.03 

## Some Things I'll Want to Change in the 431 Demo Projects Next Year

1. When running a Tukey HSD comparison, it's helpful to use the `ordered = TRUE` argument within the function, so that all of the levels of the factor are arranged in increasing order of their means before taking differences, so that all of the estimated means in the plots will be positive.

2. When reporting out the results of applying a set of regression models in a test sample, we should perhaps show the square root of the MSPE, along with the MAPE and the maximum error, because the square root of the MSPE (sometimes called the Root Mean Square Prediction Error) is on the same scale as the other two options.

3. I should drop the `options(max.print="75")` line in the Global options, so that people with large regression models will still be able to see all of the coefficients print.

4. I should provide substantial additional guidance on using `simputation`, in particular demonstrating good approaches to chaining imputations together, and dealing effectively with troubleshooting for binary variables, categorical variables stored as factors and as characters, and quantitative variables that are discrete, and those that are (more) continuous.

5. I should de-emphasize the use of skew1 and other numerical summaries of shape and tail behavior in favor of plots. Too many people didn't trust their read on a plot, but did trust skew1.

6. If the data in an ANOVA setting aren't well described by a Normal distribution, though, we should emphasize the value of simply using a transformation before running the ANOVA.

7. Using the `slice()` function in R to identify residuals that are marked in a residual plot.

8. The use of a ridgeline plot in comparing samples, to go along with summarized or facetted plots of distributions.

9. Some discussion of Cook's distance and sample size. A highly leveraged point is somewhat less likely when we have a very large sample.

10. Show how to execute some of the more exotic power transformations, in particular the inverse square and inverse square root.

11. Move the Box-Cox work and transformation assessment for the outcome in a regression model together, and use that transformation in building a scatterplot matrix.

12. Also move up the collinearity check with vif to follow the scatterplot matrix more closely.

13. We may want to read Broman and Woo in 431, much earlier than this year.

## Some Things I'm Thinking About Adding to 432 this Spring

1. A bootstrap-based one-factor analysis of variance. 
2. An earlier start to multiple imputation.
3. An earlier start to robust linear models, especially to deal with heavy or light tails in the outcome.
4. An earlier start to cross-validation of a regression model.
5. An example where we deal with a categorical predictor that has many, many levels which need collapsing in a regression context.
 
## About Analysis 5 in Study 1 and plotting results from Cross-Classifications

Most people used `assoc`, but there were several other potentially better options, including:

- [waffle plots](https://github.com/hrbrmstr/waffle), 
- [mosaic plots](https://cran.r-project.org/web/packages/ggmosaic/vignettes/ggmosaic.html), 
- [double decker plots](https://www.rdocumentation.org/packages/vcd/versions/1.4-4/topics/doubledecker), 
- [bar charts](https://ggplot2.tidyverse.org/reference/geom_bar.html), and 
- [Cleveland dot plots](https://uc-r.github.io/cleveland-dot-plots), for example.

One person even tried a correspondence analysis.

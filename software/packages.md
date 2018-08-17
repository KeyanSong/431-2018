# R Packages Used in 431

## Installing All Necessary R Packages (Do once, at the start of the semester)

1. Copy and paste the following two lines of code into the Console window of R Studio to install the packages you'll need for this course.

<!-- -->

    pkgs <- c("aplpack", "arm", "babynames", "boot", "broom", "car", "cowplot", 
              "devtools", "Epi", "faraway", "forcats", "foreign", "gapminder", 
              "GGally", "ggridges", "gridExtra", "Hmisc", "knitr", "lme4", 
              "magrittr", "markdown", "MASS", "mice", "mosaic", "multcomp", 
              "NHANES", "pander", "psych", "pwr", "qcc", "rmarkdown", "rms", 
              "sandwich", "survival", "tableone", "tidyverse", "vcd", "viridis")

    install.packages(pkgs)

2.  Execute those commands by hitting Enter.

3.  Now, go to the **Packages** tab on the right side of your screen, and click on **Update**. Select and install all available updates. This may take a few minutes.

4.  Finally, choose **File ... Quit R** from the top menu, and accept R Studio's request to save your workspace. This will eliminate the need to re-do these steps every time you work in R.

## Installing a Single Package (Do when you need to add a new package)

If you want to install a single package, you can do so by finding the word **Packages** on the right side of your screen. 

- Click on the **Packages** menu to start installing the packages you'll need. 
- Then click **Install**, which will bring up a dialog box, where you can type in the names of the packages that you need. these should be separated by a space or comma. 
- Be sure to leave the Install dependencies box checked.

## Updating Your Packages (About once per week)

You should update your R packages about once a week, and also whenever you encounter a problem in R that you can't solve otherwise.

- Click on the **Packages** tab on the right side of your screen, and click on **Update**. 
- This will bring up a dialog box. Select and install all available updates. 
- A popup box may ask you whether you want to install from sources the packages which need compilation. Yes is fine, but No is faster, usually.
- This may take a minute or two, but definitely not more than five minutes.
- Choose **File ... Quit R** from the top menu, and accept R Studio's request to save your workspace.


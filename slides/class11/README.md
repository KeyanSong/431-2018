TEMP

In lines 16 and 17 always leave a blank line between chunks. This happens again at 32-33
In line 18, do not load the datasets package. It is part of the basic material. And ALWAYS load the tidyverse last, and don't use a semi-colon after the final package you load.
In line 28 always leave a space between the # and the header name, so # Question 1
In line 30 never have a chunk name that includes a space. Use underscore _ if you like to separate words, so {r Pearson_correlation} is fine, but {r Pearson correlation} isn't. This happens again at 33 and 41 and lots of other places.
Then in line 59, you use the iris data set for your ggplot, instead of the iris1 tibble. That doesn't make any sense.
In line 68 a better choice than   theme(legend.position = "none") is guides(color = FALSE)

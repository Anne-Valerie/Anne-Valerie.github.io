Once we were confident with the extracted serving styles, it was time to analyse and try to answer our initial question ! First, we looked at the distribution of the grades for each aspect of the tasting palette : aroma, palate, taste, appearance and overall grade, for each serving style.

**boxplot distrib**
**distributions (histplot)**

 We did this using a t-test, which yielded each time a p-value lower than 0.05, suggesting that there was a statistically significant difference in these scores, based on the serving style. Then, we realized that the number of samples was very uneven between the serving styles (lots of bottles, moderate number of draft and a few cans), so we needed to find a test that was unsensitive to the sample size when comparing distributions : the Kruskal-Wallis test. This also yielded p-values very close to 0, suggesting once again that the distributions were different. But where does the difference come from ? Because we cannot affirm that we have not neglected some common confounders such as the beer group or some region of the world. 

 **plot p-values before filtering**
 
 Therefore, we started by filtering our data once more, to evaluate beers that had at least 7 reviews in each serving style, to control for that variable. But the results were very similar, the p-values yielded by the Kruskal-Wallis test are still way below 0.05. This means that the difference in the ratings **does not come from the serving style!**

 **plot p-values after filtering**
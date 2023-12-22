Once we were confident with the extracted serving styles, it was time to analyse and try to answer our initial question ! First, we looked at the distribution of the grades for each aspect of the tasting palette : aroma, palate, taste, appearance and overall grade, for each serving style.
Does the serving style influence the rating of the beer ?

**boxplot distrib**
**distributions (histplot)**

From the boxplots, we see that indeed the ratings are different between the serving styles! As expected, people prefer draft beers, and then bottles, and finally cans. Can still seem to suffer from the bad reputation of the 70s, when they were associated with cheap beers.

What about the other aspects ? Regarding the appearance of the beer, people really don't like cans! Is it because they don't see the beer, or because the beer is not as good ? Regarding the aroma, palate and taste, the ratings are even more different between the serving styles! 

But is this difference statistically significant ?


We threw our data into the statistical boxing ring, armed with t-tests, hoping to unveil the undisputed champions of beer ratings based on serving styles. Ding, ding, ding! The p-values came out swinging, all below 0.05, indicating a statistically significant difference in scores. But wait, our dataset had a bit of a size mismatch – lots of bottles, a fair number of drafts, and just a few cans. It was like comparing heavyweights to featherweights, so our new friend Kruskal-Wallis test stepped in to level the playing field. The p-values were still below 0.05, so we can conclude that the difference in ratings is not due to the serving style!

 **plot p-values before filtering**

 But wait, is it the only cofounder ? What about the beer style, the alcohol by volume, the brewery ? We have to check that the difference in ratings is not due to these variables.
 To check this, we used a turn-around strategy. We started by filtering our data to evaluate beers that were served in the three different seving style! Therefore, if the rating is different for bottles, cans and drafts, it is not due to the beer style, the alcohol by volume or the brewery, but to the serving itself !
 We used beers that had at least 7 reviews in each beer style. The number 7 made sure the amount of reviews was significant but still enough different beers were detected. 

 The results of this analysis was... that the difference in the ratings **does not come from the beer style!**
 So where does it come from ? Maybe the beer style influences the rating at the same time as the serving style ? 
 But the results were very similar, the p-values yielded by the Kruskal-Wallis test are still way below 0.05. This means that the difference in the ratings **does not come from the beer style!**
 
 Therefore, we started by filtering our data once more, to evaluate beers that had at least 7 reviews in each serving style, to control for that variable. But the results were very similar, the p-values yielded by the Kruskal-Wallis test are still way below 0.05. This means that the difference in the ratings **does not come from the serving style!**

 **plot p-values after filtering**
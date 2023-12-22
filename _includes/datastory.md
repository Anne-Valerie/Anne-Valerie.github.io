---
layout: home
title: Bottles, Cans, or Drafts
subtitle: Pouring Over the Data to Decode the Perfect Sip
---

# Abstract

In this dive into the beer world, our project seeks to figure out the subtle differences that various ways of serving—bottle, can, and draft—bring to beer reviews. We're curious about what makes people like one style over another. Why does it matter, you ask? Because beer enthusiasts, much like you and me, take their choices seriously. And we want to know if the container affects how they rate and describe the brew. By closely looking at a dataset of beer reviews, we want to spot any connections or trends that show how serving styles might sway the overall rating and what people say about the beer. As we take on this bubbly quest, we hope to quench the thirst for understanding how picking between a bottle, can, or draft might shape how beer lovers feel.

## The Curiosity Spark

Picture this: A cozy pub, friends gathered, and the bartender presenting three options – a bottled beauty, a canned contender, and a freshly poured draft. Each sip tells a story, and we're here to decode it. What makes a person lean towards one style over another? Is it the tactile satisfaction of popping a cap, the convenience of a can, or the experience of a perfectly pulled pint?

Our journey is fueled by burning questions:

1. Does a specific serving style consistently earn higher or lower ratings than its counterparts?
2. Are certain beer types more closely linked to a particular serving style?
3. Do regional preferences influence the choice of serving style in different corners of the globe or across the United States?


## Unveiling the Data
<b> Beer Styles and Reviews </b>

To start, let's take a look at the distribution of beer styles and the number of reviews each beer has received.

![10 most common beer styles](/assets/img/beer_styles.png)
![Number of reviews per beer](/assets/img/reviews_per_beer.png)

The first image unveils the top 10 most common beer styles, providing insights into the variety within our dataset. The second image presents a histogram, showcasing the distribution of reviews per beer in a logarithmic scale.

<b> Breweries and Locations </b>

Moving on, let's explore the brewery landscape and the most prevalent brewery locations.

![Number of beers per brewery](/assets/img/beers_per_brewery.png)
![10 most common brewery locations](/assets/img/brewery_locations.png)

Here, we delve into the brewery landscape, examining the distribution of beers per brewery and the top 10 locations where breweries thrive.

<b> User Reviews and Locations </b>

Our exploration wouldn't be complete without understanding the users behind the reviews. Let's unravel the story of reviews per user and the most common user locations.

![Number of reviews per user](/assets/img/reviews_per_user.png)
![10 most common user locations](/assets/img/user_locations.png)

In these images, we unveil the distribution of reviews per user and uncover the top 10 locations where our users hail from. Let the exploration continue!


<b> Separation of Beer Types into More General Groups </b>

These groupings provide us with a more generalized view of beer styles, setting the stage for uncovering hidden patterns within each category. Let's proceed with our intriguing exploration!

[![Beer Types Sunburst](/assets/plots/sunburst.png)](/assets/plots/sunburst.html)

But wait, we've got a missing ingredient – the serving style!


---

### Could Filtering Help?

---

### How About the Emotions Beer Evokes?

---

### Readability Score and Metrics Update

---

### Which Countries Are the Most Beer-Friendly?

---

### Which Beers Are the Most User-Friendly?

- Grouping all beer styles into broader categories (Ales, Stouts, Lagers, Strong Ales, Wheat Beers, Specialty and Unique Beers, Seasonal and Celebration Beers, Sour Beers, and Historical and Traditional Beers).
- Counting the number of beers in each category. This was done to address the imbalance in category sizes (e.g., there are 30 ales in our dataset but only 8 stouts).
- Counting the number of reviews per category.
- Calculating the average number of reviews per category (number of reviews divided by the number of beers in the given category). This analysis was conducted to further understand the imbalance in category sizes.
- Counting the number of reviewers per category.
- Calculating the average number of reviewers per category (number of reviews divided by the number of beers in the given category). This was also performed to address the imbalance in category sizes.
- Counting the number of reviews from each region for every category separately. The purpose of this step was to determine which countries consume or review specific types of beers the most. At this stage, it is not possible to ascertain preferences for specific beers in different regions but rather to identify which ones are consumed or reviewed more frequently.

## Part 3: Statistical Analysis

Once we were confident with the extracted serving styles, it was time to analyse and try to answer our initial question ! First, we looked at the distribution of the grades for each aspect of the tasting palette : aroma, palate, taste, appearance and overall grade, for each serving style. We did this using a t-test, which yielded each time a p-value lower than 0.05, suggesting that there was a statistically significant difference in these scores, based on the serving style. Then, we realized that the number of samples was very uneven between the serving styles (lots of bottles, moderate number of draft and a few cans), so we needed to find a test that was unsensitive to the sample size when comparing distributions : the Kruskal-Wallis test. This also yielded p-values very close to 0, suggesting once again that the distributions were different. But where does the difference come from ? Because we cannot affirm that we have not neglected some common confounders such as the beer group or some region of the world. Therefore, we started by filtering our data once more, to evaluate beers that had at least X reviews in each serving style, to control for that variable. But the results were very similar. This means that the difference in the ratings **does not come from the serving style!**

## Part 4: Regional Analysis

...

## Part 5: Conclusion

...


---
title: Bottles, Cans, or Drafts
subtitle: Pouring Over the Data to Decode the Perfect Sip
---

## Part 2: Serving Style Extraction

In our exploration of 250 hand-checked beer reviews, we set out to uncover the mysteries of serving types. We kicked things off with the simple Naïve method, choosing a serving type when the answer was obvious. However, as the reviews got more complex, we tried the fancier Similarity method, using calculations to compare review text with potential serving types.

Despite our efforts to enhance accuracy, the straightforward Naïve method proved to be more effective overall. The accuracy decreased, and the number of reviews categorized as unknown increased. Subsequently, we decided not to pursue the Similarity method further and continued refining the Naïve method. We acknowledged its limitations, especially when dealing with ambiguous statements like the one found in some reviews: "I actually found this more elegant and less bruising than expected. Stone can still surprise," where the word "can" functioned as a verb, not a serving type, but our algorithm mistakenly considered it one.

To address such challenges, we introduced a Rule-based method. This involved differentiating between the verb 'can' and the noun 'can' in the reviews and excluding serving types if certain verbs ("would," "could," "'d," "will") were present. For instance, in sentences like "and I will certainly be keeping an eye out for a bottle," the serving type 'bottle' wouldn't be considered because the user had not yet consumed from a bottle. Despite these efforts, challenges persisted, leading us to refine our approach further with a Tense-based method.

In the Tense-based method, we focused solely on the unknown reviews identified in the Rule-based analysis. The method involved analyzing the different tenses of the verbs before the serving type. When a verb in the past was found, the serving type was taken. However, if the verbs were all in the present, the serving was concidered unknown.

All these methods were applied by examining the 250 hand reviews and were modified to maximize accuracy. The journey from the simple Naïve method to the more refined Tense-based method underscores the complexities involved in recognizing serving types in reviews.reviews.


This journey from the simple Naïve method to the refined Tense-based method shows the complexities of recognizing serving types in reviews. Cheers to the adventure! 🍻

### Naive Approach

#### Results

---

### Similarity Approach

#### Results

---

### Rule-Based Approach

#### Results

---

### Tense-Based Approach

- Analyzing 'can' to differentiate the verb and the noun (I labeled the cans that were nouns).
- Analyzing the verbs before each serving type.
- If the verb before the serving type is a modal word, don't keep it.
- For the verbs that precede the serving type in the past and present:
  - Case 1: More than one verb in the past, keep the first.
  - Case 2: One (or more) verb in the past and one (or more) in the present, keep the first verb in the past.
- For the verbs that precede the serving type only in the present:
  - Case 1: More than one serving type in the list, unknown.
  - Case 2: Only one serving type in the list, keep the unique serving type.

#### Results

- Fewer unknowns.
- Achieved 94% accuracy on the evaluation set.
- Took longer to run than the rule-based approach; took the unknowns from the rule base (had 59% on the whole dataset) and applied the tense base to reduce the number of unknowns (reduced to 55%).
- A decrease of 4% represents around 100,000 more reviews for our analysis.

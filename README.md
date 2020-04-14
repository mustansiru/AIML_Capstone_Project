# AIML Capstone Project
Aspect based sentiment analysis Capstone project for Great Learning AIML course 2019

## Pre-processing
### Sample dataset
Data is split up among all participants as follows (alphabetical order):
- 1 to 2000 : Amit
- 2001 to 4000 : Darshan
- 4001 to 6000 : Mustansir
- 6001 to 8000 : Shalini

### Determine most popular features
Do a web query to find out most popular features of mobile phones in the year 2019 using the keywords - "most popular features of mobile phones in 2019". Take top 10 features from the list. These will be our features for sentiment analysis.

### Determine relevance of reviews (which to keep and which to discard)
- Plot each feature as a column in the dataset next to each review.
- Loop through the reviews and search for the feature name. Whichever feature name is mentioned in the review, tag it in their respective column as 1, else 0

Once completed, your data frame should look similar to:
| Review Text      | F1 | F2 | F3 | F4 | F5 | F6 | F7 | F8 | F9 | F10 |
|------------------|----|----|----|----|----|----|----|----|----|-----|
| Review Record 01 | 0  | 1  | 0  | 0  | 0  | 1  | 0  | 0  | 0  | 0   |
| Review Record 02 | 1  | 0  | 0  | 1  | 0  | 1  | 0  | 0  | 0  | 1   |
| Review Record 03 | 1  | 0  | 1  | 1  | 0  | 0  | 1  | 0  | 0  | 1   |

Scan through all rows and remove the rows where all features = 0 (these are reviews where our features are not mentioned, thus they are not relevant)

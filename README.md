# Data wrangling WeRateDogs

## Introduction
This project will be analyzing tweet archive of Twitter user @dog_Rates (A.K.A. WeRateDogs) that rates and comments on people's dogs. Data gather from real world always isn't clean. Python libraries are used to gather, assess and clean its quality/tidyness. 


## Approach
1. Gathering 3 datasets
2. Assessing data for quality and tidiness issues
3. Cleaning data for all issues
4. Insights & visualization 
 
 
## 1. Gathring Data
- Twitter_archive_enhanced: Provides each tweet that includes dog name, dog score and dog stage. This link is provided to download manually.

- Tweet image predictions data (what breed of dogs): Classify each tweet's dog breeds according to a neural network. This file (image_predictions.tsv) can be downloaded programmatically from Udacity's servers using the Requests library and the following URL: https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv

- Twitter API & JSON: Include retweet count and favorite count will be gathered using Tweepy to query Twitter's API for additional data beyond the data included in the WeRateDogs Twitter archive.

## 2. Assessing Data
Both visual and programatic assessments were done to point out quality and tidiness issues. Quality issues are content issues that is inaccurate or redundant. Tidiness issues are the structural issues and unorganized data frames.

### Quality Issues
- Tweets that are retweeted because theses tweets are not original.
- Tweets that has no image.
- Fix tweets contains inconsistent capitalization on predicted dog names.
- Incorrected datatypes on tweet-id and timestamp.
- None and inaccurate strings found in name column.
- Incorrected ratings on rating_numerator and rating_denominator.
- High ratings found that do not make sense.
- Rating_numberator and rating_denominator can be converted into one column

### Tidiness Issues
- All three files have common tweet_id column, which can be used to join all three files as one dataframe.
- 4 different columns (doggo, floofer, pupper, and puppo) on dog stages should be combine in only one column.
- Drop unnecessary columns that are not useful for analysis.

## 3. Cleaning Data
Cleaning were performed on every issues found on assessment step. Each issue is fixed by the following 3 steps:

Define: Explaining the problem and the approach.
Code: The complete code that run to fix the data.
Test: Assess the data again to make sure the code works and fixed the issue.

## 4. Conclusion
By wrangling the Twitter datasets with many Python libraries with above 3 steps. The datasets became much cleaner. The datasets are now ready to be analyzes to find meaningful insights, then build visualization to summarize the results.

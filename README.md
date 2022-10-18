# Wrangle and Analyze - WeRateDogs
## by Abdulafiz Musa


## Dataset

This data wrangling project was carried out using the data wrangling process:
Gather
Assess
Clean
These 3 processes were used to gather the necessary data required; assess by identifying redundant, flawed and unwanted data present; and clean the data using the assessment. We aim at producing a high quality data that can easily be explored and reported to gain insights and make decisions concerning this project.

GATHERING

3 pieces of data were used in this project. Dataframes were created from:

a csv file, twitter_archive
a link to a tsv file, tweet_image_predictions
a query using the tweepy library on Twitter API, tweet_status
The dataframes extracted include 2356 rows x 17 columns, 2075 rows x 12 columns, 2326 columns x 32 rows dimensions respetively.

ASSESSING

9 quality issues and 4 tidiness issues were identified by visual and programmatic assesment in these 3 dataframes. Some of these issues are however resolved together since they are related and the solution to one is sufficient to clean the other issue e.g. dropping retweets and comments.

Content and structural issues identified include but are not limited to null values, missing data, incorrect value extraction, duplicates, unnecessary columns, wrong data type. These were identified using basic functions of info(), describe(), notnull(), sum(), shape.

CLEANING

After making copies of each dataframes, the assessments of the issues were effected into the copied dataframes.

t_archive_clean
t_image_predictions_clean
t_status_clean
These were finally modified into dimensions of 2085 rows x 5 columns, 2075 rows x 10 columns, 2326 rows x 3 columns respectively. This was carried out using the define-code-test cleaning sequence with functions including replace(), contains(), drop(), astype(), extract(), rename(), merge(). head() and info() were often used in confirming the functionality of each code.

The final copies after cleaning were merged to give a single final dataframe: twitter_archive_master with a dimension of 1951 rows x 16 columns; a big run down, but a more consistent and presentable data from the initial volume of data before assessing and cleaning.

## Summary of Findings

Insights and visualizations were generated from the final master dataframe: twitter_archive_master from the wrangling process.

>The twitter_archive_master contains the tweet ids, timestamps, texts displayed on the tweet, rtaings, dog breeds predictions and the amounts of likes and retweets. These columns are sufficient for us to communicate our final data without being superfluous.

>All tweets used in this study was collected from 2015-11-15 to 2017-08-01 and a total of 1951 user tweets with adequate information was selected for inisghts and visualization. This is a long way from the 5000+ tweets at the very beginning of this project. This shows how redundant, dirty and messy data can be a large chunk of unreportable data.

>The neural network was able to give 3 possible guesses to the dog breed in the image included in a particular tweet. From these guesses, we are able to check for the most occuring dog breed in our data, with golden retriever and Labrador retriever at the peak with an occurrence of 258.

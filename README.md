# WeRateDogs-Twitter-data-analysis

## Introduction
WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "they're good dogs Brent." WeRateDogs has over 4 million followers and has received international media coverage.

This report addresses the wrangling process for this data:
 
## Project Process
Process followed to wrangle the data as follow:
* Gathering data
* Assessing data 
* Cleaning data

## Gathering data
There are 3 datasets required for this project and it is collected as follow
* Twitter archive file: The twitter_archive_enhanced.csv was provided by Udacity and downloaded manually.
* The tweet image predictions: This file (image_predictions.tsv) is hosted on Udacity's servers and was downloaded programmatically using the Requests library and URL information.
* Twitter API & JSON: Based on tweet IDs in the WeRateDogs Twitter archive, Twitter API for each tweet's JSON data collected using Python's Tweepy library and stored each tweet's entire set of JSON data in a file called tweet_json.txt file.Then in padas this txt file is read with tweet ID, favorite count, retweet count, followers count, friends count, source, retweeted status and url.

## Assessing data
Assessment of data done as below:
* Visually: Jupyter Notebook (Print dataframe) and Excel is used to assess visually.
* Programmatically: Pandas methods like. info, value_counts, sample, duplicated, groupby, etc used for assessment
Then issues differentiated in quality issues and tidiness issues. Main point is to keep original ratings with images.
 
## Cleaning data
Cleaning is completed in three parts: 
* Define
* Code
* test 

Initially copy was created of the three original dataframes which helped me to keep original data untouched so that I can make copy from it in case of error occurred. 
There were a couple of cleaning steps that were very challenging. One of them was in the image prediction table. I had to create a ‘nested if’ inside a function in order to capture the first true prediction of the type of dog. The original table had three predictions and confidence levels. I filtered this into one column for dog type and one column for confidence level. Other interesting cleaning code was to melt the dog stages in one column instead of four columns as original presented in twitter archive. One very challenging cleaning step was when I had to correct some numerators that were actual decimals.

## Conclusion
* Data wrangling is one of the most important part in data analyst’s life.
* Tweepy for Twitter is really helpful in python to scrape data from web and altogether python has many libraries like beautiful soup which plays significant role in web scraping. 
* Handling, assessing, cleaning and visualizing of data is possible programmatically using python code.

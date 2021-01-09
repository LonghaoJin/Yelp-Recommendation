# YelpRecommendation
This repo contains several projects on the Yelp dataset, namely EDA, sentiment analysis as well as a basic recommendation syetem of the businesses w.r.t. the categories.

## Data Source
The dataset comes from the open source on Yelp and it is not included here due to the huge volumn. Interested reader can referr it at [Yelp](https://www.yelp.com/dataset).

## Data Processing
1. Find the business that is still open and delete the closed ones.
2. Explore the categories and extract the type **Restaurants**.
3. Merge the bussiness.json and review.json according to the *bussiness_id*.
4. Drop the irrevelent columns, for example *'address'*,*'city'*,*'state'*,*'postal_code'*,*'latitude'*,*'longitude'*,*'attributes'*, etc.
5. **Undone** Detect the language of the comments, keep only the English version. 

## Task I: Sentiment Analysis
The reviews contain float values range from 0.0 to 5.0. We need to transfer them into positive and negative signal by setting *sentiment=0* if *score<=3.0* else *sentiment=1*. Due to the large volumn of the data (more than 4M reviews), we sample 100K reviews without replacement from the original data. And 1/3 of the data are negative, 2/3 are positive.

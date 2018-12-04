# Yelp_Review_Sentiment

### The goal of this analysis was to develop a classification model that could identify a positive or negative text review. This was achieved by utilizing a dataset consisting of records of Yelp text reviews and the review’s corresponding star rating of a business.

### The sample of reviews used for model building consisted of 50,000 one star rated reviews and 50,000 five star rated reviews in order to clearly understand whether a review was positive or negative. For understanding of sentiment, an one star review will be interpreted as negative and a five star review as positive.

### The best model was able to correctly classify reviews in the validation set with 97% accuracy. Therefore, it is possible to use the model in other contexts to evaluate the sentiment of a text review. However, given the bias of the reviews fed to the model (only one and five star reviews) the model would be most appropriate in determining what percentage of text reviews were glaringly positive of the total as unit testing displayed a negative bias towards an average review. 

#### Data Source: https://www.yelp.com/dataset

#### Description of Files:

#### YELP_Review_CreateDB.ipynb:
 - Due to the size of the reviews json file from Yelp (~5 gigs representing ~6M reviews), used a Pandas JSON reader to chunk the data into a SQLite DB so that I could then query database to create sample of reviews

#### YELP_SampleQuery.ipynb:
 - File that queries the Reviews SQLite DB for 50,000 five star reviews and 50,000 one star reviews and stores sample into csv file
 
#### YELP_SentimentAnalysis-Final.ipynb contains:
 - Data Visualizations with WordClouds
 - Text Cleansing and Transformation into Count Matrix
 - Model Building and Evaluation
 

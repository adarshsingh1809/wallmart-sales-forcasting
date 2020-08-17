# Kaggle's Walmart Recruiting - Store Sales Forecasting

This is the R code I used to make my submission to Kaggle's Walmart Recruiting - Store Sales Forecasting competition.


This code uses the observation that for the same dept, the weekly sales are very similar despite of different magnitudes across all the stores. To see this, use file visualize_weekly_sales.R or have a look into the visualization folder.

I generates a few features using preprocess_data_v1.R/preprocess_data_v2.R and then train a gbm to model the ts data using train_gbm_cross_store_v1.R/train_gbm_cross_store_v2.R. However, I find my gbm model (version 1.0) can not well capture the periodic pattern of some depts, e.g., dept=1. So, I think there are still room for this approach. Some useful discussions about other competitors' approaches and adjustment can be found on the forum:

## Requirements

You should have gbm/geoR/Hmisc installed in R.


## Instructions

* download data from competition website: http://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting/data/
* put all the data into ./data dir
 - ./data/train.csv
 - ./data/test.csv
 - ./data/features.csv
 - ./data/stores.csv
 - ./data/sampleSubmission.csv
* my features can take a while to generate, so I'd suggest you download it from this repo and put then in ./data dir
* run train_gbm_cross_store_v1.R

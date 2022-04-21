# Cryptocurrencies

## Overview

The purpose of this project is to analyze a dataset from many alternative cryptocurrencies to spot trends that make a firm or person want to invest in them. The problem with cryptos is that the most common ones, like bitcoin or ethereum, are becoming unaffordable for the common public. That being said, I will be using *unsupervised machine learning* to see if we can spot any trends that result in opportunities of these altcoins. 

## Resources

- Datasets:
  - crypto_data.csv

- Technologies used: 
  - Python
  - Jupyter notebook
  - Sklearn, pandas, and hvplot libraries
  - Unsupervised Machine Learning


## Results

preprocessed and transformed the data so that unsupervised machine learning could work. This included dropping null values, using only tradaeble and mined cryptocurrencies, numerically encoding categorical columns using the `pandas.get_dummies` method, and scaling the data using the `StandardScaler()` method as well. 

Using the Principal Component Analysis (PCA) to reduce the 98 scaled columns to only 3 principal components. 

The optimal result was 4 clusters. So, I then proceeded with the KMeans analysis to fit the pca dataframe and predict the clustering. The product was this `clustered_df` with a 'Class' column that showed the predictions to which group it belonged to. 

By reading the graph the clustered cryptos by total supply and mined coins, we can observe two outliers. The first one with a lot of supply and a lot of mined coins (BitTorrent Crypto) and another one with a lot of supply but not too many coins mined (TurtleCoin). 

## Summary

The job of unsupervised machine learning is to discover patterns or groups of data when there is no known output. That being said, this analysis was successful at grouping cryptocurrencies into 4 groups. If we were to create a crypto investment portfolio we would need to further analyze the clusters. 

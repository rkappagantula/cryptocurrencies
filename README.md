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

![image](https://user-images.githubusercontent.com/96051648/164460038-8acc0975-35e1-456d-8d78-261ff94f01f8.png)


The optimal result was 4 clusters. So, I then proceeded with the KMeans analysis to fit the pca dataframe and predict the clustering. The product was this `clustered_df` with a 'Class' column that showed the predictions to which group it belonged to. 

By reading the graph the clustered cryptos by total supply and mined coins, we can observe two outliers. The first one with a lot of supply and a lot of mined coins (BitTorrent Crypto) and another one with a lot of supply but not too many coins mined (TurtleCoin). 

Elbow Curve:

![image](https://user-images.githubusercontent.com/96051648/164459534-615577f3-783d-4bb8-a7c9-fe47c9528b1d.png)

3D Scatter:

![image](https://user-images.githubusercontent.com/96051648/164459721-a322ba06-af16-49d7-83fc-998769458db5.png)

HV Plot Scatter:

![image](https://user-images.githubusercontent.com/96051648/164459855-aaa974b2-4dde-468a-b473-d8f746b243cf.png)



## Summary

The job of unsupervised machine learning is to discover patterns or groups of data when there is no known output. That being said, this analysis was successful at grouping cryptocurrencies into 4 groups. If we were to create a crypto investment portfolio we would need to further analyze the clusters. 

# Cryptocurrencies

## RESULTS

I preprocessed and transformed the data, this included dropping null values, using only tradaeble and mined cryptocurrencies, numerically encoding categorical columns using the pandas.get_dummies method, and scaling the data using the StandardScaler() method as well.

Then, I proceeded with the Principal Component Analysis (PCA) to reduce the 98 scaled columns I had, to only 3 principal components.

![Pic_1](https://user-images.githubusercontent.com/105950742/194438110-3869f9ec-557d-4679-8f91-d5aa42b6a9a1.png)

Then, to see how many clusters (k) I could divide the cryptos in, I created an elbow curve.

![Pic_2](https://user-images.githubusercontent.com/105950742/194438111-b739b922-2d74-4ce9-bfe3-8e31800c9d8d.png)


As it can be seen, the optimal result was 4 clusters. So, I then proceeded with the KMeans analysis to fit the pca dataframe and predict the clustering. The product was this clustered_df with a 'Class' column that showed the predictions to which group it belonged to


![Pic_3](https://user-images.githubusercontent.com/105950742/194438112-f2ecadc2-2150-4999-9ee5-a1ea9f915c3a.png)


As it is seen, there are 3 major groups and one outlier. Similarly, when trying to graph the clustered cryptos by total supply and mined coins, we can observe two outliers. The first one with a lot of supply and a lot of mined coins (BitTorrent Crypto) and another one with a lot of supply but not too many coins mined (TurtleCoin).

![Pic_4](https://user-images.githubusercontent.com/105950742/194438114-f6b7f359-8033-4903-b2a6-c8a6a4f3ad80.png)
![Pic_5](https://user-images.githubusercontent.com/105950742/194438109-2b180a01-4d34-48de-a236-8d1c1608918a.png)

## SUMMARY

This analysis was successful at grouping cryptocurrencies into 4 groups. If we were to create a crypto investment portfolio we would need to further analyze the clusters. We can see that the most profitable and known cryptos are somewhat in the 2 groups that have less supply and mined coins in comparison to others. These cryptos are Bitcoin and Ethereum.

# 18Cryptocurrencies

## Overview of the Project

I've been partnered with Martha to create a report on cryptocurrency.  An company wants to offer an investment portofolio of cryptocurrency options to their customers, but they are at a loss of where to begin. And they don't want their customers to lose, so they've hired Martha and myself to get to work on this report that will include what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment bank.

The data is not without fault, so it will need to be processed to fit the machine learning models using unsupervised learning grouping and a clustering algorithm. 

There are four analysis deliverables:

**Deliverable 1:** Preprocessing the Data for PCA
**Deliverable 2:** Reducing Data Dimensions Using PCA
**Deliverable 3:** Clustering Cryptocurrencies Using K-means
**Deliverable 4:** Visualizing Cryptocurrencies Results

## Results

### Deliverable 1: Preprocessing the Data for PCA

The data was preprocessed to eliminate unnecessary data:

*All cryptocurrencies that are not being traded are removed.*

![Cryptocurrency Traded](Resources/removed.PNG)

*Remove the "IsTrading" column.*

![Cryptocurrency Drop](Resources/istrading.PNG)

*Remove rows that have at least 1 null value.*

![Cryptocurrency Drop Nulls](Resources/null.PNG)

*All the rows that do not have coins being mined are removed.*

![Cryptocurrency Algorithms](Resources/algorithm.PNG)

*Keep the rows where coins are mined.*

![Cryptocurrency Coins Mined](Resources/coinsmined.PNG)

*A new df is created that stores all cryptocurrency names from the CoinName column and retains the index from the crypto_df.*

![Cryptocurrency Names](Resources/retainindex.PNG)

*The get_dummies() method is used to create variables for the text features.*

![Cryptocurrency Get Dummies](Resources/getdummies.PNG)

*Features from the df have been standardized using the StandardScaler().*

![Cryptocurrency StandardScaler](Resources/scaler.PNG)


### Deliverable 2: Reducing Data Dimensions Using PCA

*The PCA algorithm reduces the dimensions of the crypto_df down to three principal components.*

![Cryptocurrency PCA Components](Resources/PCA.PNG)

*The pcs_df is created from the three principal components and has an index from the crypto_df.*

![Cryptocurrency Component DataFrame](Resources/PCAdf.PNG)


### Deliverable 3: Clustering Cryptocurrencies Using K-means

*An elbow curve is created using hvPlot to find the best value for K.*

![Cryptocurrency Elbow](Resources/elbow.PNG)

*Predictions are made on the K clusters of the cryptocurrencies' data.*

![Cryptocurrency Kmeans](Resources/predictions.PNG)

*A new df is created with the same index as the crypto_df and has the following columns: Algorithm, ProofType, TotalCoinsMined, TotalCoinsSupply, PC1, PC2, PC3, CoinName, & Class.*

![Cryptocurrency Kmeans DF](Resources/newdf.PNG)


### Deliverable 4: Visualizing Cryptocurrencies Results

*The clusters are plotted using a 3D scatter plot, and each data point shows the CoinName and Algorithm on hover.*

![Cryptocurrency 3D Graph](Resources/3Dtext.PNG)
![Cryptocurrency 3D Graph](Resources/3Dscatter.PNG)

*A table with tradable cryptocurrencies is created using the hvplot.table() function.*

![Cryptocurrency New Table](Resources/tradabletable.PNG)

*The total number of tradable cryptocurrencies is printed.*

![Cryptocurrency Tradeable](Resources/total.PNG)

*A df is created that contains the clustered_df index, the scaled data, and the CoinName & Class columns.*

![Cryptocurrency Scaled Data](Resources/totalcoinsmined.PNG)

*A hvplot scatter plot is created where the X-axis is "TotalCoinsMined", the Y-axis is "TotalCoinSupply", the data is ordered by "Class", and it shows the CoinName when you hover over the data point.*

![Cryptocurrency Scatterplot](Resources/hvtext.PNG)
![Cryptocurrency Scatterplot](Resources/hvplot.PNG)

## Summary

Since our data set provided us with 0-4 cryptocurrencies to evaluate, those are the set parameters for our review.  Our analysis shows 3 and zero showing more prevalently than the other numbers.
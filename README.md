# Cryptocurrencies
Applying Unsupervised Machine Learning

## Purpose of the Analysis
The purpose of this project is the create a report for an investment bank interested in offering a new cryptocurrency investment portfolio. The report includes what cryptocurrencies are on the trading market and how they could be grouped to create a classification system for this new investment. In order to complete this project, I am performing unsupervised machine learning functions on data provided by CryptoCompare.

## What We are Creating
This task consists of four technical analysis, as they follow:

        1: Preprocessing the Data for PCA
        2: Reducing Data Dimensions Using PCA
        3: Clustering Cryptocurrencies Using K-means
        4: Visualizing Cryptocurrencies Results

### Preprocessing the Data for PCA

After keeping all the cryptocurrencies that are being traded, dropping the redundants columns, or the ones not used in clustering algorithms, removinge rows with at least one null value, etc, the dataframe looked like Figure 1.

#### Figure 1: The first cleaned DataFrame 

![1-crypto_DataFrame](/pics/1-crypto_DataFrame.png)

### Reducing Data Dimensions Using PCA

Applying the Principal Component Analysis (PCA) algorithm, we reduced the dimensions of the X DataFrame to three principal components and placed these dimensions in a new DataFrame (Figure 2).

#### Figure 2: Applying the Principal Component Analysis Algorithm

![2-PCA](/pics/2-PCA.PNG)

### 

Using the PCS DataFrame, we created an elbow curve using hvPlot to find the best value for K (Figure 3).

#### Figure 3: The elbow curve. 

![3-elbow](/pics/3-elbow.PNG)

### Clustering Cryptocurrencies Using K-means

Using the PCS DataFrame we ran the K-means algorithm to make predictions of the K clusters for the cryptocurrencies’ data and created a new DataFrame by concatenating the crypto_df and pcs_df DataFrames on the same columns (Figure 4).

#### Figure 4:  

![4-clustering](/pics/4-clustering.PNG)

### Visualizing Cryptocurrencies Results

 We finally, created a scatter plot with Plotly Express and hvplot to visualize the distinct groups that corresponded to the three principal components in 2-dimensional (Figure 5) and 3-dimensional plots (Figure 6).

#### Figure 5: The distinct groups that corresponded to the three principal components 

![5-totalcoinsmined](/pics/5-totalcoinsmined.PNG)

#### Figure 6: The three-dimensional plot of the components 

![6-3dPlot](/pics/6-3dPlot.PNG)

Figure 7 shows the total number of coins for the major currencies and the total number of coins for each type of cryptocurrency

![7-majorCurrencies](/pics/7-majorCurrencies.PNG)

## Summary

From the three dimisional graph, You can see that there are four different groups. Two groups are clumped very closely together with most currencies falling into one of these two groups. One group has a few different currencies that are farther away from the others and then there is the last group that only have one currency. This shows that there are lot of currencies that perform similarly while there are a few that are outliers. These outliers could be over performers or under performers, but I would need to perform more analysis to figure that out. One thing that I can connect is by looking at the total coin supply vs total coins mined graph. The two main groups have most of there data points scattered between 0% and 40% of the largest currency based on volume. The group with a few currencies are are very close to 0% of the largest currency, while the group with just one currency is at 100% as it is the largest currency.

I would want to complete further analysis on these cryptocurrencies by looking at their historical pricing to understand the performance of each of these currencies. This would help investors now how stable or risky their investment would be based on the the different cryptocurrencies they invest in.

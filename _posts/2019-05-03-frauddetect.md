---
title: "Fraud detection using Random Forest"
date: 2019-05-03
tags: [maching learning, random forest, k-means clustering]
excerpt: "Fraud Detection"
---

This summer I was determined to learn machine learning algorithms. As one of the first projects, I took up Credit Card Fraud Detection.
The data used for this is retrieved from Kaggle.

When I looked at the data, I realised that the data was heavily PCA'd. I did get rid of nan values in the dataset.![PCA'd dataset](/images/pca.JPG)
As you can see, there is no correlation between the features. I replaced the nan's with the average of that column.
I used scikit learn's random forest classification model to predict the transaction as either a fraud and not fraud. But before doing that, I checked the composition of my data.
I realised that 98% of the transactions were classsified as non-fraud. Running a classification model on such a dataset would result in all or most of the transactions being classified as non-fraud due to the imbalance.
To oversome this, I undersampled the majority class (non-fraud) using the sample method of pandas.DataFrame.![Resampled Dataset](/images/resample.JPG)

After undersampling, I split the dataset into train and test. I initialised a random forest classifier  as such : 

```python
clf= RandomForestClassifier(n_estimators= 200, max_depth= 8)
```

After fitting the training data and predicting on the test data, I got roc_auc_score of 0.9195
I created a method to visualise my test data in a confusion matrix. ![Confusion Matrix](/images/matrix.JPG)
Out of 244 fraud transactions, I predicted 205 of them correctly.

After I was done predicting, I thought of doing transaction analysis using K-Means clustering. Using the sklearns K-Menas model, I got 4 clusters, divided according to the time. Most of the fraud transactions, occured during (insert time). (Add clusering image)

The code for this project can be found [here] (https://github.com/rohitgang/Fraud-Detection)

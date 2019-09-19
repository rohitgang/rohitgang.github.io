---
title: "Fraud detection using Random Forest"
date: 2019-05-03
tags: [maching learning, data science]
header: 
    image: "/images/cluster.png"
excerpt: "KMeans clustering"
---

This summer I was determined to learn machine learning algorithms. As one of the first projects, I took up Credit Card Fraud Detection.
The data used for this is retrieved from Kaggle.

When I looked at the data, I realised that the data was heavily PCA'd. I did get rid of nan values in the dataset. I replaced the nan's with the average of that column.
I used scikit learn's random forest classification model to predict the transaction as either a fraud and not fraud. But before doing that, I checked the composition of my data.
I realised that 98% of the transactions were classsified as non-fraud. Running a classification model on such a dataset would result in all or most of the transactions being classified as non-fraud due to the imbalance.
To oversome this, I undersampled the majority class (non-fraud) using the sample method of pandas.DataFrame.

After undersampling, I split the dataset into train and test. I initialised a random forest classifier  as such : 

```python
clf= RandomForestClassifier(n_estimators= 200, max_depth= 8)```

After fitting the training data and predicting on the test data, I got roc_auc_score of 0.9195
I created a method to visualise my test data in a confusion matrix. Out of 244 fraud transactions, I predicted 205 of them correctly.

# H1

## H2

### H3

Basic text

*italics*

**bold**

[link](hyperlink)

* 1st item
* secind item

1. firdt
2. second

'''python

    import numpy as np

    def sucks():
        x= y
'''

'''r

library(tidyverse)
df <- read_csv('somefile.csv')

'''

'x+y'

<image src= "{{site.url}}{{site.baseurl}}/images/logo.png", alt="linear">

$$x+y=z$$

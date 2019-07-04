---
title: "Fraud detection using K-Means"
date: 2019-05-03
tags: [maching learning, data science]
header: 
    image: "/images/cluster.png"
excerpt: "KMeans clustering"
---

This summer I was determined to learn the machine learning algorithms. When I finished learning
K-Means Clustering algorithm naturally I wanted to do a credit card fraud analysis. The data for this 
project is used from Kaggle (link?).

When I looked at the data, I did not straightaway realise that the features, V1-V28 were anonymised features.
I did not read the documentation for the data and straightaway ignored these features. I looked at **Time**, 
**Amount** and **Class** for the answers. I checked the data for any NaN values and as such replaced them with
the average of that feature. I created a KMeans model with 2 clusters. On a 3D Axes, I plotted Time on X-axis, Amount on Y-Axis and Class on Z-Axis. The clusters that were formed using the whole dataset didn't turn out as expected.
<image src= "/images/fraud.png", alt="kmeans clusters">
The cluster seemed to get divided over the time between 75,000 and 100,000 units, rather than class. 
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
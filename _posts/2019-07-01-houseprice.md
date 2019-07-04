---
title: "Housing Price Analysis"
date: 2019-07-01
tags: [maching learning, data science]
header: 
    image: "/images/cluster.png"
excerpt: "Housing Price Analysis"
---
The data used for the housing price analysis 
came from Kaggle. When I first looked through the data,
I got nervous due to the size of the dataset. There are 
a total of 80 features excluding the ID. This was the first
time I dealt with a dataset of this size.

I am not big into the Housing sector so my domain knowledge
was little. I do have common sense and so I know that size of 
the house *positively* affects the price. When I glanced the dataset,
there were a few fields that stood out to me,
* LotArea
* SaleCondition
* MasVnrArea 
* OverallQual
I knew that these fields were gonna affect the Sale Price directly.
My very first model was a Linear Regression Model with all of the
features except for the ID and the target variable, *SalePrice*.

I defined a function **nanCheck** whihc would check for the 
nan values in the supplied dataframe and if any nan is found,
it would set that entry to zero. I used scikit learn's Label Encoder
to encode strings to integers to ensure compability with Linear Regression
model. Using '''python train_test_split ''' I prepared my training and
my testing data. 

Sklearn's LinearRegression model was fitted with the training and the 
testing data. The metric I used for evaluation is *Root Mean Squared Logarithmic Error (RMSLE)*.
I got a RMSLE of 0.20255. I was surprised to get a RMSLE as low as 0.2.
I knew that this was an easy dataset and hence I wanted to bring the RMSLE closer to zero.

Because my domain knowledge was not adequate, I improvised to select features for my model.
Instead of building from nothing and choosing features, I decided to start with all of the
features. I reduced them one by one and trained and tested my model after each modification.

Soon I ended up with 49 features with a RMSLE of 0.1544. After this, I looked at all the features
and their corresponding coeffecient value. Few of them had pretty strong coeffecients. Among these were 
**Street, Utilities, KitchenAbvGr, BsmtQual, GarageCars**. These were the outliers for my model. After reducing
my feature list, I obtained a RMSLE of 0.1535.

Though not much but still it was a progress. I have a good set of features at hand with not much variability throughout.
I am thinking of ways to improve my model. Maybe I could handle nan values better. I could also use k-cross validation folds
to create train and test data sets to better train my model. 
---
title: "Ada County Housing Analysis"
date: 2019-09-03
tags: [maching learning, random forest]
excerpt: "Housing Analysis"
permalink: /acahouse/
---

This summer my colleague, Nikita Kramar, had an amazing idea for a project. He came
across the Ada county housing website where all the housing data such as the number
of bedrooms, the porch sq. ft., so on and so forth are made public. Looking at this, he
thought of accessing this data and putting it to use. So over the summer, he learned python and 
used selenium to scrape that website and collected all the data into a dataframe. While doing this,
his laptop died many times running this process because the data he was trying to access was of high 
magnitude. 

The dataframe that resulted from his work had depth to it. The columns for the dataframe had links to 
other pages which contained critical information for that house. So he also parsed that which made the 
size of the data grow even more. After he was done parsing every thing, he showed me the dataframe. This was 
in July of this year. When I looked at that dataframe, I knew that it was going to be a long data cleaning and 
manipulation process. From there we started working on cleaning the data. 

We had to parse through html and json formats. This resulted in creation of multiple dataframes. Right now, 
we are in the process of joining those dataframes. We are going to build a model, either random forest or gradient boost
model for our dataset. Updates to come!

Updates are here! We finished our project back in November, I just have been lazy to type it out. Now, getting to 
project, we were able to join the dataframes based on a primary key. Now came the Data Cleaning phase. Lot many nulls 
to deal with. I looked at the types of the data we had and applied traditional techniques to replace nulls. But Nikita 
raised a good question, what if null means that a certain house doesn't have that feature ? For example, we had a feature
called PoolSqFt. It had a bunch of nulls. We assumed that these nulls basically mean that a particular house didn't have a 
pool. It made sense. So I replaced the nulls with 0 and engineered a boolean feature called hasPool. We did this for some 
features which are optional in a house such as garage, pool, fireplace, backyard. Another thing that we assumed was that each 
record was a house which is totally wrong. We realised that we had property data and not housing data. This changed our assumptions. 
Now we were questioning nulls for almost all of the features. Such as bathroomSqFt, maybe a property is a Drive Thru Dutch Bros and 
it doesn't have a bathroom, so it makes sense that bathroomSqFt is null because there is no bathroom! To summarize, the Data Wrangling
phase took the longest time. We also performed feature selection on the dataset and principal component analysis to remove 
correlations between the features.

Now we are at the second to last phase, Machine Learning Model. My all time favourite model is Random Forest because it is not 
sensitive to the variations in the data and you have different parameters to play with to configure your forest. I would like to 
mention that the performance of a machine learning algorithm depends largely on the quality of the data. I say this because after 
evaluating our model the scores were really bad. There were a lot of assumptions in our data wrangling phase and we paid for those 
assumptions. All of this was a learning process. There were a lot of mistakes made and I am thankful that we did.
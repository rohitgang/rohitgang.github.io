---
title: "Ada County Housing Analysis"
date: 2019-09-03
tags: [maching learning, random forest]
excerpt: "Housing Analysis"
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
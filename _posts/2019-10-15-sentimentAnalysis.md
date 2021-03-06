---
title: "Sentiment Analysis using TextBlob"
date: 2019-10-15
tags: [maching learning, sentiment analysis, flask, textblob]
excerpt: "Sentiment Analysis"
permalink: /sentimentanalysis/
---

Past summer I worked on a research project in **Natural Language Procesing**. To get my feet more into NLP,
I decided to work on a **Sentiment Analysis Project**. My initial idea was to *leverage twitter api and monitor* 
*tweets for a specific keyword*. Then I can *plot the subjectivity and polarity of the tweets in real time*. 
I actually came to this end goal by discussing about Sentiment Analysis with **Dr. Kennington**. 
As I got to development, my idea *mutated* to include **flask** and create *a web application*. So now, the main 
parts of my project are : *Flask, TextBlob, Web Dev* 

The file `serverFunctions.py` includes several functions which perform sentiment analysis using the *textblob* 
*library*. Using the textblob library was really easy. But I feel just using the library doesn't give me 
knowledge of sentiment analysis, so I am currently *reading papers* on it and *understanding* how the textblob 
library functions. My `app.py` file is the where *flask* lives. I am not an expert in servers or web interaction, 
so I took time to read up on flask and how it routes to webpages. This project gave me the opportunity to dive 
further into web development. I focused on html, javascript and css for a week. 

The product of dedicating my time to web development was that I was able to create web pages with *forms, divs, articles.* 
By this time, I decided to analyse user input too. I used forms to take in user input like this:
```javascript
<form method="POST">
        <input name="text" size="30" style="color:black">
        <button type="submit"
                value="Submit"
                style="color:black">
            <b>Analyse</b>
        </button>
        <button type="submit" 
                value="Submit" 
                style="color:black" 
                formaction="/subject.html">
            <b>Graph</b>
        </button>
</form>
```




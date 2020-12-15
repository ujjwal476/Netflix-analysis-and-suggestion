## Introduction of the topic


Netflix is popular online streaming service that offers a wide variety of award-winning TV shows, movies, anime, documentaries, and more on thousands of internet-connected devices. It is being popular as you can watch as much as you want, whenever you want without a single commercial – all for one low monthly price. With the streaming service, people are getting choice to watch movies online at home with their family. I mean who does not like this service, right? But, along with this service, are the contents of Netflix qualitative (highly rated)? People have their own choices, so is Netflix providing abundant variety of choices of contents? What genre are most popular in netflix? Keeping this question in mind, I am sure that some people love Netflix, and some don't. So what is actually netflix missing? How can it increase the likeable contents based on the popularity of its present context? Can I recommend some contents of netflix? How does recommendation system work? What if we can predict the rating for netflix and even provide some suggestion in regard to the content it has based on directors.

![Image](netflix.jpg)

Therefore, to answer these questions, my project is going to analyze the data from netflix. I am going to start with general analysis and come up with the suggestion and recommendation model for netflix and users. To start with the project, for one part of the data  I used [uNogs: RapidAPI](https://rapidapi.com/marketplace) to collect the data from API and downloaded the data as json format. Once I had json file, I converted it into csv and read the CSV files in pandas dataframe to perform processing, fitering, analysis and visualizations. Similarly, for another part of the data, I used **kaggle** 

For this project, I imported many library and packages. Some sample of my code import are:
```
import json
import requests
import csv
import pandas as pd
import time
import seaborn as sns
import numpy as np
from os import path
from PIL import Image
from wordcloud import WordCloud, STOPWORDS, ImageColorGenerator
from textblob import TextBlob
import nltk
```
For full version of my code. Click [here](https://github.com/ujjoli/Netflix-analysis-and-suggestion/blob/gh-pages/Individual%20Project%2003-Copy1.ipynb)

As introduced earlier I would like to see the contents of Netflix. 
#### 1. [General Analysis](General analysis.md)

      Quality of contents
      Analysis by country
      Genre analysis
      Rating type
    

#### 2. [Duration and rating analysis](Duration and rating analysis.md)
      
      Distribution of duration in mins
      Co-relation between rating and duration


#### 3. [Popular words and sentiment analysis](Popular words and sentiment.md)

     Popular directors
     Popular words by horror genre
     Popular words by action and adventure
     Popular words by comedy
     Popular words by romance
     Sentiment analysis of description
    
    
#### 4. [Recommendation, prediction and classification](Recommendations.md)

     Recommendation by cast,directors, title
     Prediction of rating
     Suggestion according to classification of rating and directors

You can click [here](General analysis.md) for next page.

You are on [editor on GitHub](https://github.com/ujjoli/third-individual-project/edit/gh-pages/index.md).


Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

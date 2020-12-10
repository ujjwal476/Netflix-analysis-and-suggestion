## Introduction of the topic


Netflix is popular online streaming service that offers a wide variety of award-winning TV shows, movies, anime, documentaries, and more on thousands of internet-connected devices. It is being popular as you can watch as much as you want, whenever you want without a single commercial – all for one low monthly price. With the streaming service, people are getting choice to watch movies online at home with their family. I mean who does not like this service, right? But, along with this service, are the contents of Netflix qualitative (highly rated)? People have their own choices, so is Netflix providing abundant variety of choices of contents? What genre are most popular in netflix? Keeping this question in mind, I am sure that some people love Netflix, and some don't. So what is actually netflix missing? How can it increase the likeable contents based on the popularity of its present context? Can I recommend some contents of netflix? How does recommendation system work? What if we can predict the rating for netflix and even provide some suggestion in regard to the content it has based on directors.

Put netflix image here. ![Image](src)

Therefore, to answer these questions, my project is going to analyze the data from netflix. I am going to start with general analysis and come up with the suggestion and recommendation model for netflix and users. To start with the project, for one part of the data  I used uNogs: RapidAPI to collect the data from API and downloaded the data as json format. Once I had json file, I converted it into csv and read the CSV files in pandas dataframe to perform processing, fitering, analysis and visualizations. Similarly, for another part of the data, I used kaggle.com (put the link here)

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
For full version of my code. Click here(put the link)

As introduced earlier I would like to see the contents of Netflix. 
1. General Analysis (Quality of contents, analysis by country, genre analysis, rating type)
2. Duration and rating analysis
3. Popular words and sentiment analysis
4. Recommendation, prediction and classification


You can use the [editor on GitHub](https://github.com/ujjoli/third-individual-project/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/ujjoli/third-individual-project/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.

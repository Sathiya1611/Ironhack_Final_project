# Ironhack_Final_project
## Sentiment Analysis on Twitter data using NLP

<p align="center">
  <img src="https://user-images.githubusercontent.com/60324758/127534104-02e1b270-4b1a-44fd-9ab1-c9f23c2659c1.jpg" />
</p>
The main aim of this project is to analyze the sentiment (positive or negative) on Twitter data. In particularly people review on Jeff Bezos(the CEO of Amazon and Blueorigin)first space flight on 20th July 2021.

## Contents
1. [Introduction](#Introduction)
2. [Data Cleaning](#DataCleaning)
3. [Data Preprocessing](#DataPreprocessing)
4. [Sentiment Analysis](#SentimentAnalysis)
5. [Visualization](#Visualization)
6. [Conclusion](#Conclusion)
## Introduction
The data used for this analysis was extracted from twitter using the python module called snscrape. Snscrape helps to pull unlimited data. This is a great advantage over Twitter API. The data cleaning was done using the library called regex,to lowercase the data, and to to remove the emojis python functions were used. Natural Language Processing algorithm has been used for preprocessing. The preprocessing steps were carried out using two different types of tools and compared the result both in python and Tableau. Those are Natural Language processing tool kit and spacy. Spacy has given the better result compared to nltk also known as National Language Processing tool kit. For this project I skipped the step normalization and performed only two steps,one is text tokenization and the other is stopwords removal. I took the stopword 'not' from both the default stopwords from the tools. Then the sentiment analysis was done using the new tokenized data. Considering the polarity, the analysis was divided into three positive, negative and neutral. Meaning, if the polarity is less than 0 the analysis isnegative and if its equal to 0 the analysis is neutral and if its greater than 0 the analysis is positive. At the end I visualized the data in Tableau and displayed the results which i found.

## Data set

The data set was extracted from the twitter using the python module called snscrape. The sample data has 24668 tweets. Those extracted tweets are from the timeframe from 20th July 2021 to 22nd July 2021 for the the search terms '#Bezos','#Blueorigin'and '#BezosInSpace'. The extracted data were converted into an .csv format using pandas dataframe library. The features I have selected for the analysis was tweets and the location of the people from where they tweeted. 
## Data Cleaning

Data cleaning is the process of correcting, deleting or replacing the irrelevant parts from the data. The end product I needed was the clean text. So, I had to clean the complete data with the following three steps.
#### Steps
1. Remove hyperlink, special characters, numbers, punctuation
3. Remove Emojis
4. Make it lower case [to see the python code](https://github.com/Sathiya1611/Ironhack_Final_project/blob/main/Final_project.ipynb)

## Data Preprocessing

The data preprocessing was carried out using the two important tools in NLP. Those are Natural Language Processing Toolkit also known as nltk and Spacy. The nltk includes all the algorithms used for complete data preprcessing such as tokenizing, stopword removal, stemming, normalization and Sentiment analysis and Vectorization. Spacy also a text preprocessing toolkit. But, both works similar with few differences. Some of them are, the nltk has 179 default stopwords whereas Spacy has 326 stopwords also practically when you pass string input to nltk it gives you string output whereas Spacy works in object format. 
1. Text tokenization<br/>
Tokenization is the process of spilitting the complete into tokens. 
2. Stopwords removal<br/>
Stopwords are the words which doesn't makes much sense to sentence e.g., pronouns, conjunctions, preposition etc., In my project, I removed the word 'not' from the default stopword because when people comment as 'not a good idea', after removing the stopword the system will only take as 'a good idea'. So, the sentiment analysis will be opposite. Inorder to avoid that confusion I did so. 
There are other preprocessing steps as well, however in my work I used only two of them. 
## Sentiment Analysis
Sentiment Analysis, also known as knowing the emotional or opinion tone of the text. It helps to analyse the attitude of people who comment/gives review in the social media or in any platform. Inorder to analyse the Sentiment one first need to find the polarity. The polarity changes according to the opinion/text and it lies between the range of -1 to 1 and when its greater then 0 its positive, when its less than 0 its negative and 0 is neutral. 
#### Steps
1. Calculate the polarity
2. Calculate the subjectivity 
3. Calculate the analysis<br/>
The below image shows the Sentiment Analysis performed using nltk
<p align="center">
  <img src="https://github.com/Sathiya1611/Ironhack_Final_project/blob/main/Images/sentiment_nltk.png" />
</p>
The below image shows the Sentiment Analysis performed using Spacy
<p align="center">
  <img src="https://github.com/Sathiya1611/Ironhack_Final_project/blob/main/Images/sentiment_spacy.png" />
</p>

## Visualization

The visualization was performed using the BI Tableau. The data were fed into it and the visualization has been done [see here](https://github.com/Sathiya1611/Ironhack_Final_project/tree/main/Images). The below picture shows the number of percentage of votes from different locations.

<p align="center">
  <img src="https://github.com/Sathiya1611/Ironhack_Final_project/blob/main/Images/top5.png" />
</p>

## Insights
After the analysis, I iterated over the positive comments and found the system has detected the sarcastic tweets as positive. So, I was interested to know the reason. So I looked for the most frequent words in the positive comments and did some background research
<p align="center">
  <img src="https://github.com/Sathiya1611/Ironhack_Final_project/blob/main/Images/wordcloud.png" />
</p>

#### Most frequent words
1. Billionaires                                   - people think capitalism?
2. Tax                                            - the result of 2021 article which says, Bezos pays less than 1% tax? Source: Propublica
3. Employee                                       - reflection of 2018 protest of amazon  employees?
4. Indecent(objectionable) terms                  - could be the reason of his phone hack in 2018?
5. Rich, money                                    - could be the common depressive comments?
                                                       
## Conclusion

Since the data has more sarcastic tweets the system was unable to process it good, so the system divided even the sarcasm comments as positive. So, potential way to use the sentimal analysis is where people comment in any two ways, meaning positive or negative. Always, a project is about learning and implement what I learned in the next project.  So, for the same data we can do sarcasm detection and perform further machine learning approach.




# Ironhack_Final_project
## Sentiment Analysis on Twitter data using NLP

![space_bezos_image](https://user-images.githubusercontent.com/60324758/127534104-02e1b270-4b1a-44fd-9ab1-c9f23c2659c1.jpg)

The main aim of this project is to analyze the sentiment (positive or negative) on Twitter data. In particularly people revieww on Jeff Bezos(the CEO of Amazon and Blueorigin)first space flight on 20th July 2021.

## Introduction
The data used for this analysis was extracted from twitter using the python module called snscrape. Snscrape helps to pull unlimited data. This is a great advantage over Twitter API. The data cleaning was done using the library called regex,to lowercase the data, and to to remove the emojis python functions were used. Natural Language Processing algorithm has been used for preprocessing. The preprocessing steps were carried out using two different types of tools and compared the result both in python and Tableau. Those are Natural Language processing tool kit and spacy. Spacy has given the better result compared to nltk also known as National Language Processing tool kit. For this project I skipped the step normalization and performed only two steps,one is text tokenization and the other is stopwords removal. I took the stopword 'not' from both the default stopwords from the tools. Then the sentiment analysis was done using the new tokenized data. Considering the polarity, the analysis was divided into three positive, negative and neutral. Meaning, if the polarity is less than 0 the analysis isnegative and if its equal to 0 the analysis is neutral and if its greater than 0 the analysis is positive. At the end I visualized the data in Tableau and displayed the results which i found.

## Data Cleaning
#### Steps
1. Remove hyperlink, special characters, numbers, punctuation
2. Remove Emojis
3. Make it lower case

## Data Preprocessing

With the help of two tools named spacy and nltk the preprocessing has been done.The following steps were taken care during the preprocessing.
1. Text tokenization
2. Stopwords removal

## Sentiment Analysis
#### Steps
1. Calculate the polarity
2. Calculate the subjectivity 
3. Calculate the analysis

## Visualization

The data were fed into Tableau BI and the visualization has been done.[Images]() 

## Conclusion

Since the data has more sarcasm the computer was unable to process it good. Because, the system divided even the sarcasm comments as positive. So, potential way to use the sentimal analysis is where people comment in any two ways meaning in positive or negative.
Always, a project is about learning and implement what I learn in one project in the next one. So, for the same data we can do sarcasm detection and do the further machine learning approach.




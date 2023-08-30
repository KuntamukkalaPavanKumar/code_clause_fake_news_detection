# FAKE NEWS DETECTION USING NLP AND MACHINE LEARNING MODELS
> In this information age, there is lot of room for misinformation to spread fast than credible information. To inform users of whether the information is fake or not has become a great importance. This project deploys Natural Language Processing (NLP) techniques for pre processing fake news articles. Then a machine learning model been developed to detect fake news.
![Word_Cloud](https://github.com/KuntamukkalaPavanKumar/code_clause_fake_news_detection/blob/main/wordcloudfakenews.png)


## Table of Contents
* [Dataset](#data-set)
* [Procedure](#procedure)
* [Conclusions](#conclusions)


## Data-Set
- The Data is openly avaialable on kaggle website (https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)
- The data consists of two .csv files. One is True news .csv file and other is fake news .csv file.
- Each .csv file contains 4 columns 'title', 'text', 'subject', 'date'
- A column named 'trueorfake' is created and assigned '1' for true news and '0' for fake news.

## Procedure:
1. Loading Dataset
2. Exploratory Data Analysis
3. Data Cleaning:
- This involved following steps:
    - There are some cells in 'text' column which contained only single space or double space. Those rows are completely removed.
    - The alphabets in text is converted to lower case.
    - The special characters present in the text are substituted with white space.
    - The text is broken down to word tokens used word_tokenize function
    - Then WordNetLemmatizer() is used to lemmatize the word tokens. Since using StemPorter or SnowballPorter are not properly converting words to their root form.
4. Model building:
- Train Test Splitting Data
- TFIDF Vectorizing the train and test data:
    - Only Train data is fitted and transformed using TfidfVectorizer()
    - The Test data is only transformeed using TfidfVectorizer()
- Model Building:
    - Logistic Regression:
        - An accuracy score of 99% is acheived in classifying news as fake or true on test dataset.
    - Decision Tree Classifier:
        - An accuracy score of 100% is acheived in classifying news as fake or true on test dataset.

## Conclusions:
1. Both Logistic Regression and Decision Tree Classifier gave good performance in detecting fake news.

## Contact
Created by [@KuntamukkalaPavanKumar] - feel free to contact me!

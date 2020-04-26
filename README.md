"# reditt-flair-detector" 
created reditt flair detector from word2vec model created web app successfully using flask .
extracted data using praw
I took following steps to build this project
- first i extracted data using praw library you can find its code in part 1 extracting data notebook
- then i did data anlysis in exploratory data anlysis
- i further preprocessed data by removing stop words,lemmatization,stemming
- then i used different nltk libraries like tf-idf,word2vec,bag of words out of all word2vec gave smallest eucledian distance thus used word 2 vec for predicting flair
- further i used  flask library in app.py to make basic web app which predicted label
- to choose label of given article i used following algorithm selcted top 10 headline based on eucledian distance and then based on headline with maximum frequency i outputted it's label
- https://post-flair-detector.herokuapp.com/ (heroku app)
- in app.py file i used word2vec to find vector representation of given link
- vector_representation.csv contains vector representation of headlines in mour word corpus(as it is time consuming to find vector representaion of each and every word i stored it in csv file)
- data1.csv contains all the data
- df2.csv contains all the data after preprocessing of data 

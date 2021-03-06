# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

### GA Project 3

**The Data Science Process**
- Problem Statement
- Data Collection
- Data Cleaning & EDA
- Preprocessing & Modeling
- Evaluation and Conceptual Understanding
- Conclusion and Recommendations

###  Background

When performing maintenance, an engineer accidentally deleted multiple posts from r/nottheonion and r/theonion. Unfortunately, the engineer was only able to recover the titles of the lost posts. We were therefore tasked to build a classification model which would train on posts submitted before 01 Jan 2022 to classify the recovered posts back to their respective subreddits, r/nottheonion and r/theonion, based solely on the post titles.

This model would also be used as a proof of concept for the development of an automated moderator which would automatically delete posts that do not belong to the subreddit that they are posted to. There has been an increase in bots spamming subreddits with irrelevant posts. Moderators have been spending a substantial amount of their time reviewing user reports and deleting spam posts from the subreddit. Having automated moderators police the subreddit for spam posts would free up time for human moderators, who are volunteers, to do things that they want to do.


### Problem Statement

- Is it clear what the goal of the project is?
build a classification model which would train on posts submitted before 01 Jan 2022 to classify the recovered posts back to their respective subreddits, r/nottheonion and r/theonion,

- What type of model will be developed?
we will be looking at logistic regression and MultinomialNB. with countvectorizer and TfidfVectorizer

- Is it clear who cares about this or why this is important to investigate?
There has been an increase in bots spamming subreddits with irrelevant posts. Moderators have been spending a substantial amount of their time reviewing user reports and deleting spam posts from the subreddit.
A: It helps to be efficient in dealing with subsreddits , where human moderators and spedn their time monitoring other important task.







### Data Collection
subsreddit used: r/TheOnion vs r/nottheonion
- Web Data Scraping Using Pushshift API
- Scrape ~2.5k posts from r/TheOnion & r/nottheonion, total of ~4.2k posts. 
- Used from psaw import PushshiftAPI to acquire data. Clean the data.
- Export as two individual .csv
Was enough data gathered to generate a significant result?
A: more than 500 posts 
Was data collected that was useful and relevant to the project?
A: as project problem suggest it is revelent.

---
### Data Cleaning & EDA
First cleaning the data: 
- apply regex to drop duplicates and numbers (lemminization and tokenize later in preprocessing)
- check for Null value (we have none this case, since we are not dealing with comment only post titles)

Finding out most active Authors , so we know how balance are our data is

r/TheOnion: Bar plot- Most Active Authors
![image.png](https://postimg.cc/t7mr2wKD)

r/nottheonion: Bar plot- Most Active Authors
![image.png](https://postimg.cc/cghzxJ5N)

Next i decided to find most refence Domain 

r/TheOnion: Bar plot- Most Ref Domain
![image.png](https://postimg.cc/Xr5DZLDL)
r/nottheonion: Bar plot- Most Ref Domain
![image.png](https://postimg.cc/f3hqYdGN)

This enable us to have a clearer view on what data we are handling.

concat two dataframe and perform CountVectorizer() to obtain Unigram and Bigram which 
resulted :

- Unigrams: words
- Bigrams: Covid-19 and Year Old

I perform trigram but there is not common word between the two dataset
Export to csv file

---
### Modelling
Are methods such as stop words, stemming, and lemmatization explored?
lemmatization was perform before finding out n-grams(uni /bi)

- CountVectorizer & Logistic Regression
Best score: 0.7750549795790135
Train score 0.9987433239082626
Test score 0.763430725730443

- CountVectorizer & MultinomialNB (Best Score)
Best score: 0.7841658812441094
Train score 0.9971724787935909
Test score 0.7785108388312912

- TfidfVectorize & Logistic Regression
Best score: 0.763430725730443
Train score 0.9274269557021678
Test score 0.767200754005655

- TfidfVectorizer & MultinomialNB
Best score: 0.753697560301334
Train score 0.8846999685830977
Test score 0.7483506126295947

I have decided to use NB + countvector as it gives a better score compare to Logis regress
Best model is CountVectorizer & MultinomialNB

Performed Confuse Matrix
![image.png](https://postimg.cc/4mSrHm4f)




Accuracy: 77.85 %
Precision: 78.08 %
Recall: 82.79 %
Specificity: 71.88 %
Misclassification Rate: 25.41 %

### Baseline Score ###
my baseline score: 
TheOnion  :    1    0.547597
nottheonion :  0    0.452403

### Conclusions & recommendations

The most model to optimize for accuracy in detecting recovered news, identifying(classifying) it to be fake news or absurd news would CountVectorizer and MultinomialDB. The optimal parameters for this model are where ngram_range = (1,3) and alpha = 0.6.

Accuracy: 77.85 %
Precision: 78.08 %
Recall: 82.79 %
Specificity: 71.88 %
Misclassification Rate: 25.41 %

interpretation of coefficients, I used CountVectorizer & Logistic Regression model.

The word that contributes the most positively to being from r/TheOnion is 'onion' followed by 'nation' and 'announces '.
    This means that  "onion" increase by 1 in a title, that title is 8.84 times as likely to be classified in to  r/TheOnion subreddit.
    
---------------------
The word that contributes the most positively to being from r/nottheonion is 'content ' followed by 'nft ' and 'christmas'.
   This means that  "content" increase by 1 in a title, that title is 20.15 times as likely to be classified as r/nottheonion.

- Model sufficiently good to classify posts 78%
- Machine learning Model feasible for automation moderation.
Some ideas for improvement :
- extract more data collection for use to train models.
- examine more text closely
- engineer metadata as additional features







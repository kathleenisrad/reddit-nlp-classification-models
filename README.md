# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

### Problem Statement
The goal of this project is to make a model that predicts whether a post came from the r/history subreddit or the r/worldnews subreddit.
I want to be able to distinguish whether and event is a current one or a historical one.

### Models:
I will compare multiple models based on time and accuracy- LogisticRegression, RandomForestClassifier, DecisionTreeClassifier, GradientBoost.
Success will be evaluated based off of accuracy score and how it compares with each other as well as the baseline accuracy score.

### Data:
I made a function to scrape posts off of the history and world news subreddits. 

I trained the models on TfidfVectorized text. TfidfVectorizer breaks down texts into individual words, or tokens, and then weights the tokens in a way that token classes are equalized. That way, words that appear a lot don't have too much weight over words that appear infrequently.

### Findings:

|models	|training accuracy	|testing accuracy|	time|
--------|-------------------|----------------|------|
|baseline	|0.505957	|0.505957	|998 µs|
|logistic regression	|0.957181|	0.901668	|18 s|
|random forest	|0.999495|	0.874594	|3min 16s|
|random forest (grid search)|	0.999495	|0.902751	|33min 11s|
|decision tree	|0.999495	|0.840589	|20min 33s|
|gradient boost|	0.768792	|0.754169	|1h 5min 48s|


### Conclusions and Recommendations:
Logistic Regression was the fastest and actually did pretty well. It had an even amount of false positives and false negatives, which is fine in this case. 
If someone wanted to minimize false positives, I would recommend the Random Forest and gridsearch for best hyperparameters to improve accuracy.

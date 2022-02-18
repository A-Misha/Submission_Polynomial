# Submission_Polynomial
POLYNOMIAL.AI INTERNSHIP RECRUITMENT DRIVE

MACHINE LEARNING / NLP

PROBLEM STATEMENT:
Given a dataset of Amazon product reviews for the year 2017-2018 for the category Cell Phones and accessories along with some metadata.

The outline is as follow:
1. Data overview (classification problem)
2. Text preprocessing (removing ,stopwords http, lowercase, etc…)
3. Word embedding technique (TF-IDF)
4. Analyzing technique (Linear Regression,Ridge Classifier and MultinomialNB)
5. Selecting model and run accuracy test (F1, precision vs recall, confusion matrix)

1.DATA OVERVIEW

In this analysis, we are going to use the Amazon product reviews dataset where there are positive and negative reviews.The data can be found in the zipfile.

2.TEXT PREPROCESSING

When people write reviews, it can be informal language, for example, yours and urs. Machine will understand it as different word if we don’t teach them. This is only an example problem that text analysis is facing. Other problems may include misspelling, capital letter, etc.. We need to handle these problems by doing text preprocessing.

a.Remove none text and special character
With the review data that we have, we have <br> which is not consider as text in the context. It has no meaning and won’t provide any good information for the model, therefore it must be removed. In other text analysis scenario, text data might include website link, hashtags etc… These things better be removed from the text before we run the model.

b. Convert all text to lowercase
To avoid the mistake during the training that the word like “We” and “we” might get learn differently, we turn all words with capital letter into lower cases.

c.Remove stopword
Stopwords are words such as ‘I’, ‘we’, ‘my’, ‘you’ etc… These words are not likely to represent particular meaning. The model might consider this as noise, so we remove it as to keep noise level down

d.Turn sentiment into categorical value
When we dealing with categorical data, we can turn these text categories into numbers. For example, yes and no categories can be turn into 1 and 0. In these case, we have the negative and positive sentiment. We are going to turn them into values of 0 and 1.

3. WORD EMBEDDING TECHNIQUE

Now, before we use the machine learning to further implementing the sentiment analysis, we need to turn those texts into numerical values, this is known as vector representative for the words.
We are using Tf-idf. It measures how important is the term across all documents and we find out how important each word is in the document. To apply this technique, we can use TdidfVectorizer from sklearn.

4.ANALYSING MODELS

We are training the folllowing models and finding out which one gives the maximum accuracy.
a.Ridge Classifier
b.MultinomialNB
c.Linear Regression
We also can use F1 scores and select the model with highest average F1 score.

5.SELECT MODEL AND RUN ACCURACY TEST

To measure the accuracy of the prediction, one of the simplest technique is the accuracy test.

CONCLUSION
With the  Amazon product reviews dataset, I have train the model with three models, linear regression, ridge and multinomialNB, and compare accuracies by using F1 score. With linear regression, I received 83.31% accuracy for the sentiment prediction.

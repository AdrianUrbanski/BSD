# BSD - fake news detection
This is a group project for a university machine learning course. In our team, I was responsible for implementing a model using Support Vector Machines. You can find it in the SVM notebook. The project summary notebook contains data analysis and comparison of all models (SVMs, boosted ensembles and Naive Bayes) presented in an orderly manner.
# Data
We used two datasets:  
* The first one we collected ourselves. It consists of 200 hand-picked articles (roughly half of them fake) from over 20 websites.  
* The second we found on kaggle.com [(link)](https://www.kaggle.com/clmentbisaillon/fake-and-real-news-dataset). Since it's huge (nearly 40k articles) and quite popular, we thought that it would allow us to train a reliable model, but it turned out that almost all true articles were scraped from the same site. Moreover, the articles had the website name in their content, so a simple if check was enough to achieve over 99% accuracy. No wonder people on kaggle were able to train neural networks that worked so well!
# Extracted features
Before training our models, we first had to preprocess contents of the articles, extracting following features:
* Bag of words and 2-grams
* Numerical values: number of words, frequency of adjectives, weird punctuation, uppercase words, subjectivity score etc
# Classifiers
We compared the results of three different classifiers:
* Support Vector Machines
* AdaBoost & XGBoost
* Naive bayes classifier

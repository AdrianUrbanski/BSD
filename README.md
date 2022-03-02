# BSD - fake news detection
This is a group project for a university machine learning course. 
The project summary notebook contains data analysis and comparison of all models (SVMs, boosted ensembles and Naive Bayes) presented in an orderly manner.
This project is a prime example of "garbage in, garbage out" rule - almost all the true articles from this dataset are from Reuters and include word "Reuters".
It was funny to see that the results on Kaggle achieved by people using state-of-the-art neural networks can be bested using simple if checking whether the word "Reuters" appears in the article!

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
* Support Vector Machines ([Adrian Urbański](https://github.com/AdrianUrbanski))
* AdaBoost & XGBoost ([Maria Wyrzykowska](https://github.com/Ruruthia))
* Naive bayes classifier ([Grzegorz Maliniak](https://github.com/Gizmon99))

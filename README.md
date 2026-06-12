IPL Sentiment Pipeline Challenge
Overview
This project builds an entity-aware sentiment classification pipeline for IPL-related fan posts written in Indian English and Hinglish.
The task is to predict whether the sentiment toward a given IPL team keyword is:
* Positive
* Negative
* Neutral
The model input format used throughout the project was:
subject_keyword + " [SEP] " + statement
This allows the model to learn sentiment toward a specific IPL team rather than only general sentiment.
Datasets
80-Row Dataset
Used for the initial experiment and model comparison.
300-Row Dataset
Used for validation and final model selection.
Methodology
Vectorizers Evaluated
* CountVectorizer
* Binary CountVectorizer
* CountVectorizer (1-2 grams)
* TF-IDF Word
* TF-IDF Bigram
* Character TF-IDF
* Character Word-Boundary TF-IDF
* HashingVectorizer Word
* HashingVectorizer Character
* TF-IDF + SVD
Classifiers Evaluated
* Multinomial Naive Bayes
* Complement Naive Bayes
* Bernoulli Naive Bayes
* Logistic Regression
* Ridge Classifier
* LinearSVC
* SGD Classifier (Log Loss)
* SGD Classifier (Hinge Loss)
* Passive Aggressive Classifier
* Random Forest
A total of 100 pipelines were evaluated on the 80-row dataset.
The top-performing approaches were then evaluated on the 300-row dataset.
Why These Methods Were Chosen
I wanted to compare different ways of representing text rather than relying on a single approach. Binary CountVectorizer was chosen to test word presence, TF-IDF Word to measure word importance, CountVectorizer (1-2 grams) to capture short phrases, and HashingVectorizer to evaluate a scalable vocabulary-free method.
For classifiers, I selected Complement Naive Bayes, Logistic Regression, Ridge Classifier, and LinearSVC because they are widely used for text classification, efficient on sparse text features, easy to interpret, and represent different learning approaches. Final selections were based on performance, efficiency, simplicity, diversity, and consistency across both the 80-row and 300-row datasets.
Final Selected Vectorizers
1. Binary CountVectorizer
2. TF-IDF Word
3. HashingVectorizer Word
4. CountVectorizer (1-2 grams)
Final Selected Classifiers
1. Ridge Classifier
2. Complement Naive Bayes
3. Logistic Regression (Balanced)
4. LinearSVC
Selection Strategy
Model selection was not based solely on accuracy.
The final choices were selected using:
* Accuracy
* Macro F1 Score
* Generalization across datasets
* Simplicity
* Efficiency
* Diversity of approaches
* Avoidance of heavy or near-duplicate models
Files Included
* completed_notebook.ipynb
* submission_manifest.json
* results_80R.csv
* results_300R.csv
* justification.md
* requirements.txt
Author
Aahan Lulla
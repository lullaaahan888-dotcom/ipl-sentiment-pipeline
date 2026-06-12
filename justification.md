Justification of Final Model Selection
Objective
The goal was to build an entity-aware sentiment classification pipeline for IPL fan posts written in noisy Indian English and Hinglish while balancing accuracy, simplicity, efficiency, and diversity.
Final Vectorizers
Binary CountVectorizer
Selected because it focuses on whether important words are present rather than how many times they appear. It performed consistently across experiments and remained simple and efficient.
CountVectorizer (1-2 grams)
Selected to capture short phrases and common sentiment patterns that single words may miss.
TF-IDF Word
Selected because it gives greater importance to informative words while reducing the impact of very common terms.
HashingVectorizer Word
Selected as a scalable alternative that does not require storing a vocabulary and represents a different vectorization approach.
Final Classifiers
Complement Naive Bayes
Fast, lightweight, and well suited to text classification tasks.
Logistic Regression (Balanced)
A strong and interpretable baseline that performed consistently across datasets.
Ridge Classifier
Provided strong performance while remaining simple and computationally efficient.
LinearSVC
A widely used margin-based classifier that performs well on sparse text data.
Final Decision Process
Model selection was not based solely on accuracy. Final choices were made by considering:
* Performance on both 80-row and 300-row datasets
* Macro F1 score
* Simplicity and efficiency
* Diversity of techniques
* Generalization ability
* Avoidance of unnecessary model complexity
Several pipelines achieved extremely high accuracy on the 300-row dataset. Therefore, final selections were based on overall robustness and diversity rather than accuracy alone.
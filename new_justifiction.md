Justification of Final Model Selection
Objective
The goal was to build an entity-aware sentiment classification pipeline for IPL fan posts written in noisy Indian English and Hinglish while balancing accuracy, simplicity, efficiency, and diversity.
Final Vectorizers
Binary CountVectorizer
Selected because it focuses on whether important words are present rather than how many times they appear. It consistently performed well across experiments and remained simple and efficient.
TF-IDF Word
Selected because it assigns greater importance to informative words while reducing the influence of very common terms. It provided a strong and widely used text representation baseline.
HashingVectorizer Word
Selected to represent a scalable, vocabulary-free approach. Although it was not always the highest-scoring method, it increased diversity within the final model set and demonstrated an alternative feature representation strategy.
CountVectorizer (1-2 grams)
Selected because it captures short phrases and common sentiment expressions that may not be fully represented by individual words.
Final Classifiers
Complement Naive Bayes
A fast and effective probabilistic classifier that performed competitively on text classification tasks.
Logistic Regression (Balanced)
A strong and interpretable linear model that provided consistent performance across datasets.
Ridge Classifier
Selected for its simplicity, efficiency, and strong overall results during experimentation.
LinearSVC
A widely used margin-based classifier that performs well on sparse text features and provides a useful alternative learning approach.
Final Decision Process
Model selection was not based solely on accuracy. Final choices were made by considering:
* Accuracy
* Macro F1 Score
* Generalization across datasets
* Efficiency and training speed
* Simplicity and interpretability
* Diversity of vectorization and classification approaches
* Avoidance of unnecessary model complexity
The final set was chosen to balance performance, robustness, and methodological diversity rather than selecting only the highest-scoring models.
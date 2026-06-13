Error Analysis
Observations
During experimentation, model performance varied across different vectorization and classification approaches.
Count-based vectorizers consistently performed among the strongest methods, while TF-IDF-based approaches also remained competitive. Hashing-based methods provided useful diversity but generally achieved lower scores than the best count-based models.
The larger validation dataset produced more realistic performance scores than the initial experiment, highlighting the importance of evaluating models on datasets of different sizes.
Lessons Learned
* Entity-aware input improved sentiment prediction by explicitly including the IPL team keyword.
* Simpler linear and probabilistic models often performed competitively with more complex approaches.
* Comparing multiple vectorization strategies is important because representation choice significantly affects performance.
* Model selection should consider efficiency, diversity, and generalization rather than accuracy alone.
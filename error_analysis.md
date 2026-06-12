Error Analysis
Observations
During experimentation, model performance varied significantly across vectorization methods.
Count-based vectorizers consistently performed better than several TF-IDF and dimensionality-reduction approaches on the provided datasets.
Multiple pipelines achieved perfect accuracy on the 300-row dataset. While this may indicate that the dataset is highly separable, it also highlights the importance of evaluating models using multiple metrics rather than accuracy alone.
Lessons Learned
* Simpler models can perform competitively on sentiment classification tasks.
* Comparing diverse vectorization approaches is important because performance can vary considerably.
* Model selection should consider efficiency, simplicity, and consistency in addition to accuracy.
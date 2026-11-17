 ## Movie Reviews 
 
The goal of this project is to classify movie reviews as either positive or negative.



#### Dataset and evaluation

This project uses the [IMDb Large Movie Review Dataset](https://huggingface.co/datasets/stanfordnlp/imdb), accessed through Hugging Face.

The dataset contains three splits: `train` (25,000 labeled reviews), `test` (25,000 labeled reviews), and `unsupervised` (50,000 unlabeled reviews). The `train` split is cleaned and divided into training and development holdout sets for model comparison. After selecting the full-vocabulary LinearSVC, the notebook evaluates it once on the separate official `test` split. The `unsupervised` split is not used.

The dataset card lists English as the language and reports no missing values. It lists the license as `other`, so the review text is not included in this repository.

**Project structure**
1. Explore label balance, review lengths, missing values, duplicates, and HTML markup.
2. Clean HTML markup, remove duplicate training reviews, and split the data with stratification.
3. Fit TF-IDF on training text and compare Logistic Regression, two ANN configurations, and LinearSVC on the same development holdout set.
4. Evaluate the selected full-vocabulary LinearSVC on IMDb's official test split.
5. Inspect a small sample of misclassified official-test reviews.

The development holdout results are used for model comparison and may be optimistic after trying multiple models. The official-test result is the final evaluation and should not be used to tune model choices. Results on reviews from other sources may differ.



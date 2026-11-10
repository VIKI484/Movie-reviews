 ## Movie Reviews 
 
The goal of this project is to classify movie reviews as either positive or negative.



#### Dataset

This project uses the [IMDb Large Movie Review Dataset](https://huggingface.co/datasets/stanfordnlp/imdb), accessed through Hugging Face.

The dataset contains three splits: `train` (25,000 labeled reviews), `test` (25,000 labeled reviews), and `unsupervised` (50,000 unlabeled reviews). This project uses the `train` split, which is further divided into training and test sets. The official `test` and `unsupervised` splits are not used.

The dataset card lists English as the language and reports no missing values. It lists the license as `other`, so the review text is not included in this repository.



**Project structure**
1. Load the reviews and examine their length, language, and label distribution.
2. Create a simple baseline model using TF-IDF and logistic regression.
3. Train a small neural network for text classification. 
4. Compare the models using the same test data.
5. Examine the misclassified reviews - for example those containing ironi, negation, or mixed opinions.
6. Describe what improves or gets worse when using deep learning.






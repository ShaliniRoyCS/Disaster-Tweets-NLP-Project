## Overview
Twitter is a vital communication channel during emergencies. The widespread use of smartphones allows people to announce emergencies in real-time, which is invaluable for disaster relief organizations and news agencies. However, it can be challenging to determine if a tweet is genuinely about a disaster

## Objective
The goal is to predict whether a given tweet is about a real disaster (1) or not (0).

## Dataset
Each sample in the train and test sets contains the following information:

text: The text of the tweet

keyword: A keyword from the tweet (may be blank)

location: The location the tweet was sent from (may also be blank)


Columns in train.csv
id: A unique identifier for each tweet

text: The text of the tweet

location: The location the tweet was sent from (may be blank)

keyword: A particular keyword from the tweet (may be blank)

target: Indicates whether the tweet is about a real disaster (1) or not (0)

## Data Preprocessing and Model Training
### Required Libraries
We imported the necessary libraries including seaborn for visualization, matplotlib for plotting, numpy for numerical operations, pandas for data manipulation, TensorFlow and Keras for building the machine learning model, KerasNLP for natural language processing, and scikit-learn for metrics and splitting the data.

### Data Visualization
Target Distribution: We visualized the distribution of the target variable to understand the balance between disaster and non-disaster tweets.


Tweet Length Distribution: We visualized the distribution of tweet lengths in both the training and test sets to understand the text length variability.

### Model Selection and Preparation
DistilBERT Model: Loaded a pre-trained DistilBERT model and its tokenizer from KerasNLP for text preprocessing and classification.


Preprocessor: Configured the preprocessor with a sequence length suitable for tweets.


Classifier: Set up the classifier with the DistilBERT backbone and defined it to classify tweets into two categories (disaster or non-disaster).
### Model Compilation and Training
Compile the Model: Compiled the model with the Adam optimizer, Sparse Categorical Crossentropy loss, and accuracy as a metric.


Fit the Model: Trained the model on the training data and validated it using the validation set over two epochs.

### Model Evaluation
After training the DistilBERT model, we evaluated its performance on both the training and validation datasets. The results were as follows:

Final Training Accuracy: 85.04%


Final Validation Accuracy: 84.24%

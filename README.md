# Cross-Domain Sentiment Analysis Using Amazon, IMDB, and Yelp Reviews
## Overview
This project develops a sentiment analysis pipeline to classify customer reviews as positive or negative using text data from multiple domains. The analysis integrates three datasets containing labelled reviews from Amazon product reviews, IMDB movie reviews, and Yelp restaurant reviews.

The objective is to explore whether a single machine learning pipeline can effectively perform sentiment classification across different review domains.

Dataset
The dataset was obtained from the UCI Machine Learning Repository.

Source:
https://archive.ics.uci.edu/dataset/331/sentiment+labelled+sentences

The dataset consists of:
- Amazon product reviews
- IMDB movie reviews
- Yelp restaurant reviews

Each dataset contains short review sentences labelled as:
1 → Positive sentiment
0 → Negative sentiment

Originally the dataset should contain 3,000 reviews (1,000 per source).

## Project Workflow
### Data Extraction
The datasets are retrieved and imported into the analysis environment. Initial inspection ensures that the data structure is consistent across the three sources.

### Data Cleaning and Preparation
Several preprocessing steps are performed to ensure data quality:
Handling irregular rows in the IMDB dataset
Splitting multi-sentence entries into individual reviews
Standardising the dataset structure
Merging all datasets into a single dataframe
These steps ensure that each row represents one review with its corresponding sentiment label.

### Exploratory Data Analysis (EDA)
Exploratory analysis is conducted to understand dataset characteristics and identify potential issues.

Key aspects analysed include:
Dataset size and structure
Distribution of sentiment labels
Review length distribution
Differences between data sources
This stage helps identify patterns and validate dataset integrity before modelling.

### Text Preprocessing
Natural Language Processing (NLP) techniques are applied to prepare the text for machine learning models.
Processing steps include:
Lowercasing text
Removing punctuation
Removing stopwords
Tokenisation
Text normalisation
These steps reduce noise and improve model performance.

### Feature Engineering
Text data is transformed into numerical features using TF-IDF (Term Frequency–Inverse Document Frequency) vectorisation.
TF-IDF represents each review as a vector based on the importance of words within the dataset.

### Model Development
Machine learning classification algorithms are used to predict sentiment from review text.

Models implemented include:
- Logistic Regression
- Support Vector Machine (SVM)

These models are trained on the processed text features.

### Model Evaluation
Model performance is evaluated using classification metrics such as:
Accuracy
Precision
Recall
F1-Score

### Confusion Matrix
Evaluation results provide insight into how effectively the models classify sentiment across different review domains.
Technologies Used
Python
Pandas
NumPy
Scikit-learn
NLTK / text preprocessing tools
Matplotlib
Seaborn
Jupyter Notebook

Key Insights
The analysis demonstrates that machine learning models can successfully classify sentiment from short text reviews across multiple domains. Proper text preprocessing and feature extraction play a critical role in achieving accurate sentiment predictions.

# NLP_Assignment

PART - A
Task Extraction and Categorization (Interview Assignment)
Overview
This repository contains a heuristic-based NLP pipeline to extract and categorize tasks from unstructured text. The system identifies action items, responsible entities, and deadlines without relying on pre-trained language models (LLMs).

Objective
The goal is to develop a Python-based solution that:

✅ Identifies task-related sentences from unstructured text.

✅ Extracts who is responsible, what needs to be done, and when it should be completed.

✅ Categorizes extracted tasks into meaningful groups using word embeddings and topic modeling.


Approach

The task extraction pipeline follows these steps:

1️⃣ Preprocessing


✔ Convert text to lowercase.

✔ Remove stopwords, punctuation, and special characters.

✔ Perform POS tagging and dependency parsing using spaCy.

2️⃣ Task Identification


✔ Identify imperative sentences starting with action verbs (e.g., "Submit the report").

✔ Detect action verbs, assignment phrases, and time constraints using heuristics.

✔ Extract verbs from text dynamically instead of using predefined lists.

3️⃣ Task Details Extraction


✔ Identify who is responsible using Named Entity Recognition (NER).

✔ Extract the main verb and its object as the task.

✔ Detect deadlines using regex and date/time parsing.

4️⃣ Categorization


✔ Apply TF-IDF and BERT embeddings to group similar tasks.

✔ Use Latent Dirichlet Allocation (LDA) to generate dynamic topic-based categories.

✔ Assign meaningful cluster names automatically.

5️⃣ Output Structured Data


✔ Store extracted tasks in CSV and JSON formats.

✔ Output includes: task, responsible_entity, deadline, category, and cluster_id.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

PART - B

Sentiment Analysis on Customer Reviews

📌 Project Overview

This project builds a machine learning model to classify customer reviews as positive or negative using NLP techniques. It covers data preprocessing, feature extraction, model training, and evaluation using different classification models.

📂 Dataset

Dataset Used: Amazon Alexa Reviews

Description: The dataset contains customer reviews of Alexa products, with a corresponding feedback label (0 = Negative, 1 = Positive).

🛠 Steps Followed

1️⃣ Data Collection

Used Amazon Alexa Reviews dataset from Kaggle.

Loaded the dataset using pandas.

2️⃣ Data Preprocessing

Text Cleaning: Removed special characters, digits, and stop words.

Lowercasing & Tokenization: Converted text to lowercase and tokenized sentences into words.

Stemming: Used PorterStemmer to reduce words to their root form.

3️⃣ Feature Extraction

Used TF-IDF (Term Frequency-Inverse Document Frequency) instead of Bag of Words (BoW).

Why TF-IDF?

TF-IDF assigns higher importance to rare words, improving text representation.
Unlike BoW, it reduces the weight of common words that appear frequently across all reviews.

4️⃣ Model Selection & Training

Implemented three ML models for text classification:

✅ Logistic Regression

✅ Naïve Bayes (MultinomialNB)

✅ Support Vector Machine (SVM)

Train-Test Split: Used an 80-20 split for training and testing.

Hyperparameter Tuning: Used GridSearchCV for optimizing SVM and Logistic Regression.

5️⃣ Evaluation

Used classification metrics:

📊 Accuracy

📊 Precision

📊 Recall

Visualization:

Compared BoW vs. TF-IDF performance using bar charts.

Plotted accuracy scores of different models.

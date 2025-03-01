# NLP_Assignment

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

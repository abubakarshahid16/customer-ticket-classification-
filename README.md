# customer-ticket-classification-
Customer Support Ticket Classification
This repository contains an end-to-end Machine Learning (ML) and Natural Language Processing (NLP) classification pipeline applied to a Customer Support Ticket Dataset. The project covers all stages, from data loading and exploratory data analysis (EDA) to model evaluation, including advanced NLP tasks such as Named Entity Recognition (NER), Topic Modeling, and more. Multiple classifiers are used to achieve top performance, including Logistic Regression, Decision Tree, Naive Bayes, SVM, KNN, and Random Forest.

Table of Contents
Dataset Description

Project Setup

Exploratory Data Analysis (EDA)

Data Preprocessing & Feature Engineering

NLP Tasks

Model Building

Model Evaluation

Conclusion

Submission

Dataset Description
The dataset used in this project is a Customer Support Ticket Dataset containing approximately 8,470 rows. It includes the following features:

Ticket ID: Numeric identifier for the ticket.

Product Purchased: Categorical feature indicating the product.

Ticket Type: Categorical feature for ticket type.

Ticket Priority: Categorical feature for the priority of the ticket.

Ticket Channel: Categorical feature for the support channel used.

Ticket Status: Categorical feature for ticket status.

Ticket Description: Text feature describing the issue raised in the ticket.

Ticket Subject: The target label for classification, with 16 possible classes.

The goal is to predict the Ticket Subject based on the other features, particularly leveraging the Ticket Description.


Install dependencies:

Since this project is executed on Google Colab, no need to set up virtual environments. Simply install the required libraries by running the following command in a Colab cell:

bash
Copy
Edit
!pip install -r requirements.txt
For specific NLP tasks, spaCy is used, and the model is downloaded as:

bash
Copy
Edit
!python -m spacy download en_core_web_sm
Exploratory Data Analysis (EDA)
The EDA involves visualizing both numerical and categorical features to understand data distribution and patterns.

Numerical Features: We explored numerical columns (like Ticket ID) using histograms and boxplots.

Categorical Features: We visualized categorical features (like Product Purchased, Ticket Type) using bar charts to show their frequency distribution.

Text Feature Analysis:

Word Cloud: We generated a word cloud to visualize the most common terms in Ticket Description.

Length Distribution: We plotted the distribution of the number of words per description to understand the text data better.

Sentiment Distribution: We used sentiment analysis to plot the distribution of sentiment in the dataset.

Data Preprocessing & Feature Engineering
Missing Values: Imputed missing values using suitable techniques for categorical and numerical columns.

Outlier Treatment: Outliers were detected and removed using statistical methods (e.g., IQR).

Text Cleaning: Cleaned the Ticket Description by:

Lowercasing all text.

Removing punctuation and special characters.

Tokenizing text and removing stopwords.

Categorical Encoding:

Used Label Encoding for binary categorical features.

Applied One-Hot Encoding for multi-class categorical features.

Scaling Numerical Features: Normalized numerical features using MinMax Scaling.

NLP Tasks
In this section, we demonstrated various NLP tasks:

Named Entity Recognition (NER):

Extracted named entities using spaCy and discussed how they could improve classification (e.g., identifying product names and issue types).

Topic Modeling:

Applied Latent Dirichlet Allocation (LDA) to group the ticket descriptions into topics, helping us understand common issues within tickets.

Sentiment Analysis:

Performed sentiment analysis using TextBlob and incorporated sentiment scores as additional features in the classification model.

Text Vectorization:

Converted the Ticket Description text data into numerical format using TF-IDF Vectorizer.

Model Building
We built several classification models and evaluated their performance:

Logistic Regression

Decision Tree

Naive Bayes

Support Vector Machine (SVM)

K-Nearest Neighbors (KNN)

Random Forest (optional, for improved performance)

Each model was trained on the preprocessed dataset, and hyperparameters were tuned to achieve optimal results.

Model Evaluation
The models were evaluated based on their confusion matrix and classification report, which includes precision, recall, and F1-score for each class.

We compared the results of different models before and after preprocessing steps like text cleaning and feature scaling.

Best Performing Model: After evaluation, the Random Forest classifier provided the best performance in terms of classification accuracy.

Conclusion
The classification pipeline successfully predicted the Ticket Subject based on various features, with an emphasis on the Ticket Description. The Random Forest classifier, combined with proper text preprocessing (e.g., tokenization, lemmatization) and feature engineering (e.g., sentiment scores), performed the best.

Key takeaways:

Textual data plays a crucial role in ticket classification.

Advanced NLP tasks like NER and Sentiment Analysis can significantly improve model performance.

Random Forest achieved the highest accuracy due to its ensemble nature and ability to handle diverse features.

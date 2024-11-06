# Social Media Personality Prediction using MBTI and NLP

This project analyzes social media data to identify linguistic patterns associated with MBTI personality types. By applying various NLP and machine learning (ML) techniques, we aim to predict a user’s MBTI classification based on their social media language. Our findings have potential applications in fields such as personalization, communication, HR, and mental health support.

Team Members
- Yifan Zhang
- Jackson Zhao
- Yueming Xu
- Zi Ting Ina Leung
- Prisha Samdarshi

## Background and Problem Statement

With the growing use of social media, vast amounts of data can provide insights into human behavior and personality. The Myers-Briggs Type Indicator (MBTI), a popular personality framework, categorizes individuals into 16 types based on four traits: Introversion/Extraversion, Sensing/Intuition, Thinking/Feeling, and Judging/Perceiving.

### This project aims to:
1. Discover linguistic patterns associated with each MBTI type.
2. Develop a model that can predict a user’s MBTI type based on social media text data.

### Potential Applications
- The project’s findings could enhance personalization, improve communication strategies, inform HR practices, and offer insights for mental health support.

## Data Description

The dataset includes over 8,600 rows sourced from Kaggle, where each row represents:
•	MBTI Type: One of the 16 personality types.
•	Posts: The user’s last 50 social media posts.

This data is particularly suitable for NLP and ML techniques to understand the relationship between language usage and personality traits.

## Project Workflow

1. Initial Data Exploration
•	Analyzed the structure, frequency of personality types, and initial data quality.
•	Examined common linguistic patterns across MBTI types, laying a foundation for further analysis.

2. Data Cleaning and Preprocessing
•	Removed URLs, standardized text by lowercasing, and removed delimiters.
•	Applied lemmatization and stopword removal for cleaner text features.

3. Feature Engineering
•	Transformed text data into numerical features using TF-IDF.
•	Conducted hyperparameter tuning on key models using RandomSearchCV.

4. Model Selection and Training
•	Logistic Regression (Achieved highest accuracy at 69%)
•	Support Vector Machine (SVM)
•	Random Forest
•	XGBoost

5. Results
The logistic regression model showed the best performance, achieving an accuracy of 69% following hyperparameter tuning. The Random Forest and XGBoost models also demonstrated moderate success in capturing relationships within the data.

6. Applications


## How to Run the Project

1.	Dependencies: Install the required libraries using requirements.txt.
```
pip install -r requirements.txt
```

2.	Notebook Execution: Run `main.ipynb` for data preprocessing, model training, and evaluation.

3.	Results Analysis: Review the saved model files or visualizations within the notebook to see detailed results by MBTI type.

Files in Repository

	•	mbti_1.csv: Dataset containing MBTI types and social media posts.
	•	main.ipynb: Jupyter Notebook containing the entire workflow, from data exploration to model evaluation.
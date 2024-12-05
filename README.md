# Social Media Personality Prediction using MBTI and NLP

This project explores the relationship between social media language and MBTI personality types using Natural Language Processing (NLP) and Machine Learning (ML) techniques. By identifying distinct linguistic patterns, we aim to develop predictive models capable of classifying users’ MBTI personality types based on their social media posts. The findings have potential applications in personalization, communication strategy, human resource management, and mental health support.

Team Members
- Yifan Zhang
- Jackson Zhao
- Yueming Xu
- Zi Ting Ina Leung
- Prisha Samdarshi

## Background and Problem Statement

The Myers-Briggs Type Indicator (MBTI) categorizes individuals into 16 personality types based on four dichotomies:
- Introversion (I) / Extraversion (E)
- Sensing (S) / Intuition (N)
- Thinking (T) / Feeling (F)
- Judging (J) / Perceiving (P)

Social media, as a platform for self-expression, generates vast data sets that provide valuable insights into personality and behavior. This project leverages NLP and ML to bridge the gap between linguistic patterns and MBTI classifications.

### Objectives:
- Identify linguistic patterns unique to each MBTI type.
- Develop predictive models to classify MBTI types from social media text data.

### Potential Applications
- Enhanced personalization in products and services.
- Improved communication strategies for marketing and engagement.
- Streamlined recruitment and HR practices.
- Insights for mental health support and well-being.

## Data Description
- The dataset includes over 8,600 rows sourced from Kaggle, where each row represents:
- **MBTI Type**: One of the 16 personality types.
- **Posts**: The user’s last 50 social media posts.

This data is particularly suitable for NLP and ML techniques to understand the relationship between language usage and personality traits.

## Exploratory Data Analysis (EDA)
1. **Linguistic Analysis**
- Neutral language predominates across posts, with subtle differences in emotional tone by personality type.
- Feeling (F) types tend to use more positive language than Thinking (T) types, aligning with their expressive traits.
2. **Post Length Analysis**
- No significant difference in average post length among MBTI types, though minor variations exist at the individual level.
3. **Word Choice**
- Introverts use reflective language, while extroverts use action-oriented words.
- **Common unigrams**: friend, want, way.
- **Common bigrams**: Memory-related phrases reflecting introspection and relationships.

## Preprocessing and Feature Engineering

1. **Cleaning**
- Removed special characters, URLs, and stopwords.
- Converted text to lowercase.
- Tokenized words and applied lemmatization for consistency.

2. **Feature Engineering**
- TF-IDF Vectorization: Extracted top 5,000 features capturing linguistic importance.
- Elastic-Net Regularization: Reduced noise and irrelevant features.
- Dimensionality Reduction: Applied Variance-based Reduction to reduce the remaining features.

3. **Class Balancing**
- Addressed imbalances using SMOTE, ensuring each personality type has 1,099 samples.

## Model Development

### Algorithms Tested
- Logistic Regression
- Support Vector Machines (SVM)
- Random Forest
- XGBoost
- Multi-Layer Perceptron (MLP)
- AdaBoost
- K-Nearest Neighbors (KNN)
- Decision Trees

### Performance on F-1 Score
1. Kernel SVM: 61.44%
2. XGBoost: 61.28%
2. Random Forest: 61.17%
3. Logistic Regression: 62.19%

### Hyperparameter Optimization
1. Random Search CV: Explored a broad hyperparameter space efficiently.
2. Bayesian Optimization: Fine-tuned the Random Forest model, achieving the best performance with:
- Max depth: 31
- Min samples per leaf: 1
- Estimators: 300

### Final Results
- Random Forest: F1-Score 62.97%, Accuracy 63.8%.
- While cross-validation results were strong, test set performance highlights opportunities to address overfitting and enhance generalization.

## How to Run the Project
- Dependencies: Install the required libraries using requirements.txt.

```
pip install -r requirements.txt

```

## Future Work
- **Overfitting Mitigation**: Incorporate advanced regularization techniques and alternative validation methods.
- **Feature Engineering**: Explore word embeddings like Word2Vec and BERT.
- **Model Deployment**: Build a web interface or API for real-world use cases.P
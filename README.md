# Sentiment Analysis Using Logistic Regression

This project demonstrates a sentiment analysis pipeline for IMDB movie reviews using logistic regression. The goal is to classify reviews as either positive or negative based on their text content.

## Dataset

The dataset used is the **IMDB Dataset of 50K Movie Reviews**, which contains two columns:
- **review**: The text of the review.
- **sentiment**: The label, either `positive` or `negative`.

## Steps Performed

### 1. Data Preprocessing
- **Tokenization**: The reviews were split into individual words.
- **Stopword Removal**: Common English words (like "the", "is", etc.) were removed to retain meaningful terms.
- **Lemmatization**: Words were reduced to their base forms (e.g., "running" → "run").
- **Text Vectorization**: The cleaned reviews were transformed into numerical format using the **TF-IDF** vectorizer, considering the top 5,000 features.

### 2. Model Training
- Logistic Regression was trained on 80% of the dataset.
- Labels were converted into binary values:
  - `1` for positive reviews.
  - `0` for negative reviews.

### 3. Evaluation
- The model's predictions on the test set (20% of the data) were evaluated using precision, recall, and F1-score.

## Requirements

Install the necessary Python libraries:
```bash
pip install nltk scikit-learn pandas

Observations
•	The logistic regression model achieved:
o	Precision: 0.90 for negative reviews and 0.88 for positive reviews.
o	Recall: 0.87 for negative reviews and 0.90 for positive reviews.
o	F1-Score: ~0.89 overall.


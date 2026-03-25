# News Category Classification

This repository contains a Jupyter Notebook demonstrating a basic text classification pipeline using `scikit-learn` and `spaCy` to categorize news articles.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Preprocessing](#preprocessing)
- [Model](#model)
- [Performance](#performance)
- [Confusion Matrix](#confusion-matrix)
- [Installation](#installation)
- [Usage](#usage)
- [Credits](#credits)
- [License](#license)

## Project Overview
This project aims to classify news articles into predefined categories. It showcases text preprocessing techniques (lemmatization, stop word removal) and a simple machine learning model (Multinomial Naive Bayes) for classification.

## Dataset
The dataset used for this project is a synthetic collection of 25 news articles with corresponding categories. A balanced subset of 12 articles (3 from each of 'Technology', 'Environment', 'Finance', and 'Health' categories) was created for training and testing.

## Preprocessing
Text preprocessing was performed using `spaCy` to:
- Remove stop words
- Remove punctuation
- Lemmatize words

This cleaned text was then used as input for the `CountVectorizer`.

## Model
A `Pipeline` consisting of `CountVectorizer` (with `ngram_range=(1, 2)`) and `MultinomialNB` was used for classification. The model was trained on the preprocessed news text.

## Performance
The model's performance was evaluated using a classification report. Due to the small dataset size, the performance metrics are as follows:

```
              precision    recall  f1-score   support

           0       0.00      0.00      0.00         1
           1       0.00      0.00      0.00         2
           2       0.50      1.00      0.67         1
           3       0.50      1.00      0.67         1

    accuracy                           0.40         5
   macro avg       0.25      0.50      0.33         5
weighted avg       0.20      0.40      0.27         5
```

*(Note: Precision, recall, and f1-score are low for some classes due to the limited number of samples in the test set.)*

## Confusion Matrix
The confusion matrix provides a visual representation of the model's performance on the test set

## Installation
To run this notebook, you will need the following Python libraries. You can install them using pip:

```bash
pip install pandas scikit-learn spacy matplotlib seaborn
python -m spacy download en_core_web_sm
```

## Usage
1. Clone the repository:
   ```bash
   git clone https://github.com/ArpanJana2002/N-gram-NLP
   cd ArpanJana2002/N-gram-NLP
   ```
2. Open and run the `news_classification.ipynb` notebook in your preferred environment (e.g., Jupyter, Google Colab).
3. Follow the steps in the notebook to preprocess data, train the model, and evaluate its performance.

## Credits
- This project was developed as part of a demonstration for text classification.

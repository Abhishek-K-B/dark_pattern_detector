# E-Commerce Dark Pattern Detection Using NLP and Machine Learning

## Project Overview

This project is a simple NLP and Machine Learning system developed to detect potentially manipulative **dark-pattern language** in e-commerce text.

E-commerce websites use messages such as:

* "Hurry! Only 2 items left!"
* "Limited time offer!"
* "Only a few items remaining!"

Such messages may create urgency, scarcity, or social pressure. This project uses Natural Language Processing (NLP) and Machine Learning to classify text as either **Dark Pattern** or **Not Dark Pattern**.

## Objectives

* Understand dark-pattern language in e-commerce.
* Clean and preprocess text data.
* Convert text into numerical features using TF-IDF.
* Train Logistic Regression and Naive Bayes models.
* Compare the performance of both models.
* Build a simple function for detecting dark-pattern text.

## Dataset

The project uses an e-commerce dark-pattern text dataset containing:

* **2,356 records**
* **4 original columns**
* `page_id`
* `text`
* `label`
* `Pattern Category`

The target variable contains two classes:

* `0` – Not Dark Pattern
* `1` – Dark Pattern

The dataset is balanced, with **1,178 records in each class**.

## Technologies Used

* Python
* Google Colab
* Pandas
* Regular Expressions (`re`)
* Scikit-learn
* Matplotlib
* Joblib

## Methodology

The project follows these steps:

```text
Dataset
   ↓
Text Preprocessing
   ↓
Train-Test Split
   ↓
TF-IDF Feature Extraction
   ↓
Machine Learning Models
   ↓
Prediction
   ↓
Evaluation
```

### Text Preprocessing

The text is:

* Converted to lowercase
* Cleaned by removing special characters
* Cleared of extra spaces

### TF-IDF

TF-IDF is used to convert the cleaned text into numerical features that can be processed by machine learning algorithms.

### Machine Learning Models

Two classification algorithms were trained:

1. Logistic Regression
2. Multinomial Naive Bayes

## Results

| Model               |   Accuracy |
| ------------------- | ---------: |
| Logistic Regression | **92.80%** |
| Naive Bayes         | **91.53%** |

Logistic Regression achieved the highest accuracy and was selected as the final model.

The Logistic Regression model correctly classified **438 out of 472** test samples.

## Sample Predictions

| Text                                | Prediction       |
| ----------------------------------- | ---------------- |
| "Hurry! Only 2 items left!"         | Dark Pattern     |
| "Limited time offer. Buy now!"      | Dark Pattern     |
| "The product is made from cotton."  | Not Dark Pattern |
| "This phone has a 5000mAh battery." | Not Dark Pattern |

## Limitations

* The dataset contains only 2,356 records.
* The model is mainly designed for e-commerce text.
* TF-IDF has limited understanding of sentence context.
* Some unseen sentences may be incorrectly classified.
* The model cannot verify whether a statement is actually true.
* The project focuses on text and does not analyze webpage design or visual elements.

## Future Scope

The project can be improved by:

* Using a larger and more diverse dataset.
* Using advanced NLP models such as BERT or Transformers.
* Detecting specific dark-pattern categories.
* Adding multilingual support.
* Developing a web or mobile application.
* Creating a browser extension for real-time detection.
* Combining text analysis with webpage layout and visual information.

## Project Structure

```text
E-Commerce-Dark-Pattern-Detection/
│
├── dark_pattern_detection.py
├── dataset.csv
├── NLP_Report.pdf
└── README.md
```

## Conclusion

This project demonstrates how basic NLP and Machine Learning techniques can be used to identify potentially manipulative language in e-commerce text.

TF-IDF was used for feature extraction, and Logistic Regression and Naive Bayes were compared. Logistic Regression achieved the best accuracy of **92.80%** and was selected as the final model.

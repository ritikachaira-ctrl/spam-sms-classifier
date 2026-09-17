# Spam SMS & Email Text Classifier

A machine learning project that classifies text messages as **SPAM** or **HAM (normal message)**.

## Objective

The goal of this project is to build a text classification model that can identify whether a given SMS or email message is spam.

## Dataset

The project uses the **SMS Spam Collection** dataset containing labeled messages as:
- `ham` — normal messages
- `spam` — unwanted/promotional messages

Duplicate messages were removed before training.

## Approach

The following steps were used:

1. Load and explore the dataset
2. Remove duplicate messages
3. Split the data into training and testing sets
4. Convert text into numerical features using **TF-IDF**
5. Train a **Multinomial Naive Bayes** classifier
6. Train a **Logistic Regression** classifier
7. Evaluate both models using accuracy and classification metrics
8. Visualize the results using a confusion matrix
9. Create an inference function for predicting new messages

## Models Used

- Multinomial Naive Bayes
- Logistic Regression

## Results

| Model | Accuracy | Spam Precision | Spam Recall | Spam F1-Score |
|---|---:|---:|---:|---:|
| Naive Bayes | 96.71% | 100.00% | 74.00% | 85.00% |
| Logistic Regression | 95.65% | 98.00% | 67.00% | 80.00% |

The results are based on the test split used in the notebook.

## Example Predictions

```text
"You have won a free lottery ticket! Claim your prize now."
Prediction: SPAM

"Can you send me the notes from today's class?"
Prediction: HAM

"URGENT! Your account has been selected for a cash reward."
Prediction: SPAM

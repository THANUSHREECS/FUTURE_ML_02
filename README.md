# FUTURE_ML_02
Support Ticket Classification &amp; Prioritization using Machine Learning

## 1. Introduction

In modern organizations, customer support teams handle a large number of tickets daily, including complaints, queries, and issue reports. Managing these tickets manually leads to inefficiencies such as delayed responses, incorrect categorization, and poor customer satisfaction.

This project aims to solve these challenges by developing a Machine Learning-based system that can automatically classify support tickets and assign priority levels based on their content.

## 2. Objectives

The main objectives of this project are:

* To preprocess and clean textual ticket data
* To convert text data into numerical features using TF-IDF
* To build classification models for:

  * Ticket Category
  * Ticket Priority
* To evaluate model performance using standard metrics
* To demonstrate real-world business impact

## 3. Dataset Description

The dataset consists of customer support ticket information with the following key columns:

* Ticket Subject
* Ticket Description
* Ticket Type (Category)
* Ticket Priority
* Additional fields such as customer details, timestamps, and resolution

For this project:

* Input Features: Ticket Subject + Ticket Description
* Target Variables:

  * Ticket Type (Category Classification)
  * Ticket Priority (Priority Prediction)
    
## 4. Methodology

### 4.1 Data Preprocessing

Text data is cleaned using Natural Language Processing (NLP) techniques:

* Lowercasing all text
* Removing punctuation and special characters
* Removing stopwords (common words like “the”, “is”)
* Tokenization (splitting text into words)

Additionally, Ticket Subject and Ticket Description are combined to capture more context.

### 4.2 Feature Extraction

We use **TF-IDF (Term Frequency - Inverse Document Frequency)** to convert text into numerical form.

* Assigns importance to meaningful words
* Reduces the impact of common words
* Helps machine learning models understand text

### 4.3 Model Building

Two separate models are trained:

#### 1. Category Classification Model

* Input: Cleaned ticket text
* Output: Ticket Type (e.g., Technical, Billing, Account)
* Algorithm Used: Logistic Regression

#### 2. Priority Prediction Model

* Input: Same ticket text
* Output: Ticket Priority (High, Medium, Low)
* Algorithm Used: Logistic Regression
  
## 5. Model Evaluation

The models are evaluated using the following metrics:

* **Accuracy**: Overall correctness of the model
* **Precision**: How many predicted values are correct
* **Recall**: How many actual values are captured
* **F1-Score**: Balance between precision and recall

### Confusion Matrix (Bonus)

* Displays correct and incorrect predictions
* Helps identify where the model makes mistakes

## 6. Results and Insights

* Text preprocessing significantly improves model performance
* TF-IDF effectively captures important keywords
* Logistic Regression provides good performance for text classification
* Combining subject and description improves prediction accuracy

Typical accuracy ranges between **85%–90%**, depending on the dataset.

## 7. Final System

The system works as follows:

1. User inputs a ticket
2. Text is cleaned and processed
3. Converted into numerical features using TF-IDF
4. Two models predict:

   * Ticket Category
   * Ticket Priority

### Example:

Input:
"My account is locked, please fix this immediately"

Output:

* Category: Account Issue
* Priority: High

## 8. Business Impact

This system provides significant value to organizations:

### For Support Teams:

* Reduces manual workload
* Automatically categorizes tickets

### For Managers:

* Identifies urgent issues quickly
* Improves response time

### For Companies:

* Enhances customer satisfaction
* Improves operational efficiency

## 9. Tools and Technologies Used

* Python
* Pandas & NumPy
* NLTK (Natural Language Processing)
* Scikit-learn
* TF-IDF Vectorizer
* Logistic Regression

## 10. Conclusion

This project demonstrates the practical application of Machine Learning in real-world business scenarios. By automating ticket classification and prioritization, the system improves efficiency, reduces response time, and enhances customer satisfaction.

It highlights how NLP and ML can be effectively used to solve operational challenges in support systems.



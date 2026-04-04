# FUTURE_ML_02
Support Ticket Classification &amp; Prioritization using Machine Learning

# Introduction
In modern organizations, customer support teams receive a large number of support tickets daily in the form of emails, forms, and issue reports. Managing these tickets manually is time-consuming and inefficient.

This project aims to automate the process of **support ticket classification and prioritization** using Machine Learning techniques. The system reads ticket text, classifies it into appropriate categories, and assigns a priority level to improve response time and operational efficiency.

# Objective
The main objectives of this project are:
* To classify support tickets into categories such as **Hardware, Access, HR Support, Storage**, etc.
* To predict the **priority level** of each ticket (High, Medium, Low)
* To reduce manual effort in sorting tickets
* To improve response time for critical issues

# Dataset Description
The dataset used in this project contains support ticket information with the following fields:
* **Text (Document):** Description of the issue reported by the user
* **Category (Topic_group):** Type of issue (e.g., Hardware, Access)
* **Priority:** Urgency level of the issue (High, Medium, Low)
The dataset represents real-world support scenarios, making it suitable for building practical machine learning models.

# Methodology
The project follows a structured machine learning pipeline:

## Data Preprocessing
* Removed missing values
* Converted text to lowercase
* Removed punctuation and numbers
* Removed stopwords (e.g., “the”, “is”)
* Applied lemmatization to reduce words to base form

## Feature Extraction
Text data was converted into numerical format using:
* **TF-IDF (Term Frequency-Inverse Document Frequency)**
* Used **n-grams (1 to 3)** to capture context

## Model Building
Two separate models were trained:

### Category Model
* Algorithm: **Linear Support Vector Classifier (LinearSVC)**
* Purpose: Predict ticket category
  
### Priority Model
* Algorithm: **LinearSVC**
* Purpose: Predict urgency level

## Train-Test Split
* Dataset split into:
  * **80% Training**
  * **20% Testing**
* Used **stratified sampling** to maintain class balance

## Evaluation Metrics
Models were evaluated using:
* Accuracy
* Precision
* Recall
* F1-score
* Confusion Matrix

# Results

## Category Model
* Achieved good accuracy (~80–85%)
* Correctly classified most tickets
* Some misclassification due to overlapping vocabulary

## Priority Model

* Successfully predicted urgency levels
* Balanced performance across High, Medium, and Low classes
* Demonstrated strong classification capability

# Explainability

The model’s decision-making was analyzed by extracting **top important words** for each category.
Examples:
* Hardware → laptop, system, device
* Access → login, password, account
This helps in understanding how the model makes predictions.

# Real-World Applications

This system can be used in:
* Customer support platforms
* IT helpdesk systems
* SaaS companies
* Enterprise ticketing systems

# Limitations
* TF-IDF does not capture deep context
* Some tickets are ambiguous
* Model performance depends on dataset quality


# Conclusion
This project demonstrates how Machine Learning can automate support ticket classification and prioritization. By using NLP techniques and classification models, the system improves efficiency, reduces workload, and enhances customer support operations.
























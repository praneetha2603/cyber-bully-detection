
# 🚨 Cyberbullying Detection System

## 📌 Project Description

Cyberbullying is a growing problem on social media platforms, negatively impacting individuals across different age groups and communities.
This project implements a **Cyberbullying Detection System** using **Machine Learning and Natural Language Processing (NLP)** techniques to automatically detect and classify cyberbullying tweets into multiple categories.

The system focuses on **text preprocessing, feature extraction using TF-IDF, and classification using Linear Support Vector Machine (LinearSVC)**.

---

## 🎯 Objectives

* Detect cyberbullying content from tweet text
* Classify tweets into different cyberbullying categories
* Perform detailed text preprocessing and feature analysis
* Evaluate model performance using standard metrics

---

## 🧠 Technologies Used

* **Programming Language:** Python
* **Environment:** Google Colab / Jupyter Notebook
* **Libraries:**

  * pandas
  * numpy
  * scikit-learn
  * nltk
  * matplotlib
  * seaborn

---

## 📂 Dataset Overview

* Contains tweet text and corresponding cyberbullying labels
* **Input Feature:** `tweet_text`
* **Target Variable:** `cyberbullying_type` (label encoded)
* Includes six categories:

  * Age-based cyberbullying
  * Gender-based cyberbullying
  * Religion-based cyberbullying
  * Ethnicity-based cyberbullying
  * Other cyberbullying
  * Not cyberbullying

---

## ⚙️ Data Preprocessing Steps

### **Step 1: Data Loading and Initial Inspection**

* Loaded the cyberbullying tweets dataset into a Pandas DataFrame
* Inspected sample records and dataset dimensions
* Analyzed the distribution of cyberbullying categories
* Verified that there were no missing values

### **Step 2: Label Encoding**

* Converted the categorical target variable (`cyberbullying_type`) into numerical labels
* Required because machine learning models operate on numerical data

### **Step 3: Text Normalization**

* Converted all tweet text to lowercase
* Ensured consistency and avoided case-sensitive duplication of words

### **Step 4: Noise Removal**

* Removed:

  * Stopwords
  * Punctuation
  * URLs
  * Numbers
  * Repeated character sequences
* Helped clean informal and noisy social media text

### **Step 5: Tokenization**

* Split cleaned tweets into individual word tokens using regex-based tokenization
* Enabled word-level text processing

### **Step 6: Stemming**

* Reduced words to their root form
* Minimized vocabulary size and grouped similar word forms

### **Step 7: Text Reconstruction**

* Joined processed tokens back into complete text strings
* Replaced empty tweets with a placeholder value

### **Step 8: Feature Relevance Analysis**

* Applied **Chi-Square statistical test**
* Analyzed the association between textual features and cyberbullying categories

### **Step 9: Feature Extraction using TF-IDF**

* Converted cleaned text into numerical feature vectors using **TF-IDF Vectorization**
* Vectorizer was fitted on training data and applied to both training and testing sets

### **Step 10: Model Training and Evaluation**

* Used TF-IDF vectors to train supervised machine learning models
* Evaluated model performance using classification metrics

---

## 📊 Visualization Analysis and Insights

### **1️⃣ Distribution of Cyberbullying Types**

* Count plot shows balanced representation across all six classes
* Balanced data reduces model bias and improves learning quality

### **2️⃣ Text Length Distribution by Cyberbullying Type**

* Pair plots and scatter plots show heavy overlap across categories
* Indicates tweet length alone is not a strong distinguishing feature

### **3️⃣ Statistical View of Text Length**

* Box plots and violin plots confirm similar median and distribution of text length
* Reinforces that text length is not a reliable standalone indicator

### **4️⃣ Most Frequent Words in Cyberbullying Tweets**

* Bar chart highlights commonly used abusive and discriminatory words
* Reflects aggressive and targeted language patterns

### **5️⃣ Word Cloud Analysis**

**a. Excluding `not_cyberbullying` and `other_cyberbullying`**

* Highlights strong offensive and targeted words for specific categories

**b. Excluding only `not_cyberbullying`**

* Shows broader abusive language patterns across all cyberbullying types

**c. Excluding both `not_cyberbullying` and `other_cyberbullying`**

* Confirms consistency of offensive vocabulary across defined categories

### **Overall Interpretation**

* Offensive and targeted language consistently dominates cyberbullying content
* Confirms strong linguistic patterns useful for text-based classification

---

## 🧪 Model Building and Evaluation (Step-wise)

### **Step 1: Data Splitting**

* Split dataset into:

  * **70% Training data**
  * **30% Testing data**
* Prevents overfitting and enables evaluation on unseen data

### **Step 2: TF-IDF Feature Extraction**

* Converted tweet text into TF-IDF feature matrices
* Vectorizer trained only on training data

### **Step 3: Model Training**

* Trained a **Linear Support Vector Machine (LinearSVC)** classifier
* Learned text patterns distinguishing cyberbullying categories

### **Step 4: Model Prediction**

* Predicted cyberbullying labels for the test dataset

### **Step 5: Model Evalution**

Model performance was evaluated using:

Accuracy Score

Confusion Matrix

The LinearSVC model achieved approximately 82.55% accuracy, showing strong classification performance.

Random Forest also demonstrated reliable performance by effectively classifying multiple cyberbullying categories.

### **📊 Confusion Matrix Analysis**

The confusion matrix provides a detailed view of:

Correct predictions for each cyberbullying class

Misclassification patterns between categories

Most predictions lie along the diagonal, indicating high correct classification rates.

Minor confusion occurs between closely related cyberbullying categories, which is expected in real-world social media text.

---

## 📈 Results and Observations

* Tweet length is not a strong discriminative feature
* Text content and vocabulary are crucial indicators
* TF-IDF combined with LinearSVC effectively captures cyberbullying patterns

---

## 📁 Project Structure

```
Cyberbullying-Detection-System/
│
├── cyberbullying.ipynb
├── dataset.csv
├── README.md
```

---







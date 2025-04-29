# Automatic-Issue-Labeling-using-Machine-Learning

# 🚀 Automatic Issue Labeling using Machine Learning

This project uses traditional Machine Learning (Logistic Regression with TF-IDF) to automatically classify GitHub issue descriptions into one of the three categories: **bug**, **enhancement**, or **question**. It leverages keyword-based open coding and sklearn's text processing tools to train and evaluate the classifier on labeled issue datasets.

---

## 📌 Features

- Automates labeling of GitHub issues into three categories: `bug`, `enhancement`, or `question`
- Applies custom keyword-based open coding for initial label annotation
- Uses Logistic Regression with advanced TF-IDF vectorization (n-grams, token filtering)
- Preprocesses text data using `neattext` for cleaning and stopword removal
- Built with Python 3.9 and scikit-learn pipeline for an interpretable, efficient model
- Effective on small or limited datasets without needing extensive manual labeling
- Evaluates and compares Logistic Regression model performance with LLMs like ChatGPT and Deepseek
- Tested on both cleaned project dataset and real-world GitHub issue samples

---

## 🔍 What the Code Does

1. **Reads Dataset**: Loads a labeled dataset in CSV format and separates it into `label` and `description`.

2. **Cleans Text**: Converts issue descriptions to lowercase and removes stopwords using `neattext`.

3. **Keyword-Based Labeling**: Applies an `open_coding()` function to auto-label descriptions as `bug`, `question`, or `enhancement` based on keyword matching.

4. **Filters Labels**: Removes entries labeled as `other` to maintain focus on the three major categories.

5. **Vectorizes Text**: Uses `TfidfVectorizer` with 1–3 grams and custom token patterns to convert cleaned text into numerical features.

6. **Trains Logistic Regression**: Builds a pipeline of TF-IDF and `LogisticRegression` from `sklearn`, then trains the model on 60% of the data and tests on 40%.

7. **Evaluates Performance**: Outputs precision, recall, and F1-score per label using `classification_report`.

8. **External Testing**: Predicts labels on a manually curated set of real GitHub issues (~40 records) to assess generalization.

---

## ⚙️ Installation Guide

Follow these steps to run the project locally using Python 3.9:

### Step 1: Install Python 3.9

Download and install from the [official Python website](https://www.python.org/downloads/release/python-390/)

### Step 2: Clone the Repository

```bash
git clone https://github.com/yourusername/issue-labeling-logistic.git
cd issue-labeling-logistic
```

## Step 3: Create and Activate Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

## Step 4: Install Dependencies

```bash
pip install -r requirements.txt
```

## Step 5: Launch the Jupyter Notebook

```bash
jupyter notebook
```

---

This project is licensed under the MIT License. See the LICENSE file for more information.

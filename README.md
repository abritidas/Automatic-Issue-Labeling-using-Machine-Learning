# 🚀 Automatic Issue Labeling using Machine Learning

This project uses traditional Machine Learning (Logistic Regression with TF-IDF) to automatically classify GitHub issue descriptions into one of the three categories: **bug**, **enhancement**, or **question**. It leverages keyword-based open coding and sklearn's text processing tools to train and evaluate the classifier on labeled issue datasets.

---

## 📌 Features

- Automates labeling of GitHub issues into three categories: `bug`, `enhancement`, or `question`
- Applies custom keyword-based open coding for initial label annotation
- Uses Logistic Regression with advanced TF-IDF vectorization (n-grams, token filtering)
- Preprocesses text data using `neattext` for cleaning and stopword removal
- Built with Python 3.10.0 and scikit-learn pipeline for an interpretable, efficient model
- Effective on small or limited datasets without needing extensive manual labeling
- Evaluates Logistic Regression model performance along with LLMs like ChatGPT and Deepseek
- Tested on real-world GitHub issue samples.

---

## ⚙️ Installation Guide

Follow these steps to run the project locally using Python 3.10.0:

### Step 1: Install Python 3.10.0

Download and install from the [official Python website](https://www.python.org/downloads/release/python-3100/)

### Step 2: Clone the Repository

```bash
git clone https://github.com/abritidas/Automatic-Issue-Labeling-using-Machine-Learning.git
cd Automatic-Issue-Labeling-using-Machine-Learning
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

# Malicious URL Detection using Logistic Regression

## Project Overview

This project focuses on detecting malicious URLs using machine learning techniques. By analyzing various features extracted from URLs and their associated metadata, the model classifies URLs as **malicious** or **non-malicious**. The logistic regression algorithm is used to build a reliable and interpretable classification model.

The dataset contains URL data enriched with cybersecurity-related features such as domain categories, top-level domains (TLDs), and analysis statistics. The goal is to leverage this data to enhance cybersecurity measures by automatically identifying potentially harmful URLs.

---

## Features Used

- **is_onion**: Indicates if the URL is from the Tor network (onion service).
- **white_list**: Whitelisting status of the URL.
- **last_analysis_stats_malicious**: Number of security engines reporting the URL as malicious.
- **categories_sophos_***, **categories_webroot_***, **categories_alpha_mountain_***: Categorical features describing the URL category based on different threat intelligence providers.
- **tld_***: One-hot encoded top-level domain indicators.
- Various other relevant numerical and categorical features derived from the dataset.

---

## Dataset

The dataset is sourced from `cybersecurity_extraction.csv` and contains URL metadata with multiple security analysis stats and categories.

---

## How to Run

1. Clone the repository:

    ```bash
    git clone https://github.com/CodeObsessed-1234/Malicious-URL-Detection-using-Logistic-Regression.git
    cd Malicious-URL-Detection-using-Logistic-Regression
    ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Run the Python script to:

    - Load and preprocess data.
    - Train the Logistic Regression model.
    - Evaluate the model.
    - Visualize results.

---

## Model Training and Evaluation

- Data preprocessing includes handling missing values, label encoding, and one-hot encoding of categorical variables.
- Target label (`malicious_label`) is created based on malicious votes and analysis stats.
- The Logistic Regression model is trained on an 80-20 train-test split.
- Evaluation metrics include accuracy, classification report, and confusion matrix.
- Visualizations show distribution of malicious URLs by onion status and top-level domains.

---

## Results

- Model accuracy: ~95%
- Precision, recall, and F1-scores indicate strong performance in distinguishing malicious URLs.
- Confusion matrix provides insights on false positives and false negatives.

---

## Future Work

- Try advanced models such as Random Forest, XGBoost, or deep learning classifiers.
- Incorporate more feature engineering and external threat intelligence data.
- Hyperparameter tuning for improved performance.
- Build an API for real-time URL classification.

---


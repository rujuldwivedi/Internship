<!-- Company Logo -->
![Latentview Analytics](company_logo.png)  

# AI-Powered Classification System for Automated Retail Categorization

<!-- Project Banner -->
![Project Banner](banner_image.png)

## Table of Contents

- [Introduction](#introduction)
- [Problem Statement](#problem-statement)
- [Project Objectives](#project-objectives)
- [Datasets](#datasets)
- [Solution Approach](#solution-approach)
  - [Data Preprocessing](#data-preprocessing)
  - [Modeling Techniques](#modeling-techniques)
    - [Amazon Product Metadata Classification](#amazon-product-metadata-classification)
    - [Audience Persona Categorization](#audience-persona-categorization)
    - [Chief-Level Role Classification](#chief-level-role-classification)
    - [Hybrid BERT and Generative AI Model](#hybrid-bert-and-generative-ai-model)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [Future Scope](#future-scope)
- [Getting Started](#getting-started)
- [Installation](#installation)
- [Usage](#usage)
- [References](#references)

---

## Introduction
This project focuses on developing an AI-powered classification system aimed at optimizing inventory management and product organization through automated retail categorization. The system leverages advanced NLP and deep learning techniques to classify product metadata and user-generated title descriptions.

## Problem Statement
Retail categorization in large-scale environments is complex due to diverse product attributes and extensive inventories. Manual categorization is inefficient and error-prone, necessitating an automated solution. The project addresses three major challenges:
1. Accurately classifying Amazon product metadata.
2. Categorizing user-entered titles from the Databricks dataset.
3. Managing a highly imbalanced dataset for chief-level role classification.

## Project Objectives
- Develop a high-accuracy classification model for product metadata categorization.
- Leverage NLP techniques for categorizing audience personas and chief-level roles.
- Implement a hybrid approach using LSTM, BERT, and Generative AI to handle complex scenarios.

## Datasets
- **Amazon Datasets:** Categorized under 35 categories, filtered using a defined metric to cover ~80% of total products.
- **Databricks Dataset:** Contains title descriptions with two labeling columns — Audience Personas and Chief-Level Roles.
- **Imbalanced Dataset for Chief-Level Roles:** Managed through undersampling, PCA, and SMOTE sampling.

## Solution Approach
### Data Preprocessing
- Lowercasing, special character removal, translation to English, and lemmatization.
- Feature extraction using TF-IDF, Word2Vec, and BERT embeddings.
- PCA for dimensionality reduction and SMOTE for balancing skewed data.

### Modeling Techniques
#### Amazon Product Metadata Classification
- LSTM model trained on a balanced dataset.
- Achieved **90% test accuracy**.

#### Audience Persona Categorization
- Classified user titles from Databricks using LSTM.
- Model trained on well-distributed data with **97.5% accuracy**.

#### Chief-Level Role Classification
- Classified titles into chief-level roles, managing extreme class imbalance.
- Introduced 'Others/Unprioritized' class.
- Applied undersampling, PCA, and SMOTE before training.
- Hybrid BERT and Generative AI model planned for improved recall.

#### Hybrid BERT and Generative AI Model
- Future implementation to enhance performance on imbalanced datasets.

## Evaluation Metrics
- Accuracy, Precision, Recall, F1-score.
- Classification reports and confusion matrices for detailed assessment.
- Placeholder for results: ![Classification Report](results1.png)
- Placeholder for dataset info: ![Dataset Info](results2.png)

## Results
- **Amazon Product Metadata:** 90% test accuracy.
- **Audience Persona Classification:** 97.5% test accuracy.
- **Chief-Level Roles:** Struggled with recall; hybrid BERT + Gen AI model planned.

## Future Scope
- Real-time categorization for dynamic inventory systems.
- Integration of multi-lingual models for broader applications.
- Implement feedback loops for iterative improvements.

## Getting Started
### Installation
Clone the repository:
```
   git clone <repository_url>
```

Install dependencies:
```
   pip install -r requirements.txt
```

### Usage
Run preprocessing:
```
   python preprocess.py
```

Train the models:
```
   python train_model.py --model LSTM
```

### References
- Amazon Product Data: [Link](https://registry.opendata.aws/amazon-reviews/)
- Databricks: [Link](https://databricks.com/)
- BERT and Transformers: [Link](https://huggingface.co/transformers/)

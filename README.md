# Group12_Fraud_Detection

This project demonstrates the use of autoencoders for detecting fraudulent credit card transactions. We build and compare three different autoencoder-based approaches to improve detection performance on highly imbalanced data.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Model Architectures](#model-architectures)
- [References](#references)

---

## Project Overview

We explore three autoencoder variants for fraud detection:

1. **Basic Autoencoder**: Learns to reconstruct non-fraudulent transactions and flags anomalies based on reconstruction error. (Using the original code)
2. **Denoising Autoencoder + SMOTE**: Adds noise during training and uses SMOTE to balance classes before training a classifier on encoded features. (Replicate another paper)
3. **Variational Autoencoder**: Encoder outputs mean and variance; decoder reconstructs data from latent samples.

Our goal is to compare their effectiveness on the Kaggle Credit Card Fraud dataset.

## Dataset

- **Source**: Kaggle [Credit Card Fraud Detection](https://www.kaggle.com/mlg-ulb/creditcardfraud)
- **File**: `creditcard.csv`
- **Description**: Transactions made by credit cards in September 2013 by European cardholders. The dataset has 284,807 transactions, with 492 frauds (0.17%).

## Usage

1. Place `creditcard.csv` in the project root directory or update the path in the notebook.
2. Launch the Jupyter Notebook:
   ```bash
   Group12_Fraud_Detection2.ipynb
   ```
3. Follow the notebook sections to preprocess data, train models, and evaluate results.

## Project Structure

```
├── Group12_Fraud_Detection2.ipynb  # Main analysis and models
└── README.md                           # Project documentation
```

## Model Architectures

- **Basic Autoencoder**: Fully connected symmetric network with input → bottleneck → output.
- **Denoising Autoencoder**: Adds Gaussian noise to inputs; encoder–decoder structure similar to basic AE.
- **Variational Autoencoder (VAE)**: Encoder outputs mean and variance; decoder reconstructs data from latent samples.

## References

- Kaggle Credit Card Fraud Detection dataset: https://www.kaggle.com/mlg-ulb/creditcardfraud
- Junyi Zou, Jinliang Zhang, and Ping Jiang. "Credit Card Fraud Detection Using Autoencoder Neural Network": https://doi.org/10.48550/arXiv.1908.11553

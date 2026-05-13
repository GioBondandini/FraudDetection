# Credit Card Fraud detection

Kaggle dataset available [here.](https://www.kaggle.com/datasets/kartik2112/fraud-detection)

### Project overview
This notebook explores a dataset of banking transactions between customers and merchants with the objective of detecting fraudulent activity. The goal is to build a classification model that can identify fraudulent transactions as accurately as possible.

Each transaction includes information such as timestamp, transaction amount, customer and merchant identifiers, category, geographic location, and a label indicating whether the transaction is fraudulent or legitimate. The target variable, *is_fraud*, represents whether a transaction is fraudulent (1) or legitimate (0).

### Fraud Detection Approach

The model outputs a probability of fraud for each transaction rather than a simple binary prediction. To translate this probability into an actionable decision (fraud / non-fraud), a decision threshold is applied: transactions with an estimated probability above the threshold are classified as fraudulent.

### Evaluation Focus

Special attention is given to false positives and false negatives:

- False positives: legitimate transactions incorrectly flagged as fraudulent

- False negatives: fraudulent transactions that are not detected

Both error types have important economic and operational implications, though their costs differ.

### Threshold Optimization

A key challenge of the problem is selecting an appropriate decision threshold. This choice determines the trade-off between:

- High recall, capturing as many fraudulent transactions as possible

- High precision, minimizing unnecessary fraud alerts

The analysis therefore focuses on identifying an optimal threshold that maximizes the overall effectiveness of the fraud detection system.
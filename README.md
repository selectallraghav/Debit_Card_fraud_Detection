# Debit Card Fraud Detection

This project focuses on detecting fraudulent transactions within a dataset of 2,513 records using a combination of machine learning and statistical techniques. It employs four distinct anomaly detection methods, aggregating their results to pinpoint high-risk transactions. The project is designed to deliver actionable insights through a comprehensive analysis, robust visualizations, and clear reporting. After preprocessing the dataset (handling missing values, normalizing numeric features, and defining categorical columns), univariate, bivariate, and multivariate analyses were conducted to understand feature distributions and relationships. These analyses were visualized using appropriate graphs to provide clarity and context.

## Dataset Description

| Column                  | Description                                                                 |
|-------------------------|-----------------------------------------------------------------------------|
| TransactionID           | Unique ID for each transaction                                              |
| AccountID               | Unique ID for each account, linked to multiple transactions                 |
| TransactionAmount       | Monetary value of the transaction                                           |
| TransactionDate         | Date and time of the transaction                                            |
| TransactionType         | Type of transaction, either 'Credit' or 'Debit'                             |
| Location                | U.S. city where the transaction occurred                                    |
| DeviceID                | ID of the device used for the transaction                                   |
| IP Address              | IPv4 address associated with the transaction                                |
| MerchantID              | Unique ID for the merchant involved in the transaction                      |
| Channel                 | Transaction channel (e.g., Online, ATM, Branch)                             |
| TransactionDuration     | Duration of the transaction in seconds                                      |
| LoginAttempts           | Number of login attempts before the transaction                             |
| AccountBalance          | Account balance after the transaction                                       |
| PreviousTransactionDate | Date and time of the prior transaction for the account                      |

## Datasets Used & Produced

| Dataset Name                           | Description                              |
|----------------------------------------|------------------------------------------|
| bank_transactions_data_2.csv           | Ultimate Dataset                         |
| debit_card_transactions_.csv           | Cleaned Debit Card Dataset               |
| potential_fraudulent_transactions_.csv | Model Output                             |
| debit_card_transactions_test_data_.csv | Test Data                                |

## Fraud Detection Methodologies

| Methodology           | Description                                                                 |
|-----------------------|-----------------------------------------------------------------------------|
| K-Means Clustering    | Identifies anomalies based on distance from centroids                       |
| Z-Score Analysis      | Flags extreme outliers in numeric features                                  |
| Logistic Regression   | Classifies transactions as fraud or non-fraud using supervised learning     |
| Isolation Forest      | Highlights anomalous transactions using tree-based partitioning             |

The results from these methods were consolidated into a Threat Level column, aggregating the number of fraud detections for each transaction. A higher threat level indicates a greater likelihood of fraud. To provide a prioritized view, the top 20 high-risk transactions were displayed in a color-coded threat chart. Additionally, the individual results for each method and the consolidated fraud list were saved in CSV format for further analysis.

## Note

This framework is scalable and can be integrated into real-time fraud detection systems through the Genesys platform, offering flexibility and efficiency for processing larger datasets.

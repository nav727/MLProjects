# ML Projects

# Credit Fraud Detector

### Idea/Motivation
With businesses moving online, fraud and abuse in online systems is constantly increasing as well. Traditionally, rule-based fraud detection systems are used to combat online fraud, but these rely on a static set of rules created by human experts. This project uses machine learning to create models for fraud detection that are dynamic and maintainable. 

### Data set

**Description**

The dataset contains transactions made by credit cards in September 2013 by European cardholders.
This dataset presents transactions that occurred in two days, where we have 492 frauds out of 284,807 transactions. The dataset is highly unbalanced, the positive class (frauds) account for 0.172% of all transactions.

It contains only numerical input variables which are the result of a PCA transformation. Unfortunately, due to confidentiality issues, we cannot provide the original features and more background information about the data. Features V1, V2, … V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'. Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-sensitive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.

Refer: https://www.kaggle.com/mlg-ulb/creditcardfraud

### Challenges faced
Most real-world applications possess unbalanced class distribution where the number of a class label heavily dominates the count of another class label. One of the best example to explain class imbalance problem is the fraud detection task, where the number of fraud class label is very low as compared to the normal class label. Most machine learning algorithms work poorly in the presence of unbalanced class distribution.So some questions may arise

1. How to tackle the class imbalance problem?
2. What evaluation metrics should be used to assess the performance of a predictive model?

### Design

The transactions are first checked at the terminal point to be valid or not, which is shown in figure below. At the terminal point, certain essential conditions such as sufficient balance, valid PIN (Personal Identification Number), etc. are validated and the transactions are filtered accordingly. All the valid transactions are then scored by the predictive model, which then classifies the transactions as genuine or fraudulent. The investigators investigate each fraudulent alert and provide feedback to the predictive model to improve the model’s performance.

![image](https://user-images.githubusercontent.com/43449556/118452328-aaa2f500-b713-11eb-9852-b1734dec993e.png)

### Solution

**Handle class imbalance in dataset**



**Deciding evaluation matrix**

We examine how the model performs when tested on data that was unseen. So how do we measure the performance of the model? We use evaluation metrics for evaluating the performance of the model depending on the nature of the problem.

Confusion matrix is the most commonly used evaluation metrics in predictive analysis mainly because it is very easy to understand and it can be used to compute other essential metrics such as accuracy, recall, precision, etc.











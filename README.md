🛡️ Online Payment Fraud Detection**

This project aims to detect fraudulent online transactions using Machine Learning techniques. The rise in online payments has been accompanied by an increase in financial fraud, making fraud detection systems more crucial than ever. This system uses transaction data to train models that identify potentially fraudulent behavior in financial transactions.

---

📁 Dataset Source**

Kaggle: Online Payments Fraud Detection Dataset  
Link: [https://www.kaggle.com/datasets/rupakroy/online-payments-fraud-detection-dataset](https://www.kaggle.com/datasets/rupakroy/online-payments-fraud-detection-dataset)

The dataset contains records of online financial transactions with the following key features:
- step: Time step of the transaction
- type: Type of transaction (e.g. PAYMENT, TRANSFER, DEBIT, etc.)
- amount: Transaction amount
- nameOrig: Sender’s ID
- nameDest: Receiver’s ID
- oldbalanceOrg / newbalanceOrig: Sender's balance before and after
- oldbalanceDest / newbalanceDest: Receiver's balance before and after
- isFraud: Indicates if the transaction is fraudulent (1 = fraud, 0 = genuine)

---

**📊 Exploratory Data Analysis (EDA)**

EDA was conducted to understand the dataset thoroughly:
- Overview of data types and distributions
- Checked for missing values
- Visualized imbalance in fraud vs. non-fraud cases
- Analyzed transaction types, amounts, and balance changes
- Correlation heatmaps, histograms, violin plots, and scatter plots

---

**🧠 Machine Learning Models Used**

Implemented and compared:
- Random Forest Classifier
- Logistic Regression

Data preprocessing steps:
- SMOTE for class imbalance
- Standardization of numerical features
- Train-test split (70/30) using stratified sampling

Evaluation metrics:
- Accuracy
- Precision
- Recall
- F1-score
- AUC (Area Under ROC Curve)

---

**📈 Performance**

Random Forest Classifier (Best Model):
- Accuracy: 99.6%
- Precision: 99.2%
- Recall: 98.4%
- F1-score: 98.8%
- AUC: 0.998

Logistic Regression:
- Accuracy: 98.2%
- Precision: 98.1%
- Recall: 95.8%
- F1-score: 96.9%
- AUC: 0.986

---

**🔍 Key Findings**

- TRANSFER and CASH_OUT transactions are more prone to fraud.
- Fraudulent transactions often involve high transaction amounts.
- Balances don’t align properly in many fraud cases (e.g. no decrease in sender balance).
- SMOTE helped improve performance for rare fraud class.
- Random Forest was highly effective and interpretable.

---

**🚀 Future Scope**

- Deploy models for real-time fraud detection
- Integrate user behavior, location, and device data
- Use advanced deep learning models (LSTM, autoencoders)
- Apply anomaly detection techniques
- Incorporate cost-sensitive learning
- Explainable AI: Use SHAP values to understand predictions
- Ensemble models and feedback loops for ongoing improvement

---

**📚 References**

1. Kaggle Dataset: https://www.kaggle.com/datasets/rupakroy/online-payments-fraud-detection-dataset  
2. A. Abdallah et al., "Fraud detection system: A survey," Journal of Network and Computer Applications, 2016.  
3. L. Breiman, "Random forests," Machine learning, 2001.  
4. T. Chen and C. Guestrin, "XGBoost," ACM SIGKDD, 2016.  
5. N. V. Chawla et al., "SMOTE: Synthetic Minority Over-sampling Technique," JAIR, 2002.  
6. S. M. Lundberg and S. I. Lee, "A unified approach to interpreting model predictions," NeurIPS, 2017.

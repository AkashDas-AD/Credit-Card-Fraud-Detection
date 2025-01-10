# Credit Card Fraud Detection

## Project Overview

This project focuses on detecting fraudulent credit card transactions using machine learning models. It involves data preprocessing, feature scaling, handling imbalanced data, training various classification models, evaluating their performance, and selecting the best-performing model.

## Dataset

- **Dataset Link:** https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud/data
- **Total Records:** 284,807 transactions  
- **Fraudulent Transactions:** 492 (Highly imbalanced dataset)  
- **Features:** 30 anonymized numerical input features and the transaction amount  

## Technologies Used

- **Python**  
- **Pandas, NumPy:** Data manipulation and analysis  
- **Matplotlib, Seaborn:** Data visualization  
- **Scikit-learn:** Machine learning models and evaluation  
- **SMOTE:** Handling imbalanced data  
- **Joblib:** Model serialization  

## Project Workflow

1. **Data Cleaning:**
   - Handled missing and inconsistent data to ensure data integrity.

2. **Feature Scaling:**
   - Applied **StandardScaler** to normalize the `Amount` column for better model performance.

3. **Handling Imbalanced Data:**
   - Addressed class imbalance using both **undersampling** and **oversampling** techniques.
   - **Oversampling** was done using **SMOTE (Synthetic Minority Over-sampling Technique)**.

4. **Model Training:**
   - Trained the following models on both undersampled and oversampled datasets:
     - **Logistic Regression (LR)**
     - **Decision Tree (DT)**
     - **Random Forest (RF)**

5. **Model Evaluation:**
   - Evaluated model performance using:
     - **Accuracy Score**
     - **Precision Score**
     - **Recall Score**
     - **F1 Score**

6. **Results Comparison:**

   - **Undersampled Data Results:**

     | Models | Accuracy (%) |
     | ------ | ------------ |
     | LR     | 94.73        |
     | DT     | 94.21        |
     | RF     | 94.73        |

   - **Oversampled Data Results:**

     | Models | Accuracy (%) |
     | ------ | ------------ |
     | LR     | 94.49        |
     | DT     | 99.80        |
     | RF     | **99.99**    |

7. **Model Selection:**
   - Selected and saved the **Random Forest** model trained on the **oversampled dataset** due to its highest accuracy.
   - Model saved using **Joblib** for future predictions.


## Conclusion

- Successfully built a fraud detection model with **99.99% accuracy** using a **Random Forest Classifier** on oversampled data.  
- Addressed data imbalance and optimized model performance with **feature scaling** and **SMOTE analysis**.

# Classification Models, Evaluation Metrics & Imbalanced Data Handling  

## Author  
**Arijit Gupta**  
Artificial Intelligence & Machine Learning Internship  

---

##  Project Overview  

This project focuses on building and evaluating binary classification models using the Breast Cancer dataset from `scikit-learn`.

The objective is to:

- Implement Logistic Regression and Decision Tree classifiers  
- Evaluate models using appropriate classification metrics  
- Analyze confusion matrix components  
- Handle imbalanced data using class weights  
- Compare model stability, interpretability, and overfitting behavior  
- Select the most suitable model for medical diagnosis  

---

##  Dataset  

- Breast Cancer Wisconsin Dataset  
- Binary classification problem:
  - **0 → Malignant**
  - **1 → Benign**

The dataset is slightly imbalanced, making metric selection important.

---

##  Models Implemented  

### 1️. Logistic Regression  
- Feature scaling applied  
- Evaluated using Precision, Recall, F1-score  
- ROC Curve and AUC calculated  

### 2️. Logistic Regression (Balanced)  
- Used `class_weight='balanced'`  
- Improves handling of minority class  
- Compared ROC & AUC with normal Logistic Regression  

### 3️. Decision Tree Classifier  
- Non-linear model  
- No feature scaling required  
- Overfitting checked using train vs test accuracy  

---

##  Evaluation Metrics Used  

- Confusion Matrix  
- Accuracy  
- Precision  
- Recall  
- F1-score  
- ROC Curve  
- AUC Score  

###  Why Accuracy Alone is Insufficient  

In imbalanced datasets, a model can achieve high accuracy by predicting only the majority class.  
Therefore, **Recall and F1-score provide better insight**, especially for medical applications.

---

##  Metric Importance in Medical Diagnosis  

For medical diagnosis:

- **Recall is the most important metric**  
  - Low recall → More False Negatives  
  - Missing a cancer case can be life-threatening  

- **F1-score is preferred in imbalanced data**
  - Balances Precision and Recall  
  - Provides a single robust performance measure  

---

##  Handling Imbalanced Data  

To address class imbalance:

python
LogisticRegression(class_weight='balanced')

This assigns higher penalty to minority class misclassification and improves recall.

---

## Final Model Selection

Logistic Regression was selected as the final model because:
 - Better generalization
 - More stable performance
 - Lower overfitting risk
 - Strong Recall performance (important for medical diagnosis)

---

## Conclusion

  This project demonstrates the importance of selecting appropriate evaluation metrics for classification problems, especially in healthcare.
  While accuracy provides a general overview, Recall, F1-score, and AUC are more reliable indicators for medical decision systems.
  Logistic Regression proved to be the most suitable and stable model for this task.

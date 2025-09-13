# 🏦 Bank Customer Churn Prediction in Machine Learning Using Python
This project, developed for a Machine Learning course in my 3rd-semester, focuses on building and evaluating a **binary classification model to predict bank customer churn**. The primary goal is to identify customers who are likely to leave the bank ("churn") based on their attributes and banking behavior.
By accurately predicting churn, a bank can proactively engage with at-risk customers through targeted retention strategies, thereby reducing customer loss and maintaining a stable client base. This project explores several machine learning algorithms, compares their performance, and uses fine-tuning to optimize the best-performing model.

---

### 📊 Dataset Description
The dataset used is the "Bank Customer Churn Prediction" dataset, which contains information about 10,000 anonymized bank customers.
* **Features:** The data includes 11 predictor variables such as `credit_score`, `country`, `gender`, `age`, `tenure`, `balance`, `products_number`, `credit_card` status, `active_member` status, and `estimated_salary`.
* **Target Variable:** The `churn` column is the binary target variable, where `1` indicates the customer has churned and `0` indicates they have not.

---

### ⚙️ Model Training 
Three models were trained and evaluated to predict customer churn:
1.  **K-Nearest Neighbors (KNN):** Chosen for its simplicity and effectiveness with non-linear decision boundaries. It was trained on the **scaled data**.
2.  **Random Forest Classifier:** An ensemble model chosen for its robustness against overfitting and its ability to handle non-linear relationships. It was trained on the **unscaled data**, as tree-based models are not sensitive to feature scaling.
3.  **Support Vector Machine (SVM):** Selected for its effectiveness in high-dimensional spaces and its robustness to outliers. It was trained on the **scaled data**.

---

### 📋 Evaluation
The performance of each model was compared using standard classification metrics. The Random Forest Classifier was chosen as the best initial model because:
* It showed a good balance between precision and recall.
* It is more resistant to the class imbalance present in the dataset.
* It achieved the **lowest False Negative rate**, which is crucial for this business problem (minimizing the number of customers incorrectly predicted as "not churning").

---

### 🔧 Fine-Tuning with GridSearchCV
To optimize the chosen **Random Forest** model, `GridSearchCV` was used to find the best combination of hyperparameters.
* **Hyperparameters Tuned:** `n_estimators`, `max_depth`, and `max_features`.
* **Best Parameters Found:**
    * `max_depth`: `None`
    * `max_features`: `'sqrt'`
    * `n_estimators`: `188`
* **Final Result** : After applying these parameters, the fine-tuned Random Forest model showed a **slight improvement** in overall accuracy, precision, and recall (approximately 1%). This indicates the initial model was already performing near its optimal level.

---

### 🏆 Conclusion
The **Random Forest Classifier** proved to be the most effective model for predicting bank customer churn in this project. While fine-tuning provided a marginal performance boost, the initial model was already robust. The final model serves as a valuable tool for identifying customers at risk of churning, allowing the bank to implement targeted retention efforts.

---
### 🛠️ Concepts
* **Language:** Python
* **Core Concepts:**
    * Exploratory Data Analysis (EDA) & Data Pre-Processing
    * Feature Encoding and Scaling
    * Model Training (KNN, Random Forest Classifier, SVM)
    * Evaluation (Confusion Matrix, Classification Report)
    * Hyperparameter Tuning (Grid Search)

---

### 🖋 Author
Laurel Evelina Widjaja

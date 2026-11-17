# Telco Customer Churn Prediction

A machine learning classification project that predicts whether a telecom customer will leave the service (churn) based on demographic details, subscribed services, and billing information.

---

## Dataset Overview[cite: 3]

* **Records:** 7,043 customer entries[cite: 3]
* **Features:** 20 independent attributes + 1 target variable (`Churn`)[cite: 3]
* **Key Attributes:**[cite: 3]
  * **Demographics:** `gender`, `SeniorCitizen`, `Partner`, `Dependents`[cite: 3]
  * **Account Information:** `tenure`, `Contract`, `PaperlessBilling`, `PaymentMethod`, `MonthlyCharges`, `TotalCharges`[cite: 3]
  * **Subscribed Services:** `PhoneService`, `MultipleLines`, `InternetService`, `OnlineSecurity`, `OnlineBackup`, `DeviceProtection`, `TechSupport`, `StreamingTV`, `StreamingMovies`[cite: 3]

---

## Project Workflow[cite: 3]

1. **Exploratory Data Analysis (EDA):**[cite: 3]
   * Inspected dataset dimensions, data types, and missing values (`TotalCharges` contained 11 null values)[cite: 3].
   * Visualized overall `Churn` class distribution, `Contract` type vs. `Churn` rate, and `MonthlyCharges` distribution[cite: 3].
2. **Data Preprocessing:**[cite: 3]
   * Removed the non-predictive `customerID` column[cite: 3].
   * Converted `TotalCharges` to numeric format and imputed missing values using the column median[cite: 3].
   * Encoded all categorical text variables into numeric representations using `LabelEncoder`[cite: 3].
   * Split the dataset into training (80%) and testing (20%) sets with `random_state=42`[cite: 3].
3. **Model Training & Evaluation:**[cite: 3]
   * Trained a **Logistic Regression** classifier (`max_iter=2000`)[cite: 3].
   * Trained a **Decision Tree** classifier (`random_state=42`)[cite: 3].
   * Evaluated both models using Accuracy, Precision, Recall, and F1 Score[cite: 3].

---

## Model Performance Comparison[cite: 3]

| Model | Accuracy | Precision | Recall | F1 Score |
| :--- | :---: | :---: | :---: | :---: |
| **Logistic Regression**[cite: 3] | **81.69%**[cite: 3] | **68.03%**[cite: 3] | **58.18%**[cite: 3] | **62.72%**[cite: 3] |
| **Decision Tree**[cite: 3] | 72.53%[cite: 3] | 48.21%[cite: 3] | 50.67%[cite: 3] | 49.41%[cite: 3] |

### Key Conclusion[cite: 3]
**Logistic Regression** outperformed the Decision Tree classifier across every evaluation metric, achieving **81.69% accuracy** and an **F1 Score of 62.72%**, making it the preferred model for predicting customer churn on this dataset[cite: 3].

---

## Tech Stack & Libraries[cite: 3]

* **Python 3.10**[cite: 3]
* **Data Manipulation:** `pandas`, `numpy`[cite: 3]
* **Visualization:** `matplotlib`, `seaborn`[cite: 3]
* **Machine Learning:** `scikit-learn`[cite: 3]

---

## How to Run

1. **Install dependencies:**
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter

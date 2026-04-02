## IDSC Healthcare Challenge (2026)
### Early Detection of Brugada Syndrome using ECG and Machine Learning

---

### 📌 Overview
This project develops a **machine learning model** to detect **Brugada Syndrome**, a potentially life-threatening heart condition, using ECG signal data. The model focuses on key ECG leads (V1–V3), where Brugada patterns are most visible.

---

### 🎯 Objective
- To classify patients as **Brugada or Normal** using ECG signals  
- To improve detection performance using machine learning techniques  
- To address class imbalance and enhance model reliability  

---

### 📊 Dataset
- Total patients: **363**
  - 287 Normal  
  - 76 Brugada (imbalanced dataset)  
- ECG signals from **12 leads**, focusing on **V1–V3**  
- Each sample transformed into a **feature vector (3600 features)**

---

###  Methodology

#### 🔹 Data Preprocessing
- Converted multi-class labels into **binary classification (0 = Normal, 1 = Brugada)**  
- Extracted ECG signals from **V1–V3 leads**  
- Flattened signals into structured feature vectors  

#### 🔹 Handling Class Imbalance
- Applied **SMOTE** to balance training data  
- Prevented data leakage by applying SMOTE only on training set  

#### 🔹 Model Development
Tested multiple models:
- Logistic Regression  
- Decision Tree  
- Random Forest  
- Support Vector Machine (SVM)  

#### 🔹 Model Optimization
- Performed **hyperparameter tuning (GridSearchCV)**  
- Used evaluation metrics:
  - Accuracy  
  - Recall (priority)  
  - F1-score  
  - ROC-AUC  

---

### 📈 Results & Insights
- Final model: **Decision Tree with SMOTE**  
- Accuracy: **72.7%**  
- ROC-AUC: **0.675**  
- Recall: **0.583**  
- Lead **V2** contributed the most to model predictions  
- Class imbalance significantly affected model performance  
- SMOTE improved detection of minority class  

---

### 🛠 Tools Used
- Python (scikit-learn)  
- Machine Learning Models  
- Data Preprocessing & Feature Engineering  

---

### 💡 Clinical Impact
- Supports early detection of **Brugada Syndrome**  
- Assists clinicians in identifying high-risk patients  
- Reduces risk of missed diagnosis in ECG interpretation  

---

### ⚠️ Limitations
- Small dataset size  
- Moderate model performance  
- Limited generalizability  

---

### 🚀 Future Improvements
- Use larger and multi-center datasets  
- Apply deep learning models  
- Improve feature extraction from ECG signals  

---

### 🖼 Output
- Model evaluation results  
- ROC curve and confusion matrix  
- Feature importance analysis 

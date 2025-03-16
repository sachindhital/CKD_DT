# 📊 Chronic Kidney Disease (CKD) Analysis Using Decision Tree

This project presents a **classification model** for predicting **Chronic Kidney Disease (CKD)** using the **Decision Tree (ID3) algorithm**. The model aims to assist healthcare professionals by automating the detection process, improving diagnosis speed and accuracy.

---

## ✅ **Dataset Overview**
- **Dataset**: Chronic Kidney Disease (CKD) Dataset from UCI Machine Learning Repository.
- **Total Samples**: 400
- **Features**: 25 (14 numerical and 11 categorical).
- **Target Variable**: `class` (Binary - `ckd` or `notckd`).

---

## ⚙️ **Technologies Used**
- **Python**
- **Pandas** (for data manipulation)
- **NumPy** (for numerical operations)
- **Scikit-learn** (for model training and evaluation)
- **Matplotlib & Seaborn** (for data visualization)

---

## 🧹 **Data Preprocessing**
- **Missing Values**:
  - Numerical features were analyzed for skewness.
    - **Mean imputation** for symmetric distributions.
    - **Median imputation** for skewed distributions.
  - Categorical features were imputed using **mode**.

- **Outlier Handling**: Initially considered but skipped, as removing outliers led to a **50% data loss**.

- **Feature Selection**: Retained only the most significant features: `hemo`, `sg`, `sc`, and `al`.

- **Encoding**: Categorical variables were encoded using **Label Encoding**.

---

## 📈 **Model Development**
- **Algorithm Used**: Decision Tree (ID3) with **entropy** criterion.
- **Pre-Pruning**: Limited tree depth and controlled splitting to avoid overfitting.
- **Post-Pruning**: Used **Cost Complexity Pruning (ccp_alpha)** to simplify the final tree.
- **Hyperparameter Tuning**: Utilized **GridSearchCV** to find optimal parameters.
- **Cross-Validation**: Performed 5-fold cross-validation for robustness.

---

## 📊 **Model Performance**
- **Training Accuracy**: 1.0
- **Testing Accuracy**: 0.9917
- **Cross-Validation Score**: 0.965

### **Classification Report**
| Metric    | Class 0 (Not CKD) | Class 1 (CKD) |
|-----------|------------------|---------------|
| Precision | 1.00             | 0.98          |
| Recall    | 0.99             | 1.00          |
| F1-Score  | 0.99             | 0.99          |

### **Confusion Matrix**
```
[[75  1]
 [ 0 44]]
```
- **No false negatives**, ensuring no CKD cases were missed.
- Only **one false positive**.

---

## 🚀 **How to Run**
1. **Clone the repository**:
```bash
git clone https://github.com/sachindhital/CKD-Analysis.git
cd CKD-Analysis
```

2. **Install dependencies**:
```bash
pip install -r requirements.txt
```

3. **Run the notebook**:
```bash
jupyter notebook CKD_analysis.ipynb
```

4. **Export to PDF** (Optional):
```bash
jupyter nbconvert --to pdf CKD_analysis.ipynb
```

---

## ✅ **Key Takeaways**
- The model demonstrates **high accuracy and robustness**, suitable for medical diagnosis support.
- Efficient preprocessing and pruning techniques were used to **minimize overfitting**.
- Feature selection ensured the model focused on the **most relevant medical indicators**.

---

## 🛠️ **Future Enhancements**
- Deploy the model as an **API** for real-time predictions.
- Integrate additional **external datasets** to improve generalization.
- Develop a **web interface** for user-friendly interaction.

---

## 👨‍⚕️ **Contributors**
- Sachin Dhital(https://github.com/sachindhital) - Data Science Lead

---

## 📄 **License**
This project is licensed under the **MIT License**.


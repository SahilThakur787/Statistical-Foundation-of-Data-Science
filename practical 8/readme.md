# 🌳 Decision Tree Classifier – Pima Indian Diabetes Dataset

## 🎯 Objective
To develop a **Decision Tree Classifier** using the **Pima Indian Diabetes Dataset** from Kaggle and to compare models built using **Entropy** and **Gini Index**.  
Additionally, to manually calculate **Entropy**, **Information Gain**, and **Gini Index** for understanding the root node selection.

---

## 📁 Dataset Information
**Source:** [Pima Indians Diabetes Database – Kaggle](https://www.kaggle.com/datasets/uciml/pima-indians-diabetes-database)

Each record represents health measurements of a Pima Indian woman along with a diabetes test result (0 = No Diabetes, 1 = Diabetes).

**Attributes:**
1. Pregnancies  
2. Glucose  
3. BloodPressure  
4. SkinThickness  
5. Insulin  
6. BMI  
7. DiabetesPedigreeFunction  
8. Age  
9. Outcome *(Target variable)*

---

## ⚙️ Implementation Steps

### Step 1: Import Libraries  
Used `pandas`, `numpy`, `matplotlib`, and `scikit-learn`.

### Step 2: Load the Dataset  
Read the file `diabetes.csv` into a DataFrame for analysis.

### Step 3: Data Preparation  
Separated the **features (X)** and the **target variable (y)**.

### Step 4: Split Data  
Divided data into training and testing subsets using `train_test_split()`.

### Step 5: Model Building  
Trained two Decision Tree models:
- One using **Entropy** criterion  
- Another using **Gini Index**

### Step 6: Evaluation  
Compared both models based on **accuracy** on the test set.

### Step 7: Visualization  
Plotted the trained trees using `plot_tree()` to visualize the decision paths.

### Step 8: Rule Extraction  
Generated human-readable rules from the model using `export_text()`.

### Step 9: Manual Calculation  
Calculated **Entropy**, **Information Gain**, and **Gini Index** manually for one feature (Glucose) to justify its role as the root node.

---

## 📊 Results Summary

| Metric | Entropy | Gini Index |
|:-------:|:--------:|:-----------:|
| Accuracy | ~0.74 | ~0.73 |
| Root Node | Glucose | Glucose |

- **Glucose** has the highest information gain and lowest impurity.  
- Both Entropy and Gini produce similar performance on this dataset.

---

## 📘 Key Formulas

- **Entropy:**  
  \[
  H(S) = -\sum p_i \log_2(p_i)
  \]

- **Information Gain:**  
  \[
  IG = H(S) - \sum \frac{|S_v|}{|S|} H(S_v)
  \]

- **Gini Index:**  
  \[
  Gini = 1 - \sum p_i^2
  \]

---

## 📈 Visualization Output
The notebook generates two decision tree diagrams:
- One built with **Entropy**
- One built with **Gini Index**

Both trees highlight **Glucose** as the primary split node.

---

## 🧩 Technologies Used
- Python 3.x  
- Pandas  
- NumPy  
- Matplotlib  
- Scikit-learn  

---

## ✅ Conclusion
- Decision Tree Classifiers are powerful and explainable models for classification tasks.  
- In this dataset, **Glucose** is identified as the most informative feature.  
- The **Entropy** criterion slightly outperforms **Gini** in terms of accuracy.  
- Manual calculations confirm the theoretical basis for root node selection.

# 🎓 Teachers Rating Dataset Analysis

## 🧭 Objective
The objective of this analysis is to explore a dataset of university instructors’ teaching evaluations using Python libraries such as NumPy, pandas, and SciPy.  
The goal is to perform statistical tests, evaluate relationships among variables, and interpret whether characteristics such as gender, tenure, and beauty scores influence teaching evaluation outcomes.

---

## 📊 Dataset Description
The dataset contains information about university instructors and their teaching evaluation ratings.  
It includes the following variables:

- Professor Name: Instructor’s name (may appear multiple times for different courses)  
- Gender: Male or Female  
- Tenure: Indicates whether the professor is tenured (Yes/No)  
- Beauty: Attractiveness score of the instructor  
- Evaluation: Teaching evaluation score (scale of 1–5)  
- Students: Number of students in the class (contains one large outlier)  
- Age: Instructor’s age  
- Division: Type of course — “Lower” or “Upper” division  

---

## ⚙ Tools Used
- Python 3.x  
- NumPy  
- pandas  
- SciPy  
- Jupyter Notebook / Google Colab  

---

## 🧪 Statistical Tests & Results

### 1️⃣ Gender and Evaluation (Independent T-Test)
T-statistic: 2.0053  
P-value: 0.0472  

The positive value suggests that the average Evaluation score for female professors is slightly higher than that for male professors.  
However, the difference is small and not practically meaningful.  

Since the p-value is slightly below 0.05, the result is *marginally statistically significant*.  
However, due to the small effect size, this difference should be interpreted with caution — it may not reflect a meaningful real-world effect.

---

### 2️⃣ Tenure and Evaluation (Independent T-Test)
T-statistic: 0.6587  
P-value: 0.5114  

This positive value indicates that the average Evaluation score for tenured professors is slightly higher than that of non-tenured professors.  
However, the difference in means is very small and not practically meaningful.  

Since the p-value is greater than 0.05, the result is *not statistically significant*.  
Therefore, we fail to reject the null hypothesis, indicating that *tenure status does not have a significant effect* on teaching evaluation scores.

---

### 3️⃣ Correlation Between Beauty and Evaluation
Correlation Coefficient: 0.0417  
P-value: 0.6509  

This value indicates a very weak negative linear relationship between Beauty and Evaluation.  
In practical terms, as a professor’s beauty score increases, their evaluation score tends to slightly decrease, but the effect is negligible.  

Since the p-value is greater than 0.05, this correlation is *not statistically significant*.  
We therefore fail to reject the null hypothesis, suggesting that any relationship observed in the sample is likely due to random variation.

---

### 4️⃣ Gender and Tenure (Chi-square Test)
Chi-square: 0.0801  
P-value: 0.7771  

Since the p-value is much greater than 0.05, the result is *not statistically significant*.  
We therefore fail to reject the null hypothesis, indicating that *Gender and Tenure are independent* of each other.  
In other words, there is no significant association between gender and tenure status in this dataset.

---

## 🧩 Conclusion
All statistical tests indicate that there are no strong or meaningful relationships among the variables studied.  
While there is a very slight difference in evaluations by gender, it is not practically significant.  
Gender and tenure do not meaningfully affect evaluation scores, and beauty has no significant correlation with teaching evaluations.  

These findings suggest that, within this dataset, appearance, gender, and tenure do not substantially influence how professors are evaluated by students.  
Any minor differences in averages are likely due to chance rather than genuine underlying effects.

---

## 📚 Summary

| Test | Variables | Statistic | P-value | Significance | Conclusion |
|------|------------|------------|----------|--------------|-------------|
| Correlation | Beauty vs Evaluation | r = 0.0417 | 0.6509 | ❌ Not Significant | No relationship |
| T-Test | Gender vs Evaluation | t = 2.0053 | 0.0472 | ⚠ Marginal | Slight but small difference |
| T-Test | Tenure vs Evaluation | t = 0.6587 | 0.5114 | ❌ Not Significant | No effect of tenure |
| Chi-square | Gender vs Tenure | χ² = 0.0801 | 0.7771 | ❌ Not Significant | Independent |

---

## 🧠 Final Insights
- Professors’ beauty has no meaningful effect on evaluation scores.  
- There is no strong gender difference in evaluations.  
- Tenure status does not significantly affect teaching evaluations.  
- Gender and tenure are independent characteristics.  

Overall, teaching evaluations appear independent of personal characteristics such as gender, tenure status, or beauty score.

---

🎓 Analysis of Student Evaluation Dataset
🧭 Purpose of the Study

This project focuses on examining a dataset of student evaluations of university professors using Python tools like NumPy, pandas, and Matplotlib.
The objective is to explore statistical patterns, generate visual insights, and interpret how various factors — such as tenure, age, gender, and minority status — might relate to student evaluation scores.

📊 Overview of the Dataset

The dataset includes records for individual professors, combining their demographic attributes, teaching details, and evaluation scores provided by students.

Column	Details
prof	Unique identifier assigned to each professor
age	Age of the professor (in years)
gender	Gender (Male or Female)
minority	Indicates if the professor belongs to a visible minority (Yes or No)
tenure	Whether the professor has tenure (Yes or No)
eval	Average student evaluation score (typically on a 1–5 scale)
students	Number of students who rated the professor
beauty	Numerical rating of perceived attractiveness
division	Level of course taught (Lower or Upper division)
🧰 Tools and Libraries Utilized
Tool/Library	Function
Python 3	Main programming language used
pandas	For data cleaning, handling, and analysis
NumPy	Performs numerical operations and statistical analysis
Matplotlib (Pyplot)	Creates basic visualizations like histograms and bar charts
Seaborn	For more advanced and styled visualizations
Google Colab	Used as the coding platform and execution environment
🧾 Key Findings
1. Tenure and Minority Representation

The dataset was analyzed to see if there’s a relationship between minority status and tenure.

Visible Minority Professors: 65.6% are tenured

Non-Minority Professors: 61.8% are tenured

🔍 Insight: The percentages are quite close, indicating that tenure rates in this dataset do not vary significantly with minority status.

2. Age Comparison Based on Tenure

The mean and standard deviation of age were compared between tenured and untenured faculty:

Tenured Professors: Average age = 52.3 years (±11.0)

Untenured Professors: Average age = 51.4 years (±11.4)

🔍 Insight: Tenured professors are marginally older, which aligns with the expectation that tenure is earned over time. The spread of ages is similar in both groups.

3. Age Distribution Visualization

To better understand the age spread among professors, both a histogram and a boxplot were used.

🔍 Insight: The histogram was particularly effective in showing how professors’ ages are distributed across the dataset.

4. Visualizing Categorical Variables with Bar Charts

Vertical and horizontal bar charts were explored to visualize category-based data.
A vertical bar chart was used to represent the gender distribution of professors.

🔍 Insight: Vertical bar charts (via pyplot.bar) provided a clear visual comparison of counts across gender categories.

5. Median Evaluation Score for Tenured Faculty

The median evaluation score was calculated for professors with tenure.

🔍 Finding: The median score for this group is 3.25, offering a sense of central tendency in how students rate tenured instructors.

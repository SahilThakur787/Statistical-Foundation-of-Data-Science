🌼 Iris Dataset — KNN Classification Project

🎯 Objective

This practical focuses on applying the K-Nearest Neighbors (KNN) algorithm to the classic Iris dataset to classify flowers into their respective species.
During the process, you explore how distance-based classification works through data exploration, normalization, model building, and evaluation.

📊 Dataset Overview

The Iris dataset contains 150 samples of iris flowers belonging to three distinct species. Each sample includes four measurements:


Feature	Meaning
sepal length (cm)	Sepal measurement (length)
sepal width (cm)	Sepal measurement (width)
petal length (cm)	Petal measurement (length)
petal width (cm)	Petal measurement (width)
species	Class label — Setosa, Versicolor, Virginica

🛠 Tools & Libraries

Library/Tool	Use
Python	Programming
pandas	Data handling
NumPy	Numerical operations
scikit-learn	KNN model, preprocessing, metrics
Matplotlib	Graphs & plots
Jupyter/Colab	Running the workflow

🧪 Step-by-Step Workflow

1️⃣ Exploratory Data Analysis (EDA)

Basic functions like head(), describe(), and groupby() were used to understand:

Range and distribution of each feature

Statistical summary

Differences between species

This initial inspection helps identify patterns in petal/sepal measurements.

2️⃣ Feature Scaling

Since KNN relies on distance calculations, all numerical columns were standardized using StandardScaler.
Scaling ensures all features contribute equally to the distance calculations.

3️⃣ Splitting Data & Training the KNN Model

70% data → training set

30% data → test set

Initial K value = 5

The model was then trained on the scaled training data.

4️⃣ Model Evaluation: Confusion Matrix & Accuracy

After predictions, evaluation metrics were computed:

Confusion matrix shows how many samples were correctly classified

Accuracy usually remains above 95%, indicating strong performance on this dataset

5️⃣ Detailed Metrics: Classification Report

The report includes:

Precision

Recall

F1-score

All three classes (Setosa, Versicolor, Virginica) show excellent scores due to their distinct feature boundaries.

6️⃣ Testing K = 1 to 20

To determine which K value performs best, the model was tested using K ranging from 1 to 20.
This reveals how the error rate changes as K increases.

7️⃣ Plot: Error Rate vs. K

A line plot was created showing:

Higher error at very small K values (overfitting)

More stable errors at medium K values

Best performance generally between K = 3 and 7

8️⃣ Choosing the Best K

The optimal K is the one with the lowest error rate, and in the Iris dataset, it typically lies between 3 and 7.

9️⃣ PCA Visualization

Using PCA with 2 components, a scatter plot was generated:

Each point colored by species

Clear separation, especially for Setosa

Helps visualize how the dataset clusters in lower dimensions

📈 Summary of Outcomes
Step	Purpose	Key Result
EDA	Understand dataset	Distinct species differences observed
Scaling	Normalize features	Improves distance-based accuracy
Training	Build KNN model	K=5 gives strong results
Confusion Matrix	Check performance	Very high accuracy
Error Analysis	Find best K	Optimal range: 3–7
PCA	Visualize clusters	Species clearly separated
🏁 Final Conclusion

This practical reinforces key concepts in machine learning, including:

Building and tuning a KNN classifier

Why scaling is crucial for distance-based models

How to evaluate performance with multiple metrics

Selecting the ideal K value

Using PCA to visualize high-dimensional data

The Iris dataset is perfectly suited for KNN because its species are naturally well-separated, making it easy to classify with high accuracy.

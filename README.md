# heart-disease-prediction
# 🫀 Heart Disease Prediction Project

## 🌟 Overview

This repository contains the analysis and initial data exploration for a Machine Learning project aimed at predicting heart disease. [cite_start]The work was performed in a Google Colaboratory environment[cite: 2, 13].

## 🛠️ Tech Stack

* **Language:** Python
* [cite_start]**Libraries:** `pandas` [cite: 3][cite_start], `matplotlib` [cite: 18][cite_start], `seaborn` [cite: 19]
* [cite_start]**Environment:** Colab Notebook [cite: 2]

---

## 💾 Dataset: Heart Disease Indicators

[cite_start]The analysis uses the `/content/heart_disease_dataset.csv` file[cite: 6]. [cite_start]The dataset contains **303 entries** and **14 columns**[cite: 17].

### Data Columns (Features)

[cite_start]The dataframe columns are all numerical types (`int64` or `float64`)[cite: 17].

| Column Name | Data Type | [cite_start]Notes (as seen in `df.columns` [cite: 152]) |
| :--- | :--- | :--- |
| `age` | `int64` | Patient age |
| `sex` | `int64` | Patient gender |
| `cp` | `int64` | Chest pain type |
| `trtbps` | `int64` | Resting blood pressure |
| `chol` | `int64` | Serum cholesterol in mg/dl |
| `fbs` | `int64` | Fasting blood sugar |
| `restecg` | `int64` | Resting electrocardiographic results |
| `thalachh` | `int64` | Maximum heart rate achieved |
| `exng` | `int64` | Exercise induced angina |
| `oldpeak` | `float64` | ST depression induced by exercise relative to rest |
| `slp` | `int64` | The slope of the peak exercise ST segment |
| `caa` | `int64` | Number of major vessels |
| `thall` | `int64` | Thalassemia |
| `output` | `int64` | **Target Variable (0: No Heart Disease, 1: Yes)** |

---

## 🔎 Exploratory Data Analysis (EDA)

The notebook includes several steps for initial data cleaning and visualization:

### 1. Missing Values Check ✅

* [cite_start]The check for missing values confirmed that all **303 entries** in all 14 columns are non-null[cite: 17, 59].

### 2. Feature Engineering & Encoding 🔢

* [cite_start]The `df.info()` function showed that all columns are already of type `int64` or `float64`[cite: 17].
* [cite_start]Therefore, the one-hot encoding step for categorical object columns was skipped, as the dataset is already in a suitable numerical format for modeling[cite: 174, 185].

### 3. Visual Analysis 📈

Key visualizations generated to understand feature distribution and relationships include:

* [cite_start]**Distribution of Age:** A histogram of the `age` column was plotted using `sns.histplot` to view the distribution of patient ages[cite: 22].
* [cite_start]**Cholesterol vs. Blood Pressure:** A scatterplot was created to visualize the relationship between `chol` (Cholesterol) and `trtbps` (Resting Blood Pressure)[cite: 85, 86, 119].
* [cite_start]**Average Age by Heart Disease:** A bar plot compared the `Average Age` between patients with and without heart disease (Output: 0 vs 1)[cite: 132, 146]. [cite_start]The average age of patients *without* heart disease (0) appears slightly higher than those *with* heart disease (1)[cite: 146].
* **Correlation Matrix:** A correlation heatmap was generated to show the linear relationships between all features.
* **Cholesterol Distribution:** A box plot shows the distribution of `chol` for the two `output` classes (0: No, 1: Yes).

## ➡️ Next Steps (Implied)

The next phase of the project would involve:

1.  Splitting the data into training and testing sets.
2.  Training various Classification models (e.g., Logistic Regression, Random Forest) on the prepared data.
3.  Evaluating model performance and selecting the best predictor.

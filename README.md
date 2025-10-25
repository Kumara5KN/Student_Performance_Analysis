# Data Science with Python_Kumara N_Data Science with Python Task - 1: Student Performance Data Analysis

## Project Overview

This repository contains the analysis for **Task 1: Data Science Project Using Python**, focusing on a student performance dataset. The objective was to clean the data, perform basic statistical analysis, answer specific business questions, and visualize the key findings using Python's `pandas`, `matplotlib`, and `seaborn` libraries.

---

## 💾 Dataset

* **File:** `student-mat.csv`
* **Source:** Student Performance Dataset (Math course data)
* **Description:** The dataset contains 395 student records with 33 features, including demographic information, academic habits, social factors, and final grades (G3).

---

## 🛠️ Project Steps and Methodology

The project followed the required steps outlined in the assignment document:

### 1. Data Loading and Cleaning
* The `student-mat.csv` file was loaded using `pandas`, specifying the semicolon (`;`) delimiter.
* **Missing Value Check:** No missing values were found.
* **Duplicate Check:** No duplicate student entries were found, confirming data quality.

### 2. Data Analysis (Key Findings)

The following questions were answered using the final grade **G3** (score out of 20):

| Analysis Question | Calculation | Result | Insight |
| :--- | :--- | :--- | :--- |
| **Average Final Grade (G3)?** | `df['G3'].mean()` | **10.42** | The average student score is slightly above half marks. |
| **Students scoring above 15 (G3 > 15)?** | `df[df['G3'] > 15].shape[0]` | **40** students | A small percentage of students achieved a high grade. |
| **Correlation (Study Time vs. G3)?** | `df['studytime'].corr(df['G3'])` | **0.10** | Indicates a **very weak positive correlation**. Study time is not the strongest predictor of the final grade. |
| **Gender with Higher Average G3?** | `df.groupby('sex')['G3'].mean()` | **Male (10.91)** vs. Female (9.97) | Male students achieved a slightly higher average final grade. |

---

## 📊 Visualizations

The following visualizations were generated to support the findings:

1.  **Histogram of Final Grades (G3):** Shows the overall distribution, highlighting that the majority of grades cluster between 8 and 11.
2.  **Box Plot of G3 by Gender:** Visually confirms the higher average score and greater spread of high scores for male students.
3.  **Scatter Plot of Study Time vs. G3:** Illustrates the weak relationship, showing widely scattered data points around the slight upward-trending regression line.

---


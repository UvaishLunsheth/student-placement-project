# 🎓 Student Placement & Salary Analysis

## 📌 Project Overview

This project analyzes the key factors influencing student placement outcomes and salary packages using a simulated real-world dataset.

The goal is to identify **what truly drives placements** — skills, academics, or experience — and provide actionable insights for students and educational institutions.

---

## 🎯 Problem Statement

Despite strong academic performance, many students fail to secure placements, while others achieve high salaries with moderate academic scores.

This project aims to answer:

* What factors most influence placement success?
* Do skills outweigh academic performance?
* What drives higher salary packages?
* How can students improve their placement chances?

---

## 📊 Dataset Information

* Source: Kaggle
* Records: ~9000 students
* Features: 20 columns
* Target Variables:

  * `placed` (0 = Not Placed, 1 = Placed)
  * `salary_lpa` (Salary in Lakhs Per Annum)

---

## 🧱 Project Structure

```bash
student-placement-project/
│
├── data/
│   ├── raw/
│   ├── processed/
│
├── notebooks/
│   ├── cleaning.ipynb
│   ├── eda.ipynb
│   ├── feature_engineering.ipynb
│   ├── modeling.ipynb
│
├── sql/
├── powerbi/
├── reports/
├── README.md
```

---

## Setup
* 1. Create conda environment:
`   conda create -n placement_env python=3.10`
* 2. Activate environment:
` conda activate placement_env`
* 3. Install dependencies:
   `pip install -r requirements.txt`

## 🛠️ Tech Stack

* Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
* MySQL (for data storage and querying)
* Power BI (for dashboard visualization)

---

## 🧹 Data Cleaning Summary

* No missing values in core features
* Identified **conditional missing values**:

  * `company_type` and `job_role` are null for unplaced students
* `salary_lpa = 0` correctly represents unplaced students
* No duplicate or invalid structural issues found

---

## ⚠️ Important Observations

* ~1298 students are not placed
* Missing values in job-related fields correspond to unplaced students
* Salary = 0 is a meaningful indicator, not an error

---

## 🚧 Work in Progress

* Exploratory Data Analysis (EDA)
* Feature Engineering
* Predictive Modeling
* Power BI Dashboard

---

## 🎯 Expected Outcomes

* Identify key drivers of placement
* Understand salary determinants
* Build a predictive model for placement & salary
* Provide actionable recommendations for students

---

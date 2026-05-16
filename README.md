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

## ⚙️ Setup

1. Create conda environment:
   `conda create -n placement_env python=3.10`
2. Activate environment:
   `conda activate placement_env`
3. Install dependencies:
   `pip install -r requirements.txt`

---

## 🛠️ Tech Stack

* Python (Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn)
* MySQL (for data storage and querying)
* Power BI (for dashboard visualization)

---

## 🧹 Data Cleaning Summary

* No missing values in core features.
* Identified **conditional missing values**:
  * `company_type` and `job_role` are null for unplaced students.
  * `salary_lpa = 0` correctly represents unplaced students.
* No duplicate or invalid structural issues found.

---

## ⚠️ Important Observations & Data Characteristics

* **Class Imbalance:** ~7702 students are placed, while ~1298 students are not placed (an approximate 85.5% / 14.5% split).
* **Hybrid Data:** The dataset contains a mix of highly realistic distributions (like Resume Scores and Backlogs) and synthetically generated uniform distributions (like CGPA and Projects).
* **Bimodal Salaries:** The salary distribution for placed students shows two distinct peaks (~45-50 LPA and ~70+ LPA), indicating clear tiers of hiring companies.

---

## 🔍 Key Findings (Exploratory Data Analysis)

Through univariate distributions and correlation mapping, we uncovered the primary drivers of placement and salary:

**1. What factors most influence placement success?**

* **Resume Strength:** `resume_score` (0.39) showed the strongest positive association with placement outcomes (0.39).
* **The Dealbreaker:** demonstrated the strongest negative relationship (-0.30), indicating unresolved academic backlogs significantly reduce placement probability.
* **Baseline Advantage:** `college_tier` (-0.21) showed a moderate influence on initial placement opportunities.

**2. Do skills outweigh academic performance?**

Segment analysis revealed:
* **High Skill + Low CGPA:** 95.81% Placement Rate
* **High CGPA + Low Skill:** 85.34% Placement Rate
Moreover,
*  `skill_score` (0.28) and `coding_score` (0.21) were more strongly associated with placement outcomes.
* `cgpa` (0.09) had comparatively lower influence.

These findings suggest technical capability may contribute more strongly to placement success than academic performance alone.

**3. What drives higher salary packages?**

* Once a student passes the baseline placement check, the rules change entirely. **Technical skills equal higher pay.**
* `skill_score` showed a strong relationship with salary growth (0.66).
* Hard skills like `dsa_skill` (0.33) and `python_skill` (0.33) were positively associated with higher salary packages.
* Interestingly, `college_tier` (0.007) had minimal relationship with salary levels.

**4. Actionable Recommendations for Students:**

* **Priority 1:** Clear all backlogs immediately.
* **Priority 2:** Build a strong resume by accumulating real-world experience (`internships` and `projects`).
* **Priority 3:** Master specific technical skills (DSA, Python) to break into the premium salary tiers.
* **Priority 4:** Stop obsessing over a perfect 9.5+ CGPA; an average CGPA combined with strong coding skills yields a much higher ROI.

---

## 🚧 Work in Progress

* ~~Exploratory Data Analysis (EDA)~~ *(Completed)*
* Feature Engineering (Handling class imbalances)
* Predictive Modeling (Classification for placement risk, Regression for salary tiers)
* Power BI Dashboard

---

## 🎯 Expected Outcomes

* Identify key drivers of placement *(Achieved)*
* Understand salary determinants *(Achieved)*
* Build a predictive model for placement risk & salary tier estimation
* Provide actionable recommendations for students *(Achieved)*

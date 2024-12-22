# Multivariate-R-Analysis-Assignment- - Maintenance and Personality Analysis

---

# Overview

This repository contains analyses for the **MATH 60602** course assignment at HEC Montreal on fundraising and retention using advanced multivariate statistical techniques. This group assignment focuses on two main datasets and analyses.

---

# Question 1: Personality Factor Analysis and Clustering

## Objective
Analyze responses from 2,000 individuals to a personality questionnaire to:
1. Perform a **factor analysis** to identify latent personality traits.
2. Use these traits for **clustering analysis** to segment individuals into groups.
3. Describe how these clusters differ using additional data from the previous assignment.

## Steps and Methods

### **1. Factor Analysis**
- Dataset: `TestPersonnalite.csv` (15 questions scored from 1 to 10).
- Steps:
  - Extracted factors using eigenvalues and scree plot criteria.
  - Interpreted factors based on loadings and created scales.
  - Verified **scale reliability** using Cronbach's alpha.

### **2. Clustering Analysis**
- Input: Factors from step 1.
- Methods:
  - Hierarchical clustering and k-means clustering.
  - Interpreted the clusters based on factor profiles.

### **3. Cluster Comparison**
- Merged personality data with previous dataset using `ID`.
- Analyzed how individuals differ across clusters using demographic and behavioral variables.

---

# Question 2: Maintenance Program Analysis

## Objective
Analyze data from a 10-year study of hydraulic pumps to assess the impact of three maintenance programs on pump failure times.

## Dataset
File: `LifeTimes.csv`
- **ID**: Pump identifier.
- **Time**: Time until catastrophic failure (or censoring) in days.
- **Censored**: 1 = censored, 0 = event observed.
- **Plan**: Maintenance program (1 = no maintenance, 2 = maintenance every 6 months, 3 = maintenance every 12 months).

## Steps and Methods

### **1. Survival Analysis**
- Estimated survival functions using Kaplan-Meier curves.
- Calculated:
  - Probability of pump survival after 5 years (1,800 days).
  - Quartiles of failure times for each plan.

### **2. Cox Proportional Hazards Regression**
- Modeled the effect of maintenance programs on **instantaneous failure risk**.
- Compared:
  - Maintenance every 6 months vs. no maintenance.
  - Maintenance every 12 months vs. no maintenance.
  - Maintenance every 6 months vs. maintenance every 12 months.
- Reported:
  - Hazard ratios, 95% confidence intervals, and p-values.

---

# Key Findings
1. **Survival Analysis**:
   - Kaplan-Meier survival curves illustrate differences in pump longevity across maintenance plans.

2. **Cox Regression**:
   - No statistically significant differences in failure risks between maintenance programs at the 5% level.

---

# How to Run the Code
1. Install required R packages: `survival`, `ggplot2`, `psych`.
2. Run the scripts provided in this repository to replicate the analyses.

# ❤️ Heart Disease Analysis & Insights Dashboard

## 📌 Project Overview

An end-to-end **Excel Data Analytics Project** focused on analyzing healthcare data to identify key factors associated with cardiovascular disease risks.

This interactive dashboard transforms raw patient health data into meaningful insights by combining:

- Data Cleaning & Transformation
- Power Query
- Excel Data Model
- DAX Measures
- Pivot Analysis
- Interactive Dashboard Design

The project helps analyze the relationship between **demographics, lifestyle habits, medical conditions, and heart disease risk factors**.

---

## 📊 Dashboard Preview

![Heart Disease Analysis Dashboard](image.png)

*(Dashboard screenshot is included as image.png in the repository root)*

---

# 🛠️ Project Workflow

## 1. Data Cleaning & Transformation (Power Query)

The raw healthcare dataset was cleaned and prepared using **Power Query**.

### Data Cleaning Tasks Performed:

✅ **Missing Value Handling**
- Filled missing values in important health attributes such as:
  - BMI
  - Sleep Hours
  - Medical indicators

using appropriate statistical replacement methods.

✅ **Data Standardization**
- Cleaned inconsistent categorical values.
- Converted fields into standardized formats:

Example:

Before:
```
Yes / YES / Y
No / NO / N
```

After:
```
Yes
No
```

Applied for columns such as:

- Smoking Status
- Diabetes
- Heart Disease Status

✅ **Data Type Formatting**

Corrected column data types:

- Patient ID → Integer
- Age → Whole Number
- BMI → Decimal
- Health Metrics → Numeric format

✅ **Feature Engineering**

Created new analytical columns:

- Age Groups:
  - Young
  - Middle Age
  - Old

- Risk Categories:
  - Low Risk
  - Medium Risk
  - High Risk

These helped in better segmentation and visualization.

---

# 2. Data Modeling & DAX Calculations (Power Pivot)

The cleaned dataset was loaded into the **Excel Data Model**.

Created custom DAX measures for dynamic KPI calculations.

## 📌 Total Patients

```DAX
Total Patients =
COUNT(heart_disease[PatientID])
```

## 📌 Heart Disease Cases

```DAX
Heart Disease Cases =
CALCULATE(
    COUNT(heart_disease[PatientID]),
    heart_disease[Heart Disease Status] = "Yes"
)
```

## 📌 Heart Disease Prevalence %

```DAX
Prevalence Rate =
DIVIDE(
    [Heart Disease Cases],
    [Total Patients],
    0
)
```

## 📌 Average BMI

```DAX
Average BMI =
AVERAGE(heart_disease[BMI])
```

---

# 3. Data Analysis Using Pivot Tables

Created multiple Pivot Tables to support dashboard visuals.

Performed analysis on:

- Heart Disease distribution by Gender
- Age group risk comparison
- Smoking impact analysis
- Diabetes relationship with heart disease
- Stress level vs Risk Category
- Sleep pattern analysis
- Cholesterol distribution

---

# 4. Interactive Dashboard Development

Designed an interactive Excel dashboard using:

### 📊 Visualizations

- KPI Cards
- Donut Charts
- Bar Charts
- Column Charts
- Line Charts

### 🎛️ Interactive Filters

Added slicers for:

- Gender
- Age Group
- Smoking Status
- Diabetes Status
- Risk Level

Users can dynamically filter the dashboard and explore different health patterns.

---

# 🔍 Key Insights Generated

### 1. Age Impact

Older age groups showed a higher occurrence of heart disease compared to younger groups.

### 2. Lifestyle Risk Factors

Patients with:

- High stress levels
- Reduced sleep duration
- Smoking habits

showed higher risk patterns.

### 3. Medical Conditions

Patients with conditions like:

- Diabetes
- High cholesterol

showed increased probability of heart disease indicators.

---

# 🧰 Tools & Technologies Used

| Tool | Purpose |
|---|---|
| Microsoft Excel | Dashboard Development |
| Power Query | Data Cleaning & Transformation |
| Power Pivot | Data Modeling |
| DAX | KPI Calculations |
| Pivot Tables | Data Analysis |
| Excel Charts | Visualization |

---

# 📂 Repository Structure

```
Heart-Disease-Analysis-Dashboard
│
├── heart_disease_analysis_dashboard.xlsx
│
├── image.png
│
└── README.md
```

---

# 🎯 Project Outcome

This project demonstrates practical skills in:

- Data Cleaning
- Business Intelligence Reporting
- Healthcare Analytics
- Dashboard Development
- DAX Formula Creation
- Data Storytelling

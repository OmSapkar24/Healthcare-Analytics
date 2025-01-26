# README: Healthcare Analytics Dataset

"""
# Healthcare Analytics Dataset

This dataset is designed for healthcare analytics and predictive modeling, particularly focused on patient readmissions. 
It includes detailed attributes with high variability to support machine learning and statistical analysis.

## Dataset Summary

- **Rows**: 99,000
- **Columns**: 7
- **Primary Use**: Predictive modeling for patient readmissions.

## Column Descriptions

1. **Patient_ID**: A unique identifier for each patient (e.g., `PID_1`).
2. **Age**: Patient's age in years (0–120).
3. **Gender**: Patient's gender (`Male`, `Female`, `Non-Binary`, `Other`).
4. **Length_of_Stay**: Number of days the patient stayed in the hospital (1–365).
5. **Primary_Diagnosis**: The primary diagnosis for hospitalization (`Cardiovascular`, `Respiratory`, etc.).
6. **Secondary_Diagnosis**: Any additional medical condition or none (`Diabetes`, `Hypertension`, etc.).
7. **Readmitted**: Binary flag indicating if the patient was readmitted (`1` = Yes, `0` = No).

---

## Data Cleaning Steps

1. **Missing Values**:
   - Rows with missing values were removed.
   - A heatmap was used to visualize missing data distribution.

2. **Data Type Validation**:
   - Columns like `Age`, `Length_of_Stay`, and `Readmitted` were cast to appropriate numerical types.
   - Non-numerical fields were preserved as categorical.

3. **Outlier Removal**:
   - Removed unrealistic values (e.g., `Age > 120`, `Length_of_Stay > 365`).

---

## Exploratory Data Analysis (EDA)

### Visualizations Included:
1. **Age Distribution**: Histogram with kernel density estimation (KDE) for patient age.
2. **Gender Proportion**: Bar chart showing the gender distribution.
3. **Readmission Rates**: Countplot comparing readmission rates.
4. **Length of Stay**: Boxplot showing length of stay across readmission status.
5. **Insurance Type**: Pie chart depicting the distribution of insurance types.

### Correlation Analysis:
- A heatmap of correlations among numerical columns (`Age`, `Length_of_Stay`, and `Readmitted`) was created for insights into relationships.

---

## Usage

### For Machine Learning:
- Use `Readmitted` as the target variable for classification models.
- Features like `Age`, `Gender`, `Length_of_Stay`, and diagnoses can serve as predictive inputs.

### For Statistical Analysis:
- Analyze trends in `Length_of_Stay` by `Primary_Diagnosis`.
- Explore demographic distributions (`Age`, `Gender`) against readmission patterns.

---

## How to Use This Dataset

1. **Download**: Save the dataset from the provided file.
2. **Load**: Use pandas or other tools to load the CSV.
   ```python
   import pandas as pd
   data = pd.read_csv("Healthcare_Analytics.csv")

# HR Data Analytics
### Data Cleaning and Preparation Using Python

---

## Project Overview

This project focuses on cleaning and preparing a Human Resources (HR) dataset using Python. The objective is to improve data quality by identifying and handling duplicate records, missing values, inconsistent categorical data, incorrect data types, unnecessary columns, and potential outliers.

The cleaned dataset provides a reliable foundation for further HR data analysis and visualization.

## Dataset Information

The original dataset contains employee details, employment information, performance ratings, engagement scores, satisfaction scores, and training records.

| Dataset Details | Information |
|---|---:|
| Original Records | 3,150 |
| Original Columns | 39 |
| Duplicate Rows Removed | 150 |
| Unnecessary Columns Removed | 14 |
| Final Records | 3,000 |
| Final Columns | 25 |

**Original Dataset:** `Messy_HR_Dataset_Detailed.csv`

## Tools and Technologies

- **Python** – Programming language used for data cleaning.
- **Jupyter Notebook** – Environment used to execute and document the cleaning process.
- **Pandas** – Used for data manipulation and cleaning.
- **NumPy** – Used for numerical operations.

## Data Cleaning Process

The following data-cleaning operations were performed:

### 1. Data Loading and Inspection
- Loaded the original HR dataset.
- Displayed the first five records.
- Examined dataset dimensions and column names.
- Inspected data types and missing values.

### 2. Duplicate Record Removal
- Identified 150 duplicate rows.
- Checked repeated Employee IDs.
- Verified that repeated employee records were identical.
- Removed duplicate records, retaining 3,000 unique employee records.

### 3. Removing Unnecessary Columns
Removed 14 unnecessary columns to retain relevant information for the HR Data Analytics project.

The dataset was reduced from 39 columns to 25 columns.

### 4. Date Conversion
Converted the following columns into datetime format:
- `StartDate`
- `ExitDate`
- `Survey Date`
- `Training Date`

Verified the converted values against the original dataset.

### 5. Missing Value Investigation
- Identified 1,467 missing values in the `ExitDate` column.
- Verified that all records with missing ExitDate values had an Active employee status.
- Preserved the missing values rather than filling them with estimated dates.

### 6. Categorical Data Cleaning
- Inspected 14 categorical columns for inconsistent text formatting.
- Used Pandas `str.strip()` to remove unnecessary leading and trailing spaces.
- Verified the categorical columns after standardization.

### 7. Numerical Data Examination
Used statistical summaries and frequency counts to examine numerical columns, including:
- Current Employee Rating
- Engagement Score
- Satisfaction Score
- Work-Life Balance Score
- Training Duration
- Training Cost

### 8. Outlier Detection Using IQR
Applied the Interquartile Range (IQR) method to the `Training Cost` column.

| Statistical Measure | Value |
|---|---:|
| Q1 | 327.5875 |
| Q3 | 786.9875 |
| IQR | 459.40 |
| Lower Bound | -361.5125 |
| Upper Bound | 1476.0875 |
| Potential Outliers | 0 |

No potential outliers were detected using the IQR method. Therefore, no outlier treatment was required.

### 9. Exporting the Cleaned Dataset
Exported the final cleaned dataset into a separate CSV file:

`HR_Data_Analytics_Cleaned.csv`

The original dataset was preserved without modification.

## Final Data Cleaning Results

| Description | Result |
|---|---:|
| Original Rows | 3,150 |
| Original Columns | 39 |
| Duplicate Rows Removed | 150 |
| Unnecessary Columns Removed | 14 |
| Final Rows | 3,000 |
| Final Columns | 25 |
| Duplicate Rows Remaining | 0 |
| Duplicate Employee IDs | 0 |
| Remaining Missing Values | 1,467 |
| Columns with Missing Values | ExitDate |
| Training Cost Outliers | 0 |

## Project Structure

```text
HR-Data-Analytics/
│
├── README.md
├── HR_Data_Analytics_Data_Cleaning.ipynb
├── Messy_HR_Dataset_Detailed.csv
└── HR_Data_Analytics_Cleaned.csv
```

## How to Run the Project

1. Clone or download this GitHub repository.
2. Open the project folder in Jupyter Notebook.
3. Ensure the original CSV dataset is available in the same folder as the notebook.
4. Open `HR_Data_Analytics_Data_Cleaning.ipynb`.
5. Run the notebook cells sequentially.
6. The cleaned dataset will be generated as `HR_Data_Analytics_Cleaned.csv`.

**Note:** Ensure that the original CSV filename matches the filename specified in the notebook's `pd.read_csv()` statement.

## Conclusion

The HR Data Analytics project successfully demonstrates the use of Python, Pandas, and NumPy for cleaning and preparing HR data.

The dataset was reduced from 3,150 rows and 39 columns to 3,000 rows and 25 columns. Duplicate records were removed, date columns were converted, categorical data was standardized, numerical values were examined, and potential outliers were checked using the IQR method.

The remaining missing ExitDate values were preserved based on the existing employee status information.

The final dataset is organized, consistent, and ready for further HR data analysis and visualization.

---
## Project Details

**Author:** Deepthi D.
**Project Title:** HR Data Analytics
**Domain:** Human Resources Analytics
**Technologies:** Python, Pandas, NumPy, Jupyter Notebook


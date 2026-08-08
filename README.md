# Healthcare Data Analytics & Patient Insights Dashboard

# Project Overview

This project focuses on analyzing healthcare data to generate meaningful insights into patient demographics, disease trends, treatment outcomes, hospital performance, and operational efficiency.

The project uses **Python, Pandas, SQL/DuckDB, and Power BI** to clean, analyze, visualize, and interpret healthcare data.

An interactive Power BI dashboard was developed to provide healthcare stakeholders with a centralized view of important patient and hospital performance metrics.

## 🎯 Project Objectives

The main objectives of this project are:

* Clean and preprocess healthcare records.
* Analyze patient demographics and medical conditions.
* Identify disease and admission trends.
* Evaluate treatment recovery outcomes.
* Analyze hospital and doctor performance.
* Calculate important healthcare KPIs.
* Identify patterns and potential anomalies.
* Perform descriptive and statistical analysis.
* Build an interactive Power BI dashboard.
* Generate actionable insights and recommendations.
* Maintain data quality and privacy considerations.

---

## 🗂️ Dataset

The dataset contains healthcare records covering patient information, medical conditions, hospital information, treatment costs, admission details, test results, and treatment outcomes.

### Dataset Size

* **Original Records:** 54,966
* **Columns:** 22
* **Records used for analysis:** 54,860
* **Invalid negative billing records excluded:** 106

### Main Columns

| Column               | Description                       |
| -------------------- | --------------------------------- |
| Patient_Name         | Patient name                      |
| Age                  | Patient age                       |
| Gender               | Patient gender                    |
| Blood_Type           | Patient blood type                |
| Medical_Condition    | Primary medical condition         |
| Admission_Date       | Date of hospital admission        |
| Doctor               | Treating doctor                   |
| Hospital             | Hospital name                     |
| Insurance_Provider   | Insurance provider                |
| Billing_Amount       | Treatment/hospital billing amount |
| Room_Number          | Assigned room number              |
| Admission_Type       | Type of admission                 |
| Discharge_Date       | Date of discharge                 |
| Medication           | Medication provided               |
| Test_Results         | Test result                       |
| Length_of_Stay       | Number of days spent in hospital  |
| Age_Group            | Categorized patient age           |
| Recovery_Flag        | Treatment recovery indicator      |
| Admission_Year       | Year of admission                 |
| Admission_Month      | Month of admission                |
| Admission_Month_Name | Name of admission month           |
| Admission_Year_Month | Year-month combination            |

---

## 🧹 Data Cleaning & Preprocessing

The dataset was inspected and cleaned before analysis.

### Data Quality Checks

The following checks were performed:

* Missing value detection
* Duplicate record detection
* Data type validation
* Date format validation
* Negative billing validation
* Patient name standardization
* Recovery status validation
* Length of stay calculation
* Age-group creation
* Admission year and month extraction

### Negative Billing Treatment

During data validation, **106 records contained negative billing amounts**.

Since a negative treatment billing amount is not valid for the intended analysis, these records were excluded from the analytical dataset.

The original dataset was retained separately, while the cleaned dataset was used for Python, SQL, and Power BI analysis.

---

## 🔄 Data Analysis Methodology

The project followed the following workflow:

```text
Raw Healthcare Dataset
        ↓
Data Inspection
        ↓
Data Cleaning & Preprocessing
        ↓
Exploratory Data Analysis
        ↓
Statistical Analysis
        ↓
SQL / DuckDB Analysis
        ↓
KPI Calculation
        ↓
Power BI Dashboard
        ↓
Insights & Recommendations
```

---

## 🐍 Python Analysis

Python and Pandas were used for data preprocessing and exploratory data analysis.

### Python Tasks

* Dataset inspection
* Missing-value analysis
* Duplicate detection
* Data type validation
* Data cleaning
* Patient demographic analysis
* Disease distribution analysis
* Billing analysis
* Recovery analysis
* Admission trend analysis
* Statistical analysis
* Data visualization

### Libraries Used


Python
Pandas
NumPy
Matplotlib



## 🗄️ SQL / DuckDB Analysis

SQL was used to perform structured analytical queries and calculate healthcare KPIs.

### SQL Analysis Performed

* Overall healthcare KPI analysis
* Disease-wise patient analysis
* Disease-wise recovery analysis
* Hospital performance analysis
* Doctor performance analysis
* Monthly admission analysis
* Admission type analysis
* Treatment cost analysis
* Length-of-stay analysis

DuckDB was used to execute SQL queries directly within the Jupyter Notebook.

---

## 📊 Healthcare KPIs

The following KPIs were calculated:

| KPI                    |     Result |
| ---------------------- | ---------: |
| Total Patients         |     54.86k |
| Recovery Rate          |    33.86 % |
| Average Treatment Cost |     25.59k |
| Average Length of Stay | 15.50 days |
| Total Hospitals        |    39.815k |

### Recovery Rate

Recovery rate was calculated using the `Recovery_Flag` field.

Recovery Rate =
Recovered Patients / Total Valid Patients × 100


Where:
Recovery_Flag = 1 → Recovered
Recovery_Flag = 0 → Not Recovered


## 📈 Power BI Dashboard

An interactive Power BI dashboard was developed to visualize healthcare trends and performance.

### Dashboard Components

The dashboard includes:

* Total Patient KPI
* Recovery Rate KPI
* Average Treatment Cost KPI
* Average Length of Stay KPI
* Total Hospitals KPI
* Patients by Medical Condition
* Recovery Rate by Medical Condition
* Monthly Patient Admissions
* Patient Distribution by Gender
* Patients by Admission Type
* Hospital Performance Table
* Interactive filters/slicers

### Interactive Filters

The following slicers were included:

* Medical Condition
* Gender
* Admission Type
* Admission Year

These filters allow users to dynamically explore the healthcare data.

---

## 📸 Dashboard Preview

![Healthcare Analytics Dashboard](Screenshots/Healthcare_Dashboard.png)

---

## 🔍 Key Insights

The analysis generated the following key insights:

### 1. Patient Demographics

The dataset contains '54.86k patients', with '49%' representing the most common gender/age group.

### 2. Disease Trends

'Arthritis' was the most frequently observed medical condition, accounting for the highest number of patient records.

### 3. Recovery Performance

The overall patient recovery rate was 33.36% .

### 4. Treatment Cost

The average treatment cost was '25.59k'.

### 5. Hospital Performance

Multiple hospitals recorded the highest patient volume.

Hospital performance varied based on patient volume, recovery rate, average treatment cost, and average length of stay.

### 6. Admission Trends

Patient admissions were highest during 2022, indicating a period of increased healthcare demand.

### 7. Length of Stay

The average patient length of stay was '15 days'.

Hospitals/conditions with relatively longer stays may require further investigation into operational efficiency and treatment processes.

---

## 💡 Recommendations

Based on the analysis, the following recommendations can be considered:

### 1. Improve Recovery Outcomes

Hospitals and medical conditions with relatively lower recovery rates should be investigated to identify opportunities for improving treatment and follow-up processes.

### 2. Optimize Resource Allocation

Healthcare resources, staffing, and hospital capacity can be planned according to periods with higher patient admission volumes.

### 3. Monitor Treatment Costs

High-cost treatments and hospitals should be reviewed to identify potential opportunities for improving cost efficiency without compromising patient care.

### 4. Reduce Prolonged Hospital Stays

Hospitals with unusually high average lengths of stay should investigate possible operational or treatment-related bottlenecks.

### 5. Disease-Specific Planning

Healthcare resources can be prioritized based on the frequency of medical conditions and their corresponding recovery outcomes.

---

## 🚨 Data Quality & Privacy

Data quality checks were performed before analysis, including:

* Missing-value checks
* Duplicate checks
* Invalid billing checks
* Data type validation
* Date validation
* Recovery flag validation

Negative billing records were excluded from the analytical dataset because they represented invalid treatment cost values.

If the dataset contains personally identifiable patient information, such information should not be published in a public repository. The project should use a synthetic, anonymized, or appropriately de-identified dataset for public sharing.

---

## 🛠️ Technologies Used

| Technology       | Purpose                             |
| ---------------- | ----------------------------------- |
| Python           | Data analysis and preprocessing     |
| Pandas           | Data manipulation                   |
| NumPy            | Numerical analysis                  |
| Matplotlib       | Data visualization                  |
| SQL              | Data analysis and KPI calculations  |
| DuckDB           | SQL execution                       |
| Jupyter Notebook | Analysis environment                |
| Power BI         | Interactive dashboard               |
| Excel            | Data inspection/supporting analysis |
| Git              | Version control                     |
| GitHub           | Project repository                  |

---

## 📁 Project Structure

```text
Healthcare-Data-Analytics/
│
├── Data/
│   └── healthcare_cleaned.csv
│
├── Python/
│   └── Healthcare_Step_3_EDA.ipynb
│
├── SQL/
│   └── Healthcare_Step_4_SQL.ipynb
│
├── Dashboard/
│   └── Healthcare_Analytics_Dashboard.pbix
│
├── Screenshots/
│   └── Healthcare_Dashboard.png
│
└── README.md
```

---

## 📓 Project Files

### Python Notebook

`Healthcare_Step_3_EDA.ipynb`

Contains:

* Data exploration
* Data cleaning validation
* Descriptive statistics
* Exploratory data analysis
* Visualizations

### SQL Notebook

`Healthcare_Step_4_SQL.ipynb`

Contains:

* SQL queries
* Healthcare KPI calculations
* Disease analysis
* Recovery analysis
* Hospital analysis
* Doctor analysis
* Admission analysis

### Power BI Dashboard

`Healthcare_Analytics_Dashboard.pbix`

Contains the interactive healthcare analytics dashboard.

---

## 📌 Key Project Outcomes

This project demonstrates the ability to:

* Work with real-world-style healthcare data.
* Perform data cleaning and preprocessing.
* Use Python and Pandas for exploratory analysis.
* Write SQL analytical queries.
* Calculate business and healthcare KPIs.
* Perform descriptive and statistical analysis.
* Build interactive Power BI dashboards.
* Identify trends and potential anomalies.
* Translate analytical findings into actionable recommendations.
* Document and present an end-to-end data analytics project.

---

## 🚀 Future Improvements

Potential future improvements include:

* Adding predictive patient outcome models.
* Developing a readmission prediction model.
* Adding advanced statistical testing.
* Creating automated data refresh pipelines.
* Adding hospital-level benchmarking.
* Implementing more advanced anomaly detection.
* Adding real-time healthcare monitoring capabilities.

---

## 👨‍💻 Author

**Om Bhole**

Bachelor of Engineering — Computer Engineering

### Skills Demonstrated

```text
Python
SQL
Pandas
Data Analysis
Statistics
Power BI
Data Visualization
DuckDB
Git
GitHub
```

---

## ⭐ Conclusion

The Healthcare Data Analytics & Patient Insights Dashboard provides a centralized analytical view of patient demographics, disease trends, treatment outcomes, hospital performance, and operational patterns.

By combining **Python, SQL/DuckDB, and Power BI**, the project transforms raw healthcare records into meaningful KPIs, interactive visualizations, analytical insights, and actionable recommendations that can support data-driven healthcare decision-making.

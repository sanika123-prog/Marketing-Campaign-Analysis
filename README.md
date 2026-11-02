# 📊 Marketing Campaign Analysis

## 📌 Project Overview

Marketing Campaign Analysis is a data analytics project developed using **Python, NumPy, Pandas, and Power BI**.

The main objective of this project is to analyze customer data, understand customer demographics, explore previous marketing campaign results, and create an interactive Power BI dashboard to present meaningful insights.

## 🎯 Project Objectives

- Analyze customer demographics such as age, job, and education.
- Explore customer account balance and contact information.
- Analyze customer records across different months.
- Understand previous marketing campaign results.
- Compare home loan and credit status.
- Perform data cleaning and exploratory data analysis using Python.
- Build an interactive dashboard using Power BI.

## 🛠️ Tools and Technologies

- **Python** – Data analysis and preprocessing
- **NumPy** – Numerical computations and statistical analysis
- **Pandas** – Data cleaning, transformation, grouping, and aggregation
- **Power BI** – Interactive dashboards and data visualization
- **Jupyter Notebook / Google Colab** – Python development environment

## 📂 Project Workflow

1. Import the dataset using Pandas.
2. Inspect the dataset using `head()`, `info()`, `shape`, and `describe()`.
3. Check missing values using `isnull().sum()`.
4. Identify duplicate records using `duplicated()`.
5. Perform data cleaning and preprocessing.
6. Conduct exploratory data analysis using NumPy and Pandas.
7. Create age groups and summarize customer categories.
8. Analyze customer records by job, month, education, and contact type.
9. Export the prepared dataset for Power BI.
10. Build an interactive dashboard to visualize the results.

## 📊 Power BI Dashboard

The dashboard contains two pages.

### Page 1: Marketing Campaign Overview

**KPI Cards**
- Total Records
- Average Age
- Average Account Balance
- Average Call Duration

**Charts**
- Monthly Campaign Records Trend
- Customer Records by Job
- Previous Campaign Results
- Home Loan and Credit Status
- Customer Distribution by Age Group

**Slicers**
- Job
- Age Group
- Contact Type
- Month
- Previous Campaign Result

### Page 2: Customer and Campaign Insights

**Charts and Visuals**
- Home Loan vs Credit Status
- Campaign Results by Contact Type
- Customer Distribution by Education
- Monthly Customer Records by Job (Matrix)

These visuals help explore customer categories and patterns in previous campaign results.

## 🐍 Python Libraries and Functions Used

### Pandas
- `read_csv()` – Load the dataset
- `head()` – Display the first five rows
- `info()` – Check column data types and non-null values
- `describe()` – Generate descriptive statistics
- `isnull().sum()` – Identify missing values
- `duplicated()` – Identify duplicate rows
- `groupby()` – Group data by categories
- `value_counts()` – Count category occurrences
- `agg()` – Calculate aggregated statistics
- `pivot_table()` – Summarize data in tabular form
- `to_csv()` – Export processed data

### NumPy
- `np.mean()` – Calculate the mean
- `np.median()` – Calculate the median
- `np.std()` – Calculate standard deviation
- `np.where()` – Create conditional categories
- `np.percentile()` – Calculate percentiles
- `np.nan` – Represent missing numerical values

## 💻 Example Python Code

```python
import pandas as pd
import numpy as np

# Load dataset
df = pd.read_csv("your_dataset.csv")

# Explore the dataset
print(df.head())
print("Dataset shape:", df.shape)

df.info()

# Check missing values
print(df.isnull().sum())

# Check duplicate records
print("Duplicate records:", df.duplicated().sum())

# Generate descriptive statistics
print(df.describe())

# Analyze records by job
job_summary = df.groupby("job").agg(
    total_records=("id", "count"),
    average_age=("age", "mean")
).round(2)

print(job_summary)

# Calculate average age using NumPy
print("Average age:", np.mean(df["age"]))

# Export processed data
df.to_csv("cleaned_marketing_data.csv", index=False)
```

**Note:** Update column names and file paths to match the actual dataset. Run only the functions and analysis steps that are relevant to your data.

## 🔍 Key Business Questions

- Which job categories have the highest number of records?
- How are customer records distributed across months?
- Which education categories have the most records?
- How do previous campaign results vary by contact type?
- How are home loan and credit status distributed?
- Which age group contains the most records?

## 📈 Key Learnings

This project provides practical experience in:

- Data cleaning and preprocessing
- Exploratory Data Analysis (EDA)
- Numerical analysis using NumPy
- Data manipulation using Pandas
- Data visualization using Power BI
- Dashboard design and interactive filtering
- Communicating data patterns through visualizations

## ⚠️ Data Notes

- `lastCampaignResult` represents the result of a previous campaign, not necessarily the current campaign.
- A count of `id` represents the number of records. It represents unique customers only if the IDs are unique.
- Values such as `unknown` should be analyzed before deciding whether to retain or remove them.
- Verify calculations, units, and aggregations before presenting conclusions.
- Do not upload confidential or restricted data without permission.

## 🚀 Future Improvements

- Add more DAX measures and advanced KPIs.
- Improve month sorting and number formatting.
- Add validated business insights and recommendations.
- Perform deeper statistical analysis using Python.
- Improve dashboard navigation and user experience.

## 👩‍💻 Author

**Sanika Ghadge**

- GitHub: https://github.com/sanika123-prog
- LinkedIn: www.linkedin.com/in/sanika-ghadge-6a50b9344

## 📄 License

Add an appropriate license if you want others to reuse your code. Ensure that you have permission to redistribute the dataset before publishing it.

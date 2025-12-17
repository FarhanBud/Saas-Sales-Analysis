# 💼 SaaS Sales Data Cleaning & Preparation  
**Capstone Project 2 — JCDS BSD**  
**Author:** Muhamad Farhan Budiana  

---

## 📌 Project Overview
This project focuses on **data cleaning and data preparation** for a simulated  
**Software as a Service (SaaS) sales dataset**.

The primary objective is to ensure the dataset is **clean, consistent, and analysis-ready**  
for exploratory data analysis and interactive visualization using **Tableau**.

This repository represents the **foundational data engineering stage** of the analytics workflow,  
which is critical for producing accurate and reliable business insights.

---

## 🎯 Project Objectives
- Prepare raw SaaS sales data for analysis and visualization  
- Identify and resolve data quality issues (missing values, duplicates, anomalies)  
- Ensure consistent data types and realistic business metrics  
- Produce a clean dataset ready for Tableau dashboard development  

---

## 🏢 Business Context
The dataset represents a **fictional SaaS company** that provides subscription-based software  
solutions to corporate clients across multiple regions and customer segments.

Each transaction includes information such as:
- Product sold  
- Customer segment  
- Sales region and country  
- Discount applied  
- Sales value and profit  

This project simulates a real-world scenario where high-quality data is essential to evaluate  
**discount effectiveness, profitability, and sales performance**.

---

## 📊 Dataset Information
- **Raw dataset:** `SaaS-Sales.csv`  
- **Clean dataset:** `SaaS-Sales-Clean.csv`  
- **Data source:** Kaggle — *AWS SaaS Sales Dataset*  
- **Time period:** 2020–2023  
- **Data size:** ~10,000 rows (simulated sales transactions)

### Key Columns
| Column | Description |
|------|------------|
| `Order Date` | Transaction date |
| `Customer` | Customer / company name |
| `Segment` | Customer type (SMB, Enterprise, Strategic) |
| `Region` | Sales region (AMER, EMEA, APJ) |
| `Country` | Customer country |
| `Product` | SaaS product name |
| `Sales` | Total sales value |
| `Profit` | Net profit |
| `Discount` | Discount applied (%) |
| `Quantity` | Number of licenses sold |
| `Profit Margin` | Profit-to-sales ratio |

---

##  Data Cleaning Process
 **Notebook:** `saas-sales-analisis.ipynb`

The data cleaning process was conducted step by step using **Python (Pandas & NumPy)**.

### 1️. Initial Exploration
- Loaded raw dataset using `pandas`
- Inspected data structure, column types, and missing values
- Generated summary statistics to understand initial data distribution

---

### 2️. Data Type & Formatting
- Converted date columns (`Order Date`, `Date Key`) to `datetime`
- Converted numeric columns (`Sales`, `Profit`, `Discount`, `Quantity`) to numeric format
- Cleaned categorical columns (trimmed whitespace, standardized values)

---

### 3️. Missing Values & Duplicates
- Removed duplicate records based on `Order ID`
- Handled missing values:
  - **Numeric columns:** median imputation  
  - **Categorical columns:** filled with `"Unknown"`

---

### 4️. Outlier Detection & Metric Correction
- Identified anomalies through statistical inspection and visualization
- Detected **unrealistic Profit Margin values (>100%)**
- Corrected profit margin calculation to ensure business realism:


- Revalidated summary statistics after correction

---

##  Final Output
-  Clean and consistent dataset: `SaaS-Sales-Clean.csv`  
-  Analysis-ready for Tableau visualization  
-  No critical missing values in key business columns  
-  Realistic profit margin distribution (average ≈ 19%)

---

##  Tableau Dashboard
The cleaned dataset is used to build an interactive Tableau dashboard for business analysis.

 **Tableau Public Dashboard:**  
https://public.tableau.com/app/profile/muhamad.farhan.budiana/viz/DashboardSaaSSales-MuhamadFarhanBudiana/AWSSaaSSalesPerformanceDashboard?publish=yes

---

##  Tools & Technologies
- Python (Pandas, NumPy)  
- Jupyter Notebook  
- Tableau Public  
- Git & GitHub  

---

##  Repository Structure

├── SaaS-Sales.csv # Raw dataset
├── SaaS-Sales-Clean.csv # Cleaned dataset
├── saas-sales-analisis.ipynb # Data cleaning notebook
├── README.md # Project documentation


---

##  Notes
This repository focuses specifically on the **data cleaning and preparation stage**.  
Further exploratory analysis, visualization, and business insights are presented  
in the Tableau dashboard.

---

##  Contact
**Muhamad Farhan Budiana**  
LinkedIn Link : https://www.linkedin.com/in/muhamadfarhanbudiana/
Email : farhan.budiana19@gmail.com



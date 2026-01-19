# 🔄 Basic ETL Pipeline

## 🎯 Goal
Build a basic ETL pipeline to clean, standardize, and upload SAT performance data
into a PostgreSQL database, enabling reliable relational analysis with other NYC
school datasets.

The focus of this task is on **data quality**, **schema alignment**, and
**database-ready outputs**.

---

## 🗂️ Data Context
- Source dataset: NYC SAT Results
- Target database: PostgreSQL
- Primary key: **DBN**, enabling joins with:
  - High School Directory
  - School Safety Report
  - School Demographics

---

## 🔧 ETL Steps

### 1️⃣ Column Selection
**Relevant columns**
- `DBN`: relational key for database integration  
- `Num of SAT Test Takers`: contextualizes average scores  
- `SAT Critical Reading Avg. Score`  
- `SAT Math Avg. Score`  
- `SAT Writing Avg. Score`  

**Excluded columns**
- `SCHOOL NAME`: already available in the High School Directory  
- Duplicate or inconsistently named score columns  
- Internal identifiers replaced by DBN  
- Contact and administrative fields without analytical value  
- `pct_students_tested` and `academic_tier_rating`: out of scope for this analysis  

---

### 2️⃣ Data Cleaning & Validation
- Standardized column names for consistency
- Converted score and count fields to numeric data types
- Replaced non-numeric placeholder values (e.g. `"s"` indicating suppressed or unavailable data) with `NaN`
- Validated SAT score ranges (200–800)
  - Invalid values were detected only in the Math score column and replaced with `NaN`
- Removed duplicate records

---

### 3️⃣ Load Phase
- Exported the cleaned dataset as a new CSV file
- Uploaded the dataset into PostgreSQL using Python
- Defined `DBN` as the primary key to ensure reliable relational joins

---

## 🔍 Key Insights
- Explicit validation and cleaning steps were required to handle suppressed and inconsistent values in real-world education data.
- Enforcing valid score ranges prevented distorted summary statistics.
- Early alignment of primary keys significantly simplified downstream SQL-based analysis.

---

## 📦 Result
A clean, validated, and database-ready SAT performance dataset optimized for
structured querying and integration with other NYC school data sources.


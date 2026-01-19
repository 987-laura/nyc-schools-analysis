# 🧬 Database Exploration

## 🎯 Goal
Use SQL queries via Python to explore relationships between school attributes,
demographics, and performance indicators within a relational database.

The focus of this task is on **structured querying**, **data integration**, and
**critical assessment of data coverage and limitations**.

---

## 🗂️ Data & Schema Context
- Relational joins are performed using **DBN** as the primary key.
- Core tables include:
  - High School Directory
  - School Demographics
- Queries are executed via Python using SQLAlchemy.

---

## 📊 Analytical Focus
- Relational joins across multiple tables
- Targeted analytical questions expressed in SQL
- Scalable exploration of cleaned, database-ready datasets
- Validation of data completeness and join integrity

---

## ⚠️ Data Coverage & Limitations

- School distribution across boroughs is highly uneven:
  - Brooklyn: 121 schools  
  - Bronx: 118 schools  
  - Manhattan: 106 schools  
  - Queens: 80 schools  
  - Staten Island: 10 schools  

- Demographic data availability is **severely limited**:
  - English Language Learner (ELL) and Special Education (SPED) percentages are only available for a small subset of schools.
  - Out of 243 records in the `school_demographics` table, **only 40 schools can be successfully joined** with the High School Directory.
  - All matched demographic records correspond exclusively to **Manhattan** schools.

- As a result, demographic analyses for **Brooklyn, Bronx, Queens, and Staten Island are not possible** with the available data.

---

## 🔍 Key Insights

- Borough-level comparisons for ELL and SPED students cannot be performed due to missing demographic coverage outside Manhattan.
- Within Manhattan:
  - The **average percentage of English Language Learners (ELL)** across matched schools is **7.57%**.
  - The highest observed SPED percentages all belong to the same institution:
    - *East Side Community School*  
      - 28.8% (rank 1)  
      - 27.7% (rank 2)  
      - 26.7% (rank 3)  

- These repeated high-SPED values indicate that a small number of schools can strongly influence summary statistics when sample sizes are limited.

---

## 📈 Outcome
SQL-based exploration enabled deeper and more controlled analysis than flat-file approaches.
At the same time, the task highlighted the importance of data validation, join diagnostics,
and transparent communication of analytical limitations when working with real-world datasets.

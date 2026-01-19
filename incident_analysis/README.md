# 🎓 School Incident Analysis

## 🎯 Goal
This project analyzes reported incident and delinquency data from NYC public schools (2014–2016) to identify differences across schools and boroughs.  
Analyze incident and delinquency data from NYC public schools to identify differences across schools and boroughs.

---

## 📊 Data Source
- NYC Department of Education – School Safety Incident Reporting (SSIR)
🔗 [My Google Sheet](https://docs.google.com/spreadsheets/d/1uIf_kErdsOLMNyhPVBU2AAheZKnkLRFNLdQLe0rib70/edit?usp=sharing)

---

## 🔍 Analysis Focus
- Incident frequency and category distribution
- Borough-level comparisons
- Normalized metrics (incidents per 100 students)

---

## 🧹 Data Preparation
- Handling missing values
- Standardizing school names
- Aggregation by DBN

---

## 🚨 Observations
- Total rows: 6310 data rows (6311 including header)
- Unique schools: 1891 (based on DBN)
- Most frequent incident type: Non-Criminal Incidents (11772 cases, 41.82% of all incidents)
- Bronx incident %: 28.24%

---

## 🔍 Key Insights
- Incident rates per 100 students are highly right-skewed: roughly two-thirds of schools report zero or fewer than one incident per 100 students, while elevated rates are limited to a small subset of schools.
- Non-criminal incidents increase steadily from 2014 to 2016, while most other incident categories show a slight downward trend over the same period.
- Data quality varies across fields: there are some missing values across the cells and inconsistent school naming required additional cleaning before analysis.


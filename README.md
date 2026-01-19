# 🏫 NYC Schools Data Analysis

## 🎯 Project Purpose
This repository presents an end-to-end data analysis and data engineering project based on New York City public high school datasets.  
It focuses on clean data preparation, SQL-based exploration, and interpretable analytical insights.

The project is designed as a **portfolio showcase**, demonstrating a complete workflow from raw data to structured database queries.

---

## 🧭 Project Components
The repository is organized by analytical tasks rather than by timeline:

- 🎓 **Incident Analysis** – normalized analysis of school incident data across schools and boroughs  
- 🏫 **School Directory Exploration** – structural differences in school distribution, enrollment size, and grade spans  
- 🧬 **Database Exploration** – SQL-based relational analysis of school attributes and demographics  
- 🔄 **Basic ETL Pipeline** – cleaning and loading SAT performance data into PostgreSQL  

Each component contains a dedicated README describing methodology and details.

---

## 📁 Project Structure

```text
nyc-schools-analysis/
├── incident_analysis/
│   ├── data/
│   │   ├── school-safety-report.csv
│   │   └── School_Safety_Report_Data_Dictionary.xlsx
│   └── README.md
├── school_directory_exploration/
│   ├── notebook.ipynb
│   ├── visuals/
│   │   ├── Avg-number-schools-per-borough.png
│   │   └── Avg-number-students-per-borough.png
│   └── README.md
├── database_queries/
│   ├── queries.ipynb
│   └── README.md
├── database_population/
│   ├── cleaned_data.csv
│   ├── upload_script.ipynb
│   └── README.md
├── requirements.txt
└── README.md
```

---

## 📌 Key Findings (Summary)

- **Incident rates are highly concentrated**  
  Most schools report zero or very low incident rates per 100 students, while elevated rates are limited to a small subset of schools.

- **Strong structural differences across boroughs**  
  Boroughs differ substantially in school density and average school size; boroughs with fewer schools tend to have larger average enrollments.

- **Data availability constrains demographic analysis**  
  Usable demographic data is limited to a small number of Manhattan schools, preventing borough-wide demographic comparisons.

- **Data quality issues require explicit handling**  
  Suppressed values, inconsistent identifiers, and incomplete joins significantly affect analysis and must be addressed early in the workflow.

- **Early schema and key alignment improves downstream analysis**  
  Consistent use of DBN across datasets simplifies relational joins and enables scalable SQL-based exploration.

---

## 🚀 Next Steps

- Extend analyses to additional school years and outcome metrics  
- Develop more advanced SQL queries and performance optimizations  
- Build interactive dashboards (e.g. Tableau or Power BI)  
- Automate data ingestion, validation, and ETL workflows  
- Improve reproducibility through environment and dataset versioning  

---

## 🛠️ Tools & Technologies
Python (pandas, numpy, matplotlib), PostgreSQL, SQLAlchemy, Jupyter Notebooks, Git & GitHub

---

## 👤 Author
Created as part of the onboarding and training program at **Webeet.io**.  
This repository serves as a personal portfolio project demonstrating applied data analysis and data engineering skills.

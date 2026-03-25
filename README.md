# PATIENT DIAGNOSTIC ANALYSIS DASHBOARD
### DATABUZZ CHALLENGE - MARCH 2026

![Power BI](https://img.shields.io/badge/Tool-Power%20BI-yellow)
![Analytics](https://img.shields.io/badge/Focus-Data%20Analytics-blue)
![Status](https://img.shields.io/badge/Project-Dashboard-green)

The report is built using **Power BI**, focuses on analyzing patient diagnostic data to uncover meaningful insights that support accurate clinical decisions and improved patient care.


## 📑 TABLE OF CONTENT

- [Dashboard Preview](https://github.com/Aashriya11/Patient-Diagnostic-Analysis-Dashboard?tab=readme-ov-file#%EF%B8%8F-dashboard-preview)
- [Dashboard Video](https://github.com/Aashriya11/Patient-Diagnostic-Analysis-Dashboard?tab=readme-ov-file#-dashboard-video)
- [Dashboard Pre-Processing Process](https://github.com/Aashriya11/Patient-Diagnostic-Analysis-Dashboard?tab=readme-ov-file#%EF%B8%8F-data-pre-processing-process)
- [Dashboard Structure & Insights](https://github.com/Aashriya11/Patient-Diagnostic-Analysis-Dashboard#-dashboard-structure--insights)
- [Key Takeaways](https://github.com/Aashriya11/Patient-Diagnostic-Analysis-Dashboard?tab=readme-ov-file#-key-takeaways)
- [Tools Used](https://github.com/Aashriya11/Patient-Diagnostic-Analysis-Dashboard?tab=readme-ov-file#-tools-used)
- [Connect](https://github.com/Aashriya11/Patient-Diagnostic-Analysis-Dashboard#-connect)


## 🖼️ DASHBOARD PREVIEW

![Dashboard gif](https://github.com/Aashriya11/Patient-Diagnostic-Analysis-Dashboard/blob/ba81485052c77fd1dd6bb29b5d832effc2664bfb/Assets/Dashboard%20gif.gif)

🔗Explore the Live Dashboard - [Click Here](https://app.powerbi.com/view?r=eyJrIjoiNTI4ZDNlMGYtMTJiOC00NjVjLWE1MjYtM2IzOTA0MjIwMDhkIiwidCI6IjUxMTBiMWYwLTk4N2YtNGNlYi05NTk1LTM2NWViZDk0NTFjNyJ9)


## 🎥 DASHBOARD VIDEO

https://github.com/user-attachments/assets/d74463c6-4bfe-413c-8ec5-29784712539f


## 🛠️ DATA PRE-PROCESSING PROCESS
The first stage of preparing the datasets for analysis involved accurate analysis and efficient reporting, the dataset was transformed and structured using a star schema approach, separating data into Fact and Dimension tables for better performance and scalability.


### 1- Data Feature Engineering:- (In Excel)
Create a structure Patient Detail Dim_Table. The Partient Detail Dimension Table creation involves restructuring the raw patients data from the dataset. This process includes:
* Separating Patients details from Fact_Patient Symptoms Table.
* Creating a dimension table with cleaned and structures patient information.
* Retaining only the first visit data for each patient to ensure unique patient records. (usage of claude.ai for getting the best suitable data)
[Click here to get prompt](https://github.com/Aashriya11/Patient-Diagnostic-Analysis-Dashboard/blob/0542ac0655d5cca71c626fbabd094e6814b6ebf0/Assets/AI%20Prompt.png)

***Pupose:** The Patient Profile Dim_Table enables more efficient analysis & quering of patient data by poviding a clean, structured and unique set of patient profiles.*

### 2- Data Modeling Approach:- (In PowerBI)
* Implemented one-to-many relationships between dimension tables and the fact table
* Ensured proper data normalization to avoid redundancy
* Applied data cleaning and transformation techniques for consistency and accuracy

| Table Name              | Table Type        | Description |
|------------------------|------------------|-------------|
| Fact_PatientSymptoms   | Fact Table       | Central table containing patient-level transactional data including symptoms, risk levels, admission status and vital readings. |
| Dim_PatientDetails     | Dimension Table  | Stores patient demographics such as age, age group and visit behavior for segmentation analysis. |
| Dim_DateTable          | Dimension Table  | Date table with Year, Month and Date hierarchy for time-based analysis and trends. |
| Dim_BloodTestResults   | Dimension Table  | Contains lab test metrics like Hemoglobin, ESR, CRP, etc used for diagnostic insights. |
| Dim_FeverTypeProfile   | Dimension Table  | Includes symptom categories such as body pain, chills, cough, etc to analyze fever patterns. |
| Dim_Medication         | Dimension Table  | Holds medication details like dosage, frequency and duration for treatment analysis. |
| Measure Table          | Supporting Table | Stores all DAX measures (KPIs like Admission Rate %, Avg Patient Age) for better model organization. |
| Prm_Location           | Supporting Table | Parameter table used for dynamic location-based filtering and interactive analysis. |



## 📋 DASHBOARD STRUCTURE & INSIGHTS
Built 3-page Power BI dashboard focusing on:
* Overview
* Patient Visit & Diagnostic Overview
* Patient Medical Report



### Page 1 – Overview

This dashboard provides a high-level overview of patient diagnostics, tracking visit trends, risk distribution and demographic patterns to support data-driven healthcare decisions.

#### Key KPIs:
| Metric             | Value          |
| ------------------ | -------------- |
| Total Visits       | 10,000         |
| Total Patients     | 3,678          |
| Visit Frequency    | 2.7            |
| High Risk Patients | 1,151 (⚠︎ 31.3%) |    
| Avg Patient Age    | 43             |
| Top Fever Type     | Viral          |

> *Note: **High-risk patients** are calculated based on the patient’s last visit to ensure the most accurate and current health status.*

#### Key Insights:
* Patient visits show fluctuating trends over time, indicating possible seasonal or external influences on healthcare demand.
* A significant rise in high-risk patients (31.3%) highlights the need for proactive monitoring and early intervention.
* Viral fever emerges as the most common diagnosis with infectious diseases contributing heavily to patient cases.
* Adults (25–44) and key locations like Guntur and Hyderabad drive the majority of visits, indicating concentrated healthcare demand in specific segments.



### Page 2 – Patient Visit & Diagnostic Overview

This dashboard provides a detailed view of patient visits, admission trends and chronic risk indicators, helping identify patterns in patient behavior and diagnostic health conditions.

#### Key KPIs:
| Metric                      | Value        |
| --------------------------- | ------------ |
| Admission Rate %            | 65.8%        |
| Diabetic Patients           | 47 (⚠︎ 1.3%) |
| Thyroid Risk Patients       | 580 (⚠︎ 15.8%) |
| Liver Disease Risk Patients | 106 (⚠︎ 2.9%)  |
| Asthma Risk Patients        | 607 (⚠︎ 16.5%) |
| Avg Gap Between Visits      | 160 Days     |

> *Note: **Diabetic , Thyroid risk , Liver disease risk & Asthma risk patients** are calculated based on the patient’s last visit to ensure the most accurate and current health status.*

#### Key Insights:
* Admission rate stands at 65.8%, indicating a significant proportion of patients requiring hospital care.
* Chronic conditions like Asthma (607) and Thyroid Risk (580) are highly prevalent, highlighting key health concerns among patients.
* Visit patterns show many patients returning after longer gaps (3–4+ months), suggesting irregular follow-ups or delayed care.
* Diagnostic data reveals a mix of normal and high-risk indicators, emphasizing the need for continuous monitoring and early diagnosis.



### Page 3 - Patient Medical Report

This dashboard provides a detailed patient-level view, combining medical history, symptoms, medications and lab results to enable comprehensive diagnostic analysis and personalized care insights.

* Patient history shows multiple visits with varying risk levels, indicating fluctuating health conditions over time.
* Presence of high-risk indicators and admissions suggests the need for continuous monitoring and timely intervention.
* Symptom tracking reveals recurring issues like fever and fatigue, helping identify patterns in patient health.
* Blood test results and medical records highlight a mix of normal and abnormal parameters, supporting detailed diagnostic evaluation and personalized treatment planning.



## 🔍 KEY TAKEAWAYS

* **Patient Trends & Risk Growth:** Patient visits show dynamic trends with moderate engagement, but a rising proportion of high-risk cases highlights the need for proactive healthcare strategies.

* **Disease & Health Patterns:** Infectious diseases (especially viral) along with chronic conditions like asthma and thyroid risks are key contributors to the overall patient load.

* **Patient Behavior & Visit Patterns:** Irregular visit frequency and longer gaps between visits indicate delays in follow-ups and gaps in continuity of care.

* **Demographics & Location Insights:** Adults and specific high-density locations contribute the majority of patient visits, showing concentrated healthcare demand.

* **Patient-Level Diagnostic Insights** Detailed analysis reveals fluctuating risk levels and recurring symptoms, emphasizing the need for continuous monitoring and personalized treatment.

* **Overall Impact:** The dashboard enables data-driven decision-making by connecting high-level trends with granular patient insights, supporting better clinical and operational outcomes.



## 🛠 Tools Used

- Power BI  
- DAX  
- Data Modeling  
- Data Visualization
- Canva
- Excel 



## 🔗 Connect

**Made By:** Aashriya Rawat  
**LinkedIn Post:** [Click Here](https://www.linkedin.com/posts/aashriya-rawat_databuzz-dataanalytics-powerbi-activity-7442227701572075520-IOKx?utm_source=share&utm_medium=member_desktop&rcm=ACoAAEaKQXIB1-GIE2Nng4OT5hcLpf_ah6hUxno)

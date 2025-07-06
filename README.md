# 👤 Employee Attrition Analysis


## 🎯 Project Summary

This Power BI project presents an in-depth analysis of employee attrition using the publicly available IBM HR Analytics Employee Attrition & Performance dataset from Kaggle [IBM HR Analytics Employee Attrition & Performance](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset). It focuses on uncovering key factors influencing employee turnover and providing actionable insights for HR decision-makers. The dashboard highlights attrition trends by department, role, gender, tenure and job satisfaction.


## 🔧 Tools & Technologies

Kaggle Dataset – IBM HR Employee Attrition & Performance (1,470 employees)
Power BI – Data visualisation and interactive dashboard design
DAX – For calculated metrics like attrition rate and satisfaction scores


## 🚀 Workflow Overview

📂 Data Preparation

Created new calculated fields (e.g., Avg Tenure, Attrition Count)
Encoded categorical variables for slicers

📊 Dashboard Design

KPI Cards: Overall Attrition Rate, Total Employees, Avg. Job Satisfaction
Bar Chart: Attrition Rate by Department
Matrix: Attrition by Job Role and Tenure
Pie Chart: Gender Distribution in Attrition
Line Chart: Attrition by Years at Company
Histogram: Age Distribution (Attrition vs Non-Attrition)

📐 DAX Calculations

Avg Job Satisfaction = AVERAGE('HR-Employee-Attrition'[JobSatisfaction])

Avg Tenure = AVERAGE('HR-Employee-Attrition'[YearsAtCompany])

Employee Count = COUNTROWS('HR-Employee-Attrition')

Attrition % by Dept = 
DIVIDE(
    CALCULATE(COUNTROWS('HR-Employee-Attrition'), 'HR-Employee-Attrition'[Attrition] = "Yes"),
    CALCULATE(COUNTROWS('HR-Employee-Attrition'))
)

Attrition Count = 
CALCULATE(
    COUNTROWS('HR-Employee-Attrition'),
    'HR-Employee-Attrition'[Attrition] = "Yes"
)

Overall Attrition Rate = 
DIVIDE(
    COUNTROWS(FILTER('HR-Employee-Attrition', 'HR-Employee-Attrition'[Attrition] = "Yes")),
    COUNTROWS('HR-Employee-Attrition'),
    0
)

Total Attrition Count = 
CALCULATE(
    COUNTROWS('HR-Employee-Attrition'),
    'HR-Employee-Attrition'[Attrition] = "Yes"
)


## 🧠 Key Insights

Sales and HR departments show the highest attrition rates
Majority of attrition occurs within the first 2 years
Lower job satisfaction is associated with higher attrition
Gender-wise attrition is nearly balanced with slight male dominance


## 📷 Dashboard Preview

[🔗 Click here to view the full Power BI dashboard preview (PDF)][(dashboard/dashboard_preview.pdf](https://github.com/SebnemKeles/Employee-Attrition-Analysis/blob/main/HR%20Employee%20Attrition.pdf)]


## 📈 Project Metrics

Metric	Value
Overall Attrition Rate - 16%
Total Employees Analysed - 1,470
Average Job Satisfaction - 2.73 / 5
Highest Attrition Department - Sales (20.6%)


## 💡 Future Improvements

Introduce time-series trends (monthly/quarterly attrition)
Add voluntary vs. involuntary attrition breakdown
Benchmark against industry standards
Integrate predictive ML models (e.g., attrition risk scoring)


## ✅ Status
✔️ Completed (Individual Project)
This project was created as a personal portfolio project based on the IBM HR dataset from Kaggle to showcase Power BI, DAX, and data storytelling skills.

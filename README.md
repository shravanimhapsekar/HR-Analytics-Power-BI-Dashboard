# HR-Analytics-Power-BI-Dashboard
This HR Analytics Dashboard analyzes employee attrition using Excel and Power BI. It identifies key factors like age, job role, salary, and education that influence why employees leave. The dashboard includes KPIs, interactive filters, and visuals to help HR teams make data-driven decisions and improve retention strategies.

## Problem Statement
The organization is experiencing ongoing employee attrition, but the exact reasons behind it are unclear. Without clear visibility into the contributing factors — such as age, job role, salary, education level, and years at the company — it becomes difficult for HR teams to design effective retention strategies.

To address this, a data-driven solution is needed to analyze patterns in employee exits and uncover key insights. The HR Analytics Dashboard was created to visualize and track attrition trends across departments using interactive filters, KPIs, and detailed charts. This dashboard aims to help HR professionals identify problem areas, understand employee behavior, and make informed decisions to reduce attrition and improve workforce stability.

## Steps followed 
- Step 1 (Data Collection) : Load data into Power BI Desktop, dataset is a csv file. The dataset includes employee demographics, job satisfaction, compensation, and attrition status.
- Step 2 (Initial Exploration in Excel) : Used Pivot Tables and Pivot Charts to explore patterns related to attrition. Applied filters to test variables like Gender, Department, Education Field, and Salary to identify meaningful insights.
- Step 3 (Data Cleaning in Power BI (Power Query Editor)) : Removed column "YearsWithCurrManager" containing null values. Identified and removed duplicate records using EmpID as the unique key. Standardized inconsistent data entries (e.g., TravelRarely vs Travel_Rarely) using Replace Values. Detected and corrected data types using the "Detect Data Type" feature.
- Step 4 (Data Transformation) : Converted Attrition column from Yes/No to binary (1/0) using a Conditional Column for numerical analysis. Removed unnecessary columns and cleaned the dataset for reporting.
- Step 5 (Creating DAX Measures) : Created custom measure for Attrition Rate.
             
           AttritionRate = SUM(HR_Analytics[AttritionCount]) / SUM(HR_Analytics[EmployeeCount])
  Calculated KPIs like Average Age, Average Salary, and Years at Company.
- Step 6 (Building the Dashboard in Power BI) : Added interactive slicers/filters. Designed KPI cards for high-level metrics (Total Employees, Attrition, etc.). Created six visualizations to show attrition by Education, Age, Job Role, Salary Slab, Tenure, and Job Satisfaction.
- Step 7 (Formatting & Alignment) : Applied consistent color schemes and conditional formatting (e.g., matrix heatmap).

## Snapshot of Dashboard (Power BI Service)
![Image](https://github.com/user-attachments/assets/9fcea257-b95d-4e14-bc52-6833909e5144)

## Insights
1. Overall Attrition Rate is 16.1% : Out of 1,470 employees, 237 have left the company. This is a moderately high attrition rate, suggesting possible issues with engagement, compensation, or role satisfaction.
2. Most Attrition Comes from the 26–35 Age Group : 116 employees who left are in the 26–35 age group — almost half of total attrition. This is often a high-mobility age range; targeted retention strategies for this age group are crucial.
3. Employees with Life Sciences and Medical Education Are Leaving the Most : Life Sciences (38%) and Medical (27%) graduates account for 65% of total attrition. Indicates a potential mismatch between job expectations and the role offered, or better opportunities outside.
4. Lower Salary Slabs Face the Highest Attrition : 163 out of 237 employees who left were earning less than 5K. Very few high earners left the company, indicating compensation is a key factor in attrition.
5. High Attrition in First Few Years : Highest attrition occurred during 1st and 2nd years, especially at year 1 (59 exits). Shows that many employees don’t stay beyond early onboarding or training phase — early engagement needs improvement.
6. Laboratory Technicians and Sales Executives Resigned the Most : Laboratory Technicians (62) and Sales Executives (57) together make up nearly half the total attrition. These roles may involve repetitive work or performance pressure — job satisfaction or work-life balance might be low.
7. Low Job Satisfaction Correlates Strongly with Attrition : Out of 237 resignations - 66 employees rated their job satisfaction as 1 and 46 rated it as 2. This means almost 47% of employees who left had very low satisfaction — a clear indicator of disengagement.
8. Male Employees Show Higher Attrition : 140 males resigned compared to 79 females. Though this might reflect the gender distribution in the company, it suggests male employees might be more prone to leaving.

## Acknowledgements
This dashboard is built as part of a Data Visualization and Analytics learning project. Inspired by Rishabh Mishra – YouTube.






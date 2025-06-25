# HR-Analytics-Power-BI-Dashboard
This HR Analytics Dashboard analyzes employee attrition using Excel and Power BI. It identifies key factors like age, job role, salary, and education that influence why employees leave. The dashboard includes KPIs, interactive filters, and visuals to help HR teams make data-driven decisions and improve retention strategies.

## Problem Statement
The organization is experiencing ongoing employee attrition, but the exact reasons behind it are unclear. Without clear visibility into the contributing factors — such as age, job role, salary, education level, and years at the company — it becomes difficult for HR teams to design effective retention strategies.

To address this, a data-driven solution is needed to analyze patterns in employee exits and uncover key insights. The HR Analytics Dashboard was created to visualize and track attrition trends across departments using interactive filters, KPIs, and detailed charts. This dashboard aims to help HR professionals identify problem areas, understand employee behavior, and make informed decisions to reduce attrition and improve workforce stability.

### Steps followed 
- Step 1 (Data Collection) : Load data into Power BI Desktop, dataset is a csv file. The dataset includes employee demographics, job satisfaction, compensation, and attrition status.
- Step 2 (Initial Exploration in Excel) : Used Pivot Tables and Pivot Charts to explore patterns related to attrition. Applied filters to test variables like Gender, Department, Education Field, and Salary to identify meaningful insights.
- Step 3 (Data Cleaning in Power BI (Power Query Editor)) : Removed column "YearsWithCurrManager" containing null values. Identified and removed duplicate records using EmpID as the unique key. Standardized inconsistent data entries (e.g., TravelRarely vs Travel_Rarely) using Replace Values. Detected and corrected data types using the "Detect Data Type" feature.
- Step 4 (Data Transformation) : Converted Attrition column from Yes/No to binary (1/0) using a Conditional Column for numerical analysis. Removed unnecessary columns and cleaned the dataset for reporting.
- Step 5 (Creating DAX Measures) : Created custom measure for Attrition Rate.
             
           AttritionRate = SUM(HR_Analytics[AttritionCount]) / SUM(HR_Analytics[EmployeeCount])
  Calculated KPIs like Average Age, Average Salary, and Years at Company.
- Step 6 (Building the Dashboard in Power BI) : Added interactive slicers/filters. Designed KPI cards for high-level metrics (Total Employees, Attrition, etc.). Created six visualizations to show attrition by Education, Age, Job Role, Salary Slab, Tenure, and Job Satisfaction.
- Step 7 (Formatting & Alignment) : Applied consistent color schemes and conditional formatting (e.g., matrix heatmap).


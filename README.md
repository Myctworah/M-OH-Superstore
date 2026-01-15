#  Sales Performance and Business Intelligence Analysis  
## M’OH Superstore (Power BI Project)

 
 

---

##  Executive Summary
This project analyzes sales performance data recorded at **hourly, daily, weekly, and monthly** levels for a fictional retail business, **M’OH Superstore**. The objective was to transform raw, multi-granular sales data into a unified analytical model that supports time-based analysis and business decision-making.

Using **Power BI**, the project involved data cleaning, transformation (unpivoting), dimensional modeling with a central date table, DAX calculations for key performance indicators, and the development of an interactive dashboard. The final dashboard provides insights into revenue trends, product category performance, sales behavior by weekday and hour, and overall business growth patterns.

---

##  Introduction
Retail businesses generate sales data at different time intervals depending on operational needs. However, analyzing such datasets becomes challenging when they exist as separate tables with different granularities.

This project focuses on solving that challenge by:
- Preparing each dataset correctly  
- Designing a scalable data model  
- Enabling accurate time intelligence analysis  
- Delivering clear, interactive dashboards for stakeholders  

---

##  Aim and Objectives

### **Aim**
To build a comprehensive sales performance dashboard that enables time-based and product-level analysis across multiple sales granularities.

### **Objectives**
1. Clean and standardize hourly, daily, weekly, and monthly sales datasets  
2. Transform wide-format sales data into an analysis-ready structure  
3. Create a centralized **Date Dimension Table**  
4. Build a star-schema data model with correct relationships  
5. Develop DAX measures for KPIs such as Total Revenue, MoM Growth, and YTD Sales  
6. Design an intuitive, interactive dashboard suitable for business users  

---

##  Business Questions
The analysis was guided by the following business questions:

1. What is the total revenue generated within the selected period?  
2. How do sales trend across months?  
3. Which product categories generate the highest revenue?  
4. How does sales performance vary by weekday?  
5. At what hours of the day do sales peak?  
6. How does current performance compare to previous periods (MoM growth)?  
7. What is the Year-to-Date (YTD) sales performance?  
8. Are there noticeable patterns in customer purchasing behavior over time?  

---

##  Data Cleaning Processes
The dataset was provided in four separate tables:
1. Hourly sales  
2. Daily sales  
3. Weekly sales  
4. Monthly sales  

Each dataset contains:
- Date information  
- Product category  
- Sales values  

The datasets were modeled together using a **star schema**.

### **Cleaning Steps Applied**
- Verified data types for date, numeric, and categorical columns  
- Removed unnecessary blank and null values  
- Standardized column naming across tables  
- Ensured consistent product category naming  
- Confirmed date consistency across all tables  
- No rows were removed arbitrarily to preserve data integrity  

---

##  Data Preparation and Modelling Process

### 1. Unpivoting
The original sales tables were in a wide format where product categories were stored as separate columns. These were unpivoted to create:
- `Product Category`
- `Sales`

This step normalized the data and made it suitable for aggregation and filtering.

---

### 2. Date Table Creation
A dedicated **Date Table** was created to:
- Enable time intelligence calculations (MoM, YTD)  
- Act as a central filtering dimension  
- Provide attributes such as Year, Month, Weekday, and Week Number  

The presence of **12:00 AM** in the date column is expected, as the table represents date-level granularity unless time is explicitly added.

**Date Table Columns:**
- Date  
- Year  
- Month  
- Month Number  
- Weekday Name  
- Week Number  

---

### 3. Data Model
- Each sales table was connected to the Date Table using the `Date` column  
- Relationships were:
  - One-to-many  
  - Single-directional filtering for optimal performance  

This resulted in a clean, optimized **star schema**.

---

##  DAX Measures
Key measures created include:
- **Total Revenue**
- **Year-to-Date (YTD) Sales**
- **Month-over-Month (MoM) Growth**

Time intelligence functions such as `DATEADD()` and `TOTALYTD()` were used to enable period-over-period analysis.

---

##  Dashboard and Visual Design

###  Executive Overview Dashboard

#### **1. KPI Cards**
| KPI | Value |
|---|---|
| Total Revenue | 127.60K |
| MoM Growth % | Varies |
| Year-to-Date Sales | 17.08K |
| Total Products | 8 |

---

#### **2. Interactivity**
Dynamic slicers were added for:
- Year  
- Month  
- Product Category  
- Weekday  

Cross-filtering was enabled across all visuals.

---

#### **3. Charts Used**
- Line Chart: Monthly sales trend  
- Column Chart: Sales by weekday  
- Bar Chart: Top product categories  
- Line Chart: Hourly sales trend  

---

#### **4. Design Considerations**
- Consistent color theme  
- Clear titles and labels  
- Logical layout for readability  
- Responsive filtering using slicers  

---

##  Key Insights and Findings
- Sales exhibit clear **seasonal trends** at the monthly level  
- Certain weekdays consistently outperform others  
- Sales peak during specific hours, indicating strong time-based purchasing behavior  
- A small number of product categories contribute the majority of revenue  

---

##  Business Recommendations
Based on the analysis:
1. Focus marketing efforts on high-performing weekdays and peak sales hours  
2. Optimize inventory for top-selling product categories  
3. Investigate low-performing time periods for promotional opportunities  
4. Use MoM and YTD metrics for continuous performance monitoring  
5. Adjust staffing levels during peak hourly sales windows  

---

##  Conclusion
This project demonstrates how multi-granular sales data can be transformed into a unified, business-ready analytical solution using **Power BI**. Through effective data cleaning, modeling, DAX calculations, and dashboard design, actionable insights were generated to support informed business decision-making.

---

##  Author
**Hassan Mistura Olaitan**
*Data Analyst*
PowerBi | Data Cleaning | Data Modelling | Data Analysis | Data Visualization


 *If you found this project insightful, feel free to explore the dashboard and datasets included in this repository.*


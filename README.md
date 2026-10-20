# Global-Superstore-Sales-Performance
![Power BI](https://img.shields.io/badge/Tool-Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Domain](https://img.shields.io/badge/Domain-Sales%20Analytics%20%7C%20Business%20Intelligence-teal)

## Table of Contents
1. [Project Overview](#project-overview)
2. [Problem Statement](#problem-statement)
3. [Business Questions](#business-questions)
4. [Dataset Description](#dataset-description)
5. [Tools Used](#tools-used)
6. [Importing the Dataset](#importing-the-dataset)
7. [Data Cleaning and Transformation](#data-cleaning-and-transformation)
8. [Data Analysis](#data-analysis)
9. [Dashboard](#dashboard)
10. [Key Findings](#key-findings)
11. [Recommendations](#recommendations)
12. [Conclusion](#conclusion)
13. [Project Files](#project-files)
14. [Contact Information](#contact-information)
 
## Project Overview
In this project, I play the role of a Business Intelligence Analyst working for a national retail company. Management asked for an executive dashboard that enables them monitor sales performance, profitability, customer behavior, and regional performance, and I prepared the data, built the dashboard in Power BI, and wrote up the findings and recommendations based on my analysis.

## Problem Statement
Senior management has raw transaction data but no quick way to see how the business is performing. They need to know where sales and profit come from, which customers, regions, categories, and products drive results, and where money is being lost. Without a single view, those questions take too long to answer and decisions get delayed.

This dashboard puts the answers on one page so management can filter, compare, and make informed strategic decisions.

## Business Questions
The dashboard is built to answer seven questions from management:
* What is the overall sales performance of the company?
* Which regions generate the highest sales and profit?
* Which customer segments contribute the most revenue?
* Which product categories perform best?
* Which products are the most profitable?
* What trends can be observed over time?
* What recommendations should management implement to improve business performance?

## Dataset Description
The dataset is the Global Superstore sales data (Global_Superstore_data.csv). It has 51,290 rows and 24 columns, and each row is one order line. Order dates run from 1 January 2011 to 31 December 2014.

Across the dataset there are 25,035 unique order IDs, 1,590 customers, 10,292 products and 147 countries, grouped into 13 regions and 7 markets (US, Canada, LATAM, EU, EMEA, Africa and APAC).

The columns fall into a few groups:
* Order details: Row ID, Order ID, Order Date, Ship Date, Ship Mode and Order Priority.
* Customer details: Customer ID, Customer Name and Segment (Consumer, Corporate, Home Office).
* Location: City, State, Country, Postal Code, Market and Region.
* Product details: Product ID, Category (Furniture, Office Supplies, Technology), Sub-Category and Product Name.
* Measures: Sales, Quantity, Discount, Profit and Shipping Cost.

Ship Mode has four values: Same Day, First Class, Second Class and Standard Class. Order Priority also has four: Critical, High, Medium and Low. Both are used as slicers on the dashboard.

## Tools Used
* Microsoft Power BI for data modeling, DAX measures and the dashboard itself.
* Power Query for cleaning and transforming the data.

## Importing the Dataset
Open Power BI Desktop and select Get Data > Text/CSV.
Choose Global_Superstore_data.csv and review the preview.
Click Transform Data to open Power Query and clean the data before loading it into the model.

## Data Cleaning and Transformation
The cleaning was done in Power Query before building any visuals:
* Checked the data types of every column and set Order Date and Ship Date as dates. The source stores them in dd-mm-yyyy format, so the locale had to be set correctly or the days and months would swap.
* Confirmed there are no duplicate rows and no missing values in the fields the dashboard relies on (sales, profit, category, segment, country, region and dates).
* Noted that Postal Code is blank for most non-US rows. It is not used in any visual, so it was left out of the analysis.
* Created a Year field from Order Date to drive the sales trend.
* Created the DAX measures behind the KPI cards: Total Sales, Total Profit, Total Orders, Average Sales and Profit Margin (Total Profit divided by Total Sales).
* Renamed fields and fixed formatting so labels and number formats read cleanly in the visuals.

## Data Analysis
The analysis looked at the business from five angles:
* Overall KPIs: total sales, profit, order count, average sales per order line and profit margin.
* Customer segment: how sales split between Consumer, Corporate and Home Office customers.
* Product category: profit by Furniture, Office Supplies and Technology, plus order counts by category and segment.
* Geography: the top 5 countries by number of orders and total sales by region.
* Time and products: the sales trend from 2011 to 2014 and the top 10 products ranked by profit.

Two slicer groups let users filter the whole page by Order Priority (Critical, High, Medium, Low) and by Ship Mode (First Class, Same Day, Second Class, Standard Class).

## Dashboard
<img width="1446" height="811" alt="Screenshot (263)" src="https://github.com/user-attachments/assets/7e1fe411-06e5-419d-9d69-f47b6e622d42" />

The dashboard has three layers. The top row holds the five KPI cards and the slicers. The middle row covers orders by category and segment, the top 5 countries by orders, sales share by segment and profit by category. The bottom row shows the top 10 products by profit, sales by region and the yearly sales trend.

## Key Findings
* The business generated $12.64M in total sales and $1.47M in total profit from about 51K orders, which gives an overall profit margin of 11.61%. Average sales per order line were $246.49.
* The Consumer segment brought in the most revenue, about $6.51M, or 51.48% of total sales. Corporate contributed 30.25% and Home Office 18.27%.
* Technology was the most profitable category at roughly $0.66M. Office Supplies followed with about $518K and Furniture had the lowest profit at about $285K.
* Office Supplies had the most orders (31,273), well ahead of Technology (10,141) and Furniture (9,876).
* The United States had the highest number of orders among the top 5 countries, with about 10K. Australia and France each had about 2.8K, then Mexico (2.6K) and Germany (2.1K).
* The Central region had the highest sales at about $2.8M, followed by South ($1.6M) and North ($1.2M). Canada ($0.1M) and the Caribbean ($0.3M) were the lowest.
* Sales grew every year, from about $2.3M in 2011 to $4.3M in 2014.
* The most profitable single product, the Canon imageCLASS 2200 Advanced Copier, made about $25K in profit. Phones from Cisco and Motorola came next at roughly $17K each.

## Recommendations
* Prioritize the Consumer segment. It contributes the largest share of revenue, so retention and acquisition work here pays off most.
* Study what makes Technology work. Find out why it earns the most profit and look for ways to grow it further.
* Build targeted plans for weaker regions and categories. Review customer demand, product mix, pricing, discounting and delivery performance in places like Canada and the Caribbean, and in Furniture.
* Favor high-margin products and strong customer segments to grow sales without eroding profit.
* Protect the top performers. Use cross-selling, bundling and targeted promotions on highly profitable products such as copiers and phones.
* Keep tracking the sales trend, and watch profit alongside it. Growth only helps if profit keeps pace with it.

## Conclusion
The dashboard gives management a clear, single-page view of where sales come from, which products and categories earn the money, and how each region is performing. Sales have nearly doubled in four years, and Technology and the Consumer segment lead the way. The next step is making sure profit growth stays healthy as revenue climbs.

This project strengthened my practical skills in Power BI, data cleaning and transformation, KPI development, data visualization, interactive dashboard design, business intelligence, data storytelling, insight generation and business recommendations.

## Project Files
* [View Dataset](./Global_Superstore_data.csv)
* [View power BI Report](./Global_Superstore_BIreport.pbix).

## Contact Information
* Email: aladeloyeesther616@gmail.com
* LinkedIn: https://linkedin.com/in/estheraderonke

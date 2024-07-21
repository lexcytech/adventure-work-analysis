# ADVENTURE-WORK-ANALYSIS
![](https://github.com/lexcytech/adventure-work-analysis/blob/main/project2/download.png)

## Project Overview 
Project Objective: Comprehensive Sales and Customer Analysis
The objective of this project is to conduct a comprehensive analysis of sales and customer data to uncover insights that can drive business growth and operational efficiency. The analysis will focus on understanding sales trends, customer behavior, product performance, and territorial distribution, as well as optimizing order fulfillment and inventory management.
---
## Data Source/description 
I was given a folder containing raw csv files.
This dataset contains sales transactions from a chain store, spanning three years from 2015 to 2017. The data captures various aspects of the sales process, including order details, product information, customer demographics, and territorial distribution. This comprehensive dataset provides a foundation for in-depth analysis and insights into sales performance, customer behavior, and operational efficiency
![](project2/rawfile_folder)
---
## Skills demonstrated/ Tools 
1.	Excel for data connection 
2.	Powerbi for data cleaning, transformation, Modeling, creating report and dashboard
   ---
### DATA CLEANING AND TRANSFORMANTION 
 The dataset was loaded and inspected before cleaning and transformation were carried out as follows:
1.  **Product Table**:
The product price and cost were formatted to two decimal places.
A dollar sign was added to the columns to indicate the prices were calculated in dollars.
2. **Customer Table**:
The first name and last name were merged to create a new column called "Fullname."
The gender column was transformed from "M" to "Male" and "F" to "Female."
The marital status column was transformed from "S" to "Single" and "M" to "Married."
All other redundant columns were deleted.
3. **Calendar Table**:
The Calendar table was imported into Power BI from the raw CSV file.
Transformation in Power Query Editor
Opened the Calendar table in the Power Query Editor.
Adding New Columns as follows
-   *Start of the Week*.
Formula:
StartOfWeek = Date.StartOfWeek([Date])
-   *start of the month*.
Formula:
StartOfMonth = Date.StartOfMonth([Date])
-   *Day Name*.
Formula:
DayName = Date.ToText([Date], "dddd")
-   *Month Name*
Formula:
MonthName = Date.ToText([Date], "MMMM")
-   *Year*
Formula:
Year = Date.Year([Date])
![](https://github.com/lexcytech/adventure-work-analysis/blob/main/project2/rawfile_folder/Calendar.csv)
    **Validation**
Ensured that the new columns contained the correct values by cross-referencing a sample of dates with an external calendar.
Applied the changes and loaded the transformed Calendar table back into the Power BI model.

3.    **Sales Table**:
The sales tables from 2015, 2016, and 2017 were merged to create a new table called "sale adventure."
The stock date column was formatted to the data type "Date."
An "Amount Paid" column was created using DAX to relate the unit price in the product table and the quantity in the sales table.
An "Order Profit" column was created using DAX to relate the product cost, unit price in the product table, and the order quantity in the sales table.
Two DAX measures were created: one summing the "Amount Paid" column to calculate "Total Revenue" and another summing the "Order Profit" column to calculate "Total Profit."

## ANALYSIS OBEJECTIVES AND FINDINGS 
1. **Total Sales**:
Analysis: The dashboard shows a total sales amount of 84.17K.
Objective: Aim to increase total sales by implementing targeted marketing campaigns and promotional activities to boost revenue.
2. **Number of Customers**:
Analysis: There are 18K unique customers.
Objective: Expand the customer base by reaching new markets and improving customer retention strategies.
3. **Number of Transactions**:
Analysis: The total number of transactions is 56K.
Objective: Increase transaction volume by encouraging repeat purchases and optimizing the sales process to make transactions smoother.
4. **ender Distribution**:
Analysis: The gender distribution shows 8892 females and 9K male customers.
Objective: Develop gender-specific marketing strategies to cater to both male and female customers effectively and boost overall customer engagement.
5. **Orders by Product Category**:
Analysis:
Accessories have the highest number of orders.
Bikes come second, and Clothing has the least number of orders.
Objective: Focus marketing and sales efforts on the Accessories category to leverage its popularity, while also developing strategies to boost sales in the Bikes and Clothing categories.
6. **Revenue by Product Name**:
Analysis:
Specific models of Mountain Bikes (e.g., Mountain-200 Black, Mountain-200 Silver) have generated significant revenue, each around 1M.
Objective: Continue promoting top-selling products and explore opportunities to introduce similar high-demand models to maximize revenue.
7. **Profit by Product Subcategory**:
Analysis:
Road Bikes and Mountain Bikes are the top profit-generating subcategories.
Other subcategories like Tires and Tubes, Fenders, and Jerseys generate less profit.
Objective: Prioritize investment in high-profit subcategories while analyzing and improving the performance of lower-profit subcategories through cost optimization and targeted promotions.
8. **Revenue by Country**:
Analysis:
Countries like Australia, Canada, France, Germany, the United Kingdom, and the United States show significant revenue and profit contributions.

9.   **Revenue by Customer**
Visual Setup: Bar chart showing total revenue generated by the top five customers.
Objective: Identify key customers who contribute significantly to the revenue to develop targeted marketing strategies, loyalty programs, or personalized services to retain these customers and enhance their spending.
10.   **Total Sales**
Visual Setup: Card visual displaying the total sales amount, which is 84.17K.
Objective: Provide a high-level summary of total sales achieved, serving as a key performance indicator (KPI) for overall sales performance and aiding in setting future sales targets.

10.   **Total Order by Month**
Visual Setup: Bar chart illustrating the total order count by month, highlighting peak sales periods and slower months.
Objective: Understand seasonal demand to optimize inventory levels, staffing, and marketing campaigns accordingly, and plan promotions during slower months to boost sales and improve revenue consistency throughout the year.

11.   **Revenue by Year (Pie Chart)**
Visual Setup: Pie chart breaking down the revenue by year: 2015 (36.87%), 2016 (25.71%), and 2017 (37.42%).
Objective: Compare revenue distribution across different years to identify growth trends and year-on-year performance, aiding in assessing yearly performance, strategic planning, budget allocation, and resource management.
12.   **Number of Products**
Visual Setup: Card visual displaying the total number of products, which is 293.
Objective: Monitor the total number of products in the inventory to ensure a diverse product range that meets customer needs, avoid overstocking or stockouts, and evaluate product performance for inventory optimization.

13.   **Revenue by Year (Bar Chart)**
Visual Setup: Bar chart showing total revenue for each year, providing a straightforward comparison of yearly revenue.
Objective: Assess yearly revenue performance to set realistic revenue goals, track progress, and adjust sales strategies as needed.
14.   **Profit Trend by Year**
Visual Setup: Line chart illustrating the profit trend over the years, showing a clear trend of increasing profit from 2015 to 2017.
Objective: Track profit growth to identify years with significant profit changes, investigate underlying causes, and replicate successful strategies or address issues contributing to declines.
15.   **Profit by Product Subcategory**
Visual Setup: Bar chart displaying profit by product subcategory, highlighting the most profitable categories like Road Bikes, Mountain Bikes, and Touring Bikes.
Objective: Determine which product subcategories are the most profitable, focus sales and marketing efforts on these high-profit categories, and consider expanding these categories or developing similar products to maximize overall profitability.
---

## Overall recommendation 
**Sales and Customer Base Expansion**:
-   Marketing Campaigns: Develop targeted marketing campaigns to attract new customers and retain existing ones. Utilize insights from the high-performing product categories and regions.
-   Loyalty Programs: Implement loyalty programs to encourage repeat purchases and reward high-value customers.
    -   Seasonal Promotions: Leverage peak sales months (June, May, December) by offering seasonal promotions and discounts.
   **Product Portfolio Optimization**:
-   Focus on High-Profit Products: Continue to invest in and promote Road Bikes and Mountain Bikes, which are the most profitable subcategories.
-   Diversify Product Range: Analyze customer preferences to introduce new products or variations in lower-performing subcategories like Tires and Tubes, Fenders, and Jerseys.
-    Product Development: Consider developing new models similar to the top-performing Mountain Bikes (e.g., Mountain-200 series) to capitalize on their popularity.
-   **Regional Strategy Enhancement**:
-	Maximize Top-Performing Regions: Strengthen marketing and distribution efforts in high-revenue regions like Australia, Canada, France, Germany, the UK, and the USA.
-	Explore New Markets: Identify potential growth opportunities in underrepresented regions and develop entry strategies to expand market presence.
-	**Customer-Centric Approaches**:
-	Gender-Specific Marketing: Create gender-specific marketing strategies to cater to both male and female customers, ensuring balanced appeal and engagement.
-	Personalized Experiences: Utilize customer data to offer personalized shopping experiences, tailored recommendations, and targeted promotions.
-	**Operational Efficiency and Performance Monitoring**:
-	Regular Performance Reviews: Continuously monitor key performance indicators (KPIs) such as total sales, number of transactions, and profit trends to adjust strategies promptly.
-	Data-Driven Decisions: Use the insights from the dashboards to make informed decisions on inventory management, product development, and marketing strategies.
-	**Customer Relationship Management (CRM)**:
-	Engage Top Customers: Focus on maintaining strong relationships with top customers like Jordan Turner, Maurice Shan, and Janet Munoz, who contribute significantly to revenue.
-	Feedback Mechanism: Implement a robust feedback mechanism to gather insights from customers and improve products and services accordingly.
-   **Profitability and Cost Management**:
-	Optimize Costs: Review and optimize operational costs in lower-profit subcategories to improve overall profitability.
-	Profit Margin Analysis: Conduct a detailed profit margin analysis to identify areas where costs can be reduced or prices can be adjusted without compromising sales.
-   **Seasonality and Demand Planning**:
-	Seasonal Inventory Management: Adjust inventory levels based on the seasonality of sales to ensure sufficient stock during peak months and avoid overstocking during low-demand periods.
-	Demand Forecasting: Implement advanced demand forecasting techniques to better predict sales trends and adjust supply chain strategies accordingly.
  ---
 ## SUMARRY
-   The analysis of the dashboards reveals strong sales performance and a balanced customer base, with notable insights into product and regional market dynamics from 2015 to 2017. Here are the key points:
1.	Total Sales: The company achieved 84.17K in total sales.
2.	Customer Base: 18K customers with a balanced gender distribution.
3.	Product Categories:
o	Accessories lead in orders.
o	Mountain Bikes, especially the Mountain-200 series, are top revenue generators.
o	Road Bikes and Mountain Bikes are the most profitable subcategories.
4.	Regional Performance:
o	Australia, Canada, France, Germany, the UK, and the USA are top-performing regions in terms of revenue and profit.
5.	Key Customers: High-value customers significantly contribute to revenue.
6.	Seasonal Trends: Sales peak in June, May, and December, indicating seasonal influences.
7.	Profit Trends: Consistent profit growth from 2015 to 2017.
Strategic Recommendations:
1.	Marketing and Customer Retention:
o	Develop targeted marketing campaigns.
o	Implement loyalty programs and seasonal promotions.
2.	Product Strategy:
o	Focus on high-profit products and diversify the product range.
o	Enhance and develop new models similar to top-performing bikes.
3.	Regional Strategy:
o	Strengthen efforts in high-revenue regions.
o	Explore new markets for expansion.
4.	Operational Efficiency:
o	Optimize costs and improve lower-performing subcategories.
o	Utilize data-driven decisions for inventory and marketing.
By leveraging these insights and implementing the recommendations, the company can enhance its sales performance, improve product offerings, and strategically expand its market presence for sustained growth and success.





 

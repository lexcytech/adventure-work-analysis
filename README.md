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
a. *Start of the Week*.
Formula:
StartOfWeek = Date.StartOfWeek([Date])
b. *start of the month*.
Formula:
StartOfMonth = Date.StartOfMonth([Date])
c. *Day Name*.
Formula:
DayName = Date.ToText([Date], "dddd")
Month Name
Added a new column to extract the name of the month from the date.
Formula:
MonthName = Date.ToText([Date], "MMMM")
Year
Added a new column to extract the year from the date.
Formula:
Year = Date.Year([Date])
Validation
Ensured that the new columns contained the correct values by cross-referencing a sample of dates with an external calendar.
Applied the changes and loaded the transformed Calendar table back into the Power BI model.
Sales Table:
The sales tables from 2015, 2016, and 2017 were merged to create a new table called "OrderTable."
The stock date column was formatted to the data type "Date."
An "Amount Paid" column was created using DAX to relate the unit price in the product table and the quantity in the sales table.
An "Order Profit" column was created using DAX to relate the product cost, unit price in the product table, and the order quantity in the sales table.
Two DAX measures were created: one summing the "Amount Paid" column to calculate "Total Revenue" and another summing the "Order Profit" column to calculate "Total Profit."



# Adidas_Sales_Analysis
### This project focuses on analysing Adidas sales for their various products

## Introduction
This project was done using Power BI. It provides insights into Adidas's product sales performance. It includes data preparation, modeling, DAX Calculations, interactive reports and publishing on the web.

## Data Preparation
In this stage, I used a data cleaning tool in Power BI called Power Query to clean and structure the data correctly. The file is primarily clean, so minimal cleaning is needed.
   - Removed the empty rows.
   - Promoted headers and changed the data type to the appropriate datatype.

## Data Modelling
In this stage, I used a star schema to optimize efficiency
   - Created a calculated date table.
```
Calendar = ADDCOLUMNS ( CALENDARAUTO (),
    "DateID", VALUE(FORMAT([Date], "YYYYMMDD")),
	"Year", YEAR([Date]), 
	"MonthNo", MONTH([Date]), 
	"Month", FORMAT([Date],"mmm"),
	"Quarter", FORMAT([Date],"\QQ"))
```
   - Established relationship between the product, location, data and sales tables.

## DAX calculation
I used the anchor, time intelligence, and variance calculation for this report. Some key measures used in this report are
   - Anchor: Total Sales, Total Profit, Transaction Count, Average Price, etc
   - Time Intelligence: Sales Year-to-Date, Profit Year-to-Date
   - Variance: Profit MOM, Sales MOM, etc

## Report building
   - Built three report pages.
1. Product page: This page displays he various products and how much sales are made from each product
![](https://github.com/thephloral/Adidas_Sales_Analysis/blob/main/Product.PNG)
2. Trend analysis page: The chart displays the sales variance by state and product. It also displays profit for every monthly sale
![](https://github.com/thephloral/Adidas_Sales_Analysis/blob/main/trendanalysis.PNG)
3. Deeper insights page: This page shows how many sales were made and the sales method with the most sale
![](https://github.com/thephloral/Adidas_Sales_Analysis/blob/main/deepinsights.PNG)

## Publishing report on Power BI Service
The report was published to the Power BI service. View the [report](https://app.powerbi.com/groups/me/reports/9aadd991-d822-4e57-8ee2-f47c63008a5f/a2bfecab78d045039bc7?experience=power-bi)





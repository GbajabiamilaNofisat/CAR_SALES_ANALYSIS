## CAR_SALES_ANALYSIS

### Overview:

**The project analyzes car sales data to uncover performance trends over time, identify top-performing model and regions, and segment customers based on purchasing value**

---

## Contents
+ [Project Overview](#Proect-Overview) |+ [Data Source](#Data-Source) |+ [Tools Used](#Tools-Used) |+ [Table Outlay](#Table-Outlay) |+ [Query Language](#Query-Language) |
+ [Visualization](#Visualization)

----
## Project Overview:
>This project presents a comprehensive analysis of Car sales data using SQL for data extraction and cleaning, Excel for detailed analysis, and Power BI for interactive visualization and dashboard creation. The analysis explores key business metrics to provide actionable insights for sales performance optimization which are Total sales by model, Sales by region and Customer segmentation by customer profit.

## Data Source:
www.kaggle.com/dataset

## Tools Outlay
* Pivot Tables / Charts
* PowerBI
* SQL

 ## Table Outlay
 First three records

|Car_id	|Date  |Customer Name	|Gender	|Annual Income	|Dealer_Name	|Company	|Model |Engine	|Transmission	|Color	|Price ($)	|Dealer_No 	|Body Style	|Phone	|Dealer_Region
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
|C_CND_000001|	1/2/2022	|Geraldine	|Male	|13500	|Buddy Storbeck's Diesel Service Inc	|Ford	|Expedition	|DoubleÃ‚Â Overhead Camshaft	|Auto	|Black	|26000	|06457-3834	|SUV	|8264678	|Middletown
|C_CND_000002|	1/2/2022	|Gia	|Male	|1480000	|C & M Motors Inc	|Dodge	|Durango	|DoubleÃ‚Â Overhead Camshaft	|Auto	|Black	|19000	|60504-7114|	SUV	|6848189	|Aurora
|C_CND_000003|	1/2/2022	|Gianna	|Male	|1035000	|Capitol KIA	|Cadillac	|Eldorado	|Overhead Camshaft	|Manual	|Red	|31500	|38701-8047	|Passenger	|7298798	|Greenville

## Query Language:
### (SQL)
Some of the query language i retrieve from the records are diplayed here

```SQL
---find the region with the most sales---
  SELECT max(Price) AS Price, Dealer_Region FROM  [dbo].[CAR DATA]
  GROUP BY Dealer_Region
  ORDER BY Price DESC;

---Profile the customer by price---
SELECT Price,
CASE
WHEN Price <= 9000 THEN 'VIP' WHEN Price >= 15000 THEN 'VVIP'
ELSE 'MVP' 
END
FROM [dbo].[CAR DATA];

```

## Visualization
### Pivot Table


 

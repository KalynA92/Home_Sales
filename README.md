# Home_Sales

## Task

1. Rename the Home_Sales_starter_code.ipynb file as Home_Sales.ipynb.

2. Import the necessary PySpark SQL functions for this assignment.

3. Read the home_sales_revised.csv data in the starter code into a Spark DataFrame.

4. Create a temporary table called home_sales.

5. Answer the following questions using SparkSQL:

* What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.

* What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.

* What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.

* What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.

6. Cache your temporary table home_sales.

7. Check if your temporary table is cached.

8. Using the cached data, run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

9. Partition by the "date_built" field on the formatted parquet home sales data.

10. Create a temporary table for the parquet data.

11. Run the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determine the runtime and compare it to uncached runtime.

12. Uncache the home_sales temporary table.

13. Verify that the home_sales temporary table is uncached using PySpark.

## Description

I started by importing all of the necessary PySpark SQL functions required. I read the CSV file into a Spark DataFrame. I created a temporary view of the DataFrame and previewed the first 10 rows. To get the average price of a four-bedroom house sold each year I selected the date, rounded the average price to two decimals, from the home_sales view, that had four bed-rooms, grouped and ordered by the date. To get the average price of a home with three bedrooms and bathrooms built each year, I selected the date_built, rounded average price to two decimals, accounted for three bed and bathrooms, grouped and ordered by the date_built. The next question added two floors and greater than or equal to two thousand square feet to the additional parameters of the previous query. I used the same methodology accounting for the added parameters of this question. For the next question I selected the "view" rating, rounded the average price to two decimals, from the home_sales view and grouping by the "view" rating when it had an average price greater than or equal to three hundred fifty thousand, and ordered by the view rating. I also printed the run time for this query which was approximately 1.63 seconds. I cached the temporary table. I ran the same query that filters out the view ratings with average price of greater than or equal to three hundred fifty thousand with the cached data. I also printed the run time for this query which was approximately 0.62 seconds. I partioned by the date_built field on the formatted parquet home sales data. I read and created a temporary table for the parquet formatted data. I ran the same query that filters out the view ratings with average price of greater than or equal to three hundred fifty thousand with the parquet DataFrame. I also printed the run time for this query which was approximately 0.55 seconds. I uncached the temporary table and confirmed it was uncached.
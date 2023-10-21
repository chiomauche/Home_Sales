# Home_Sales

I used my knowledge of SparkSQL to determine key metrics about home sales data. Then I used Spark to create temporary views, partition the data, cache and uncache a temporary table, and verified that the table has been uncached.

I answered the following questions using SparkSQL:

1. What is the average price for a four-bedroom house sold for each year? Round off your answer to two decimal places.
![Alt text](<Screenshot 2023-10-21 044732.png>)

2. What is the average price of a home for each year it was built that has three bedrooms and three bathrooms? Round off your answer to two decimal places.
![Alt text](<Screenshot 2023-10-21 044919.png>)

3. What is the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet? Round off your answer to two decimal places.
![Alt text](<Screenshot 2023-10-21 045033.png>)

4. What is the "view" rating for homes costing more than or equal to $350,000? Determine the run time for this query, and round off your answer to two decimal places.
![Alt text](<Screenshot 2023-10-21 045134.png>)

I cached my temporary table home_sales.

Checked if my temporary table was cached.

* Using the cached data, I ran the query that filtered out the view ratings with an average price of greater than or equal to $350,000. Determined the runtime and compared it to uncached runtime.
![Alt text](<Screenshot 2023-10-21 045351.png>)

Partitioned by the "date_built" field on the formatted parquet home sales data.

Created a temporary table for the parquet data.

* Ran the query that filtered out the view ratings with an average price of greater than or equal to $350,000. Determined the runtime and compared it to uncached runtime.

Uncached the home_sales temporary table.

Verified that the home_sales temporary table is uncached using PySpark.

## Runtime

1. Uncache Runtime: 1.368062973022461 seconds
2. Cached Runtime: 0.4902327060699463 seconds 
3. Runtime with the parquet DataFrame: 0.9032614231109619 seconds 


## Conclusion

Based on the time table, it is evident that executing a query on the cached version of the table was the most efficient option.
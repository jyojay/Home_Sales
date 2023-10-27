# Home_Sales
**Big Data - Spark SQL challenge**
In this challenge, I have used SparkSQL to determine key metrics about home sales data. Then I have used Spark to create temporary views, partition the data, cache and uncache a temporary table, and verified that the table has been uncached.
Note: Google Colab has been used for this challenge

## Repository Folders and Contents
- Resources:
  - Home_Sales.ipynb  --> Google colab notebook

### Tools/Libraries Imported:
- SparkSession from pyspark.sql
- time
- SparkFiles from pyspark

### Finding the average price for a four-bedroom house sold for each year rounded off to two decimal places.
#### Query run
![image](https://github.com/jyojay/Home_Sales/assets/132628129/aae2e60a-712b-49c6-9911-4453fa80d6c0)

#### Result Sorted on ascending order of year
![image](https://github.com/jyojay/Home_Sales/assets/132628129/b9feb126-1bff-4e64-980d-11c7dbb13b78)

### Finding the average price of a home for each year it was built that has three bedrooms and three bathrooms rounded off two decimal places.
#### Query run
![image](https://github.com/jyojay/Home_Sales/assets/132628129/f7f24513-fed0-4ebf-8db7-267afd1f8446)

#### Result Sorted on ascending order of year
![image](https://github.com/jyojay/Home_Sales/assets/132628129/affddcb5-ee05-465c-a35b-8e423b67e588)

### Finding the average price of a home for each year that has three bedrooms, three bathrooms, two floors, and is greater than or equal to 2,000 square feet. round off to two decimal places. Note: sqft_living has been used since all of sqft_lot are > 2,000
#### Query run
![image](https://github.com/jyojay/Home_Sales/assets/132628129/7fdcdde1-e6ed-4f48-8f19-0dcc9fa5220d)

#### Result Sorted on ascending order of year
![image](https://github.com/jyojay/Home_Sales/assets/132628129/37a1b75c-fda4-46ed-ba6f-06c49e7b393b)

### Finding the "view" rating for homes costing more than or equal to $350,000. Determine the run time for this query, and rounding off our answer to two decimal places.
#### Query run
![image](https://github.com/jyojay/Home_Sales/assets/132628129/296c2512-d425-41c2-9054-37ec30b021bc)

#### Result
![image](https://github.com/jyojay/Home_Sales/assets/132628129/11a082e7-016b-4c18-8683-38d70c33f8d5)

### Caching temporary table home_sales
### Checking if your temporary table is cached.
![image](https://github.com/jyojay/Home_Sales/assets/132628129/fb86a3f0-34c8-46da-9d67-2ea4f5d18c12)

### Using the cached data, running the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determining the runtime and comparing it to uncached runtime.
#### Query run
![image](https://github.com/jyojay/Home_Sales/assets/132628129/3ab2c960-df08-4e2c-8cb3-497d839c9417)

#### Result
-  <font color='#fa8072'>Uncached Runtime was 1.42 seconds vs Cached runtime of 0.63 seconds. **Cached runtime was shorter than the uncached runtime of the query** </br>
![image](https://github.com/jyojay/Home_Sales/assets/132628129/f70fb154-959c-4b34-989b-1ce7becdebeb)

### Partitioning by the "date_built" field on the formatted parquet home sales data.
#### Query run
![image](https://github.com/jyojay/Home_Sales/assets/132628129/1fa4b4b4-7513-4e01-80b8-39f91d3b4f66)

### Creating a temporary table for the parquet data.
##### Query run
![image](https://github.com/jyojay/Home_Sales/assets/132628129/e5b5b170-2e25-4c86-a795-86177a6aa859)

### Running the query that filters out the view ratings with an average price of greater than or equal to $350,000. Determining the runtime and comparing it to uncached runtime.
#### Query run
![image](https://github.com/jyojay/Home_Sales/assets/132628129/cfcff0aa-2d9a-4cc6-a6f9-526ae16b493f)

#### Result
-  <font color='#fa8072'> Parquet Runtime was 0.96 seconds vs uncached runtime of 1.42 seconds. Parquet runtime was lower than uncached runtime. </br>
![image](https://github.com/jyojay/Home_Sales/assets/132628129/c2c3027a-c8b7-4510-8575-749f07f978f9)

### Uncaching the home_sales temporary table.
##### Query run
![image](https://github.com/jyojay/Home_Sales/assets/132628129/7bc68bef-0777-4408-b55a-b1355e580d38)

### Verifying that the home_sales temporary table is uncached using PySpark.
##### Query run
![image](https://github.com/jyojay/Home_Sales/assets/132628129/fe880d7c-ea89-43de-a166-1ccc24f13552)



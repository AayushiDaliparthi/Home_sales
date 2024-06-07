$$
Home Sales Data Analysis
$$
This project leverages SparkSQL to derive insights from home sales data. We performed data ingestion, transformation, querying, and explored optimizations like caching and partitioning to enhance query performance.

**Key Objectives**
Data Ingestion and Transformation

Read home sales data into a Spark DataFrame.
Create temporary views for SQL-based querying.
SQL Queries Executed

Average price for four-bedroom houses by year.
Average price of homes with three bedrooms and three bathrooms by the year built.
Average price of homes with three bedrooms, three bathrooms, two floors, and at least 2,000 square feet by the year built.
Average price of homes by "view" rating where the average price is at least $350,000.
Optimization Techniques

Caching: Store data in memory to reduce query execution time.
Partitioning: Organize data by specific fields for efficient querying.
Detailed Analysis and Outcomes
SQL Query Insights

Four-Bedroom Houses: Average Prices by Year

Extracted the yearly average prices for homes with four bedrooms, providing trends in housing costs over time.
Homes with Three Bedrooms and Bathrooms: Average Prices by Construction Year

Analyzed average prices based on the construction year for homes with three bedrooms and three bathrooms, offering insights into value retention and trends.
Detailed Criteria Homes: Average Prices by Construction Year

Focused on homes with specific features: three bedrooms, three bathrooms, two floors, and a minimum of 2,000 square feet. This query illuminated how specific criteria impact pricing over time.
View Rating: Average Prices for High-Value Homes

Investigated homes based on "view" rating and extracted average prices for homes with an average price of at least $350,000. This provided insights into how a good view impacts home prices.
Caching and Performance Optimization

Caching:

The home_sales DataFrame was cached, significantly reducing the runtime for subsequent queries. Caching stores the data in memory, decreasing access times and improving query performance by reducing the need to repeatedly read from the disk.
Comparison: The uncached query took longer compared to the cached one, highlighting the efficiency gained through caching.
Partitioning and Parquet Format:

The data was partitioned by the date_built field and stored in Parquet format. This method reduced the runtime for query execution by improving data retrieval speed and storage efficiency.
Partitioned Query: Running the same query on partitioned data further reduced the runtime compared to both cached and uncached queries, demonstrating the effectiveness of partitioning combined with Parquet’s columnar storage format.
Technical Implementation


**Conclusion**
Through this project, we demonstrated the power of SparkSQL in analyzing home sales data. Caching and partitioning significantly enhanced performance, even for relatively small datasets. For larger datasets, these optimizations would provide even greater improvements, enabling faster and more efficient data analysis. The approach highlights how modern data processing techniques can provide actionable insights quickly, reducing resource usage and improving query response times.

By applying these techniques, analysts and data scientists can streamline their workflows, reduce latency in data retrieval, and enhance the overall efficiency of their data processing pipelines.





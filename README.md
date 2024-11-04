# Home Sales Data Analysis with PySpark

## Overview
This project analyzes a home sales dataset using Apache Spark, focusing on various queries to derive insights about home prices based on different features. The dataset includes information such as home prices, the number of bedrooms, the number of bathrooms, square footage, view ratings, and the year homes were built.

## Technologies Used
- **Apache Spark**: Utilized for processing large datasets in a distributed manner.
- **Python**: The primary programming language for data manipulation and analysis.
- **PySpark**: The Python API for Spark, enabling Python developers to leverage the simplicity of Python alongside the power of Apache Spark.

## Steps Taken
1. **Data Preparation**: Loaded the home sales dataset into a Spark DataFrame to facilitate efficient data manipulation and analysis.

2. **Creating a Temporary View**: Established a temporary view of the home sales DataFrame, allowing SQL queries to be executed against the DataFrame.

3. **Average Price Analysis**: Conducted several queries to calculate the average price of homes based on various criteria, such as the number of bedrooms, bathrooms, and square footage, rounding the results to two decimal places.

4. **Query Optimization**: Implemented caching on the temporary view to enhance the performance of repeated queries, resulting in improved execution speed.

5. **Data Storage in Parquet Format**: Saved the processed DataFrame in Parquet format, which is optimized for efficient data storage and retrieval. Partitioned the data by specific fields to enhance performance during queries.

6. **Performance Comparison**: Compared the execution times of queries run on the cached DataFrame and the Parquet DataFrame, evaluating the consistency of performance improvements across different query types.

7. **Runtime Evaluation**: Measured the runtime for specific queries to assess the efficiency of caching versus the Parquet format.

## Key Insights
- **Caching**: The creation of a temporary view of the home sales DataFrame and the utilization of caching optimized the performance of repeated queries, generally improving execution speed across various analyses.

- **Parquet Format**: While the processed data was saved in Parquet format for efficient storage and retrieval, the performance benefits when querying the Parquet DataFrame were inconsistent compared to the cached DataFrame.

Overall, caching provided reliable speed improvements for many queries, while the performance of both caching and Parquet was unpredictable. In some cases, cached queries executed faster, while in others, the Parquet format was quicker. Both methods outperformed the temporary view, likely influenced by factors such as available RAM and the speed of the personal computer used for analysis.

### End Notes
This activity was completed with reference to past class activities and with the assistance of ChatGPT.

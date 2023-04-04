
# Pandas

Explain the purpose and basic functionality of the Pandas library. What are some common operations that can be performed on data using Pandas, and how do they contribute to data analysis and manipulation?

Pandas is a Python library used for data manupilation and analysis. 

Data Cleaning: Cleaning up data is an essential step in data analysis, and Pandas provides a range of functions to achieve this. For instance, one can remove missing data or duplicates, replace values or remove outliers, etc.

Data Manipulation: Pandas makes it easy to manipulate data by providing functions for merging, filtering, sorting, grouping, and pivoting data.

Data Aggregation: With Pandas, one can perform aggregations like sum, mean, count, min, and max, among others, on grouped data.

Data Visualization: Pandas integrates well with visualization libraries such as Matplotlib and Seaborn to create visualizations of data in the form of charts, graphs, and tables.

Time Series Analysis: Pandas provides powerful tools for working with time series data such as date ranges, frequency conversions, moving window statistics, and resampling

The wide functionality allows for ease of use, versatality and speed. 


What are the primary data structures in Pandas, and how do they differ in terms of use cases?

There are two primary data structures in Pandas, Series and DataFrame.

A Series is a one-dimensional array-like object that can hold any data type such as integers, floats, strings, etc. A DataFrame is a two-dimensional tabular data structure with rows and columns, similar to a spreadsheet or SQL table.

Describe the process of loading a dataset into a Pandas DataFrame. What are some common file formats that can be used, and which Pandas functions are utilized to read these formats?

import pandas as pd

CSV: pd.read_csv()
Excel: pd.read_excel()
SQL: pd.read_sql()
JSON: pd.read_json()
HTML: pd.read_html()

df = pd.read_csv('mydata.csv')


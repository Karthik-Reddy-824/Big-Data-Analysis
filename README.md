# Big-Data-Analysis
*COMPANY*:CODE TECH IT SOLUTIONS
*NAME*:DARGULA KARTHIK REDDY
*INTERN ID*:CT6WQWS
*DOMAIN*:DATA ANALYTICS
*DURATION*:6 WEEKS
*MENTOR*:NEELA SANTOSH

The project focuses on analyzing Netflix's dataset using Dask, an efficient parallel computing framework for handling large-scale data processing. The goal is to extract insights on content trends over time and genre distribution using optimized computation and visualization techniques.
The script performs an exploratory data analysis (EDA) on the Netflix dataset using Dask, which enables parallel computing for handling large datasets efficiently.
The analysis of the Netflix dataset aims to provide insights into the trends of content added over time and the distribution of genres. Due to the large size of the dataset, Dask is used for efficient data processing. Dask is a parallel computing library that allows handling large datasets without loading everything into memory at once, making it ideal for scalable data analysis.

Data Processing with Dask
To ensure scalability, the dataset is loaded using dask.dataframe.read_csv(), which allows for parallel processing without loading the entire dataset into memory. This is particularly beneficial for handling large datasets that exceed standard memory limits.

Once loaded, the date_added column is converted to datetime format, and the year of addition is extracted using dt.year. This transformation enables time-series analysis of Netflix’s content expansion.

Trend Analysis of Content Additions
The dataset is grouped by year to compute the total number of movies and TV shows added annually.
A line plot is generated using seaborn and matplotlib to visualize the yearly trend.
This visualization highlights Netflix’s growth trajectory, showcasing peak years of content additions.
Genre Distribution Analysis
Netflix's content spans multiple genres, which are stored as comma-separated values in the listed_in column. To analyze genre distribution:

The column is split into individual genres using str.split() and exploded to create multiple rows per title.
The dataset is processed using Dask’s parallel capabilities to count occurrences of each genre efficiently.
A bar chart visualizes the top 10 most common genres, providing insights into Netflix’s content strategy.
Key Benefits of Using Dask
Parallel Computing: Faster execution compared to traditional pandas processing.
Scalability: Handles large datasets efficiently without memory limitations.
Optimized Computation: Uses lazy evaluation to process only the necessary computations.


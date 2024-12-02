# EDA-with-Pandas-in-Jupyter-Notebook
This repository contains EDA performed on a dataset containing information regarding applications of various genres from the Apple App Store. 

# Exploratory Data Analysis on App Store Games Dataset

# Project Overview
This project involves a detailed EDA of the App Store Games dataset using Python's Pandas library along with visualization tools like Matplotlib. The dataset includes various features of mobile games, such as names, user ratings, release dates, and more. The analysis aims to clean, transform, and derive meaningful insights from the data.

# Objectives

Clean the dataset by handling missing and duplicate values.
Create new features for deeper analysis.
Generate visual insights to highlight trends and patterns in the data.
Prepare the data for further analysis by removing redundant or unnecessary columns.

# Tools and Libraries Used

Pandas: For data manipulation and cleaning.
NumPy: For numerical computations.
Matplotlib: For data visualization.
Warnings Module: To suppress warnings for better readability.

# Key Steps and Methods

1. Data Import and Exploration:

Imported the dataset using pd.read_excel().
Displayed the first few rows with .head() and checked its structure using .info() and .describe().

2. Handling Duplicates:

Identified and removed duplicate rows using .duplicated() and .drop_duplicates().

3. Managing Missing Values:

Checked missing values with .isna().sum().
Used strategies to fill missing values:
Median imputation: For skewed numerical columns (e.g., Average User Rating).
String replacements: For textual data (e.g., Subtitle and Description).
Column removal: Dropped columns with excessive missing values (e.g., Subtitle).

4. Feature Engineering:

Extracted Year from the Release Date column.
Created a Paid or Free column using a lambda function on Price per App (USD).
Added a Revenue column by multiplying User Rating Count with Price per App (USD).
Converted Size in Bytes to MB and renamed the column for clarity.
Created size buckets based on app size using a custom function.

5. Data Cleaning:

Renamed all columns to lowercase and replaced spaces with underscores for uniformity.
Dropped irrelevant columns like Icon URL, App URL, and others.

6. Visualization:

Visualized the distribution of missing values using a bar chart.
Plotted trends:
Number of games launched each year.
Annual revenue.
Highlighted top 10 games by rating count using a bar graph.

# Key Insights

1. Missing Data:

Managed missing values with meaningful imputations, ensuring no critical data loss.

2. Feature Trends:

Identified years with the highest number of game launches.
Analyzed revenue trends over time, highlighting peak years.

3. User Behavior:

Identified the top 10 most-rated games, reflecting user preferences.

4. Game Size Patterns:

Categorized games into size buckets, revealing that most games fall under specific size ranges.

# Problems Addressed

1. Handling Missing and Duplicate Data:
Ensured data integrity by addressing null and duplicate entries.

2. Feature Creation:
Enhanced the dataset with new columns like Year, Revenue, and Size Buckets.

3. Preparing Data for Analysis:
Removed redundant columns and standardized formats for efficient analysis.

# Future Work and recommendations
1. Use advanced visualization libraries (e.g., Seaborn) for deeper insights.
2. Incorporate machine learning models for predictive analysis based on user ratings and revenue.


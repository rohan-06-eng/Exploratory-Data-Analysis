# Flight Price Prediction - Exploratory Data Analysis (EDA)

## Project Overview

This project aims to perform **Exploratory Data Analysis (EDA)** on a dataset of flight prices. The objective is to identify key patterns, trends, and relationships between different features and flight prices. The dataset includes various flight attributes, which will help us understand the factors influencing the flight prices and prepare the dataset for further predictive modeling.

## Dataset Information

The dataset contains information about flights, including details on flight timings, source and destination, airline, route, stops, and the ticket price. The primary goal is to predict the **Price** of a flight based on other attributes.

## Dataset Overview

The dataset contains **10,683 rows** and **16 columns**. Below are the details of each column:

### Dataset Columns:

The dataset contains the following columns:

1. **Airline**: The airline operating the flight (e.g., Air India, IndiGo, etc.).
2. **Date_of_Journey**: The date of flight departure (in DD/MM/YYYY format).
3. **Source**: The city/airport of departure.
4. **Destination**: The city/airport of arrival.
5. **Route**: The route taken by the flight (including any stopovers).
6. **Dep_Time**: The time of flight departure.
7. **Arrival_Time**: The time of flight arrival.
8. **Duration**: The total duration of the flight (in hours and minutes).
9. **Total_Stops**: The total number of stops during the flight (0 for direct flights, 1 or more for flights with stopovers).
10. **Additional_Info**: Other information such as whether the flight is a non-stop or involves additional details like baggage policy.
11. **Price**: The price of the flight ticket (target variable).

## EDA Objectives

The primary goal of this EDA is to explore the data and extract useful insights that can help in the prediction of flight prices. Key objectives include:

1. **Data Inspection**: Check for missing values and data types.
2. **Statistical Summary**: Summarize the data with descriptive statistics.
3. **Correlation Analysis**: Examine the relationships between numerical features and the target variable (Price).
4. **Feature Engineering**: Create new features or transform existing features to improve the prediction.
5. **Outlier Detection**: Identify and handle outliers in the dataset.
6. **Visualization**: Visualize the distribution and relationships of various features to better understand the data.

## EDA Steps

### 1. **Data Inspection and Cleaning**
   - Load the dataset and inspect the data.
   - Check for missing values and handle them (e.g., imputation or removal).
   - Convert data types where necessary (e.g., `Date_of_Journey` to datetime format).
   - Handle duplicates or irrelevant information.

### 2. **Statistical Summary**
   - Generate summary statistics for numerical columns (`Price`, `Duration`, `Total_Stops`).
   - Examine the distribution of categorical features (`Airline`, `Source`, `Destination`, etc.).

### 3. **Data Visualization**
   - **Price Distribution**: Visualize the distribution of flight prices using histograms and box plots.
   - **Price vs. Features**: Explore how flight prices vary based on other features, such as `Airline`, `Source`, `Destination`, `Total_Stops`, and `Duration`.
   - **Route Analysis**: Investigate how different routes and stopovers impact flight prices.
   - **Duration vs. Price**: Create scatter plots to examine how flight duration affects the price.

### 4. **Feature Engineering**
   - **Date_of_Journey**: Extract the day of the week, month, and year from the `Date_of_Journey` column.
   - **Dep_Time and Arrival_Time**: Extract time-related features such as departure time, arrival time, and duration.
   - **Total_Stops**: Convert the `Total_Stops` to categorical values (e.g., "Non-stop", "1 Stop", "2+ Stops").
   - **Additional_Info**: Explore if any additional information can be useful for the model.

### 5. **Outlier Detection**
   - Use box plots to detect outliers in numerical columns like `Price`, `Duration`, and `Total_Stops`.
   - Analyze the effect of outliers on model performance and decide whether to remove or transform them.

### 6. **Correlation Analysis**
   - Use heatmaps to analyze the correlation between numerical features and the target variable (`Price`).
   - Identify features that are highly correlated with the target variable, which can be useful for modeling.

### 7. **Missing Data Analysis**
   - Visualize missing data using heatmaps.
   - Determine the method for handling missing data (e.g., imputation with the mean, median, or mode).

## Tools & Libraries

This project utilizes the following Python libraries:

- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical computations.
- **Matplotlib**: For data visualization (e.g., histograms, box plots, scatter plots).
- **Seaborn**: For advanced data visualizations (e.g., heatmaps, count plots).
- **Scikit-learn**: For preprocessing, feature engineering, and model evaluation.

### Installation

To install the required libraries, run the following command:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn

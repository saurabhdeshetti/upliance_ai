# Assignment for Data Analytics Intern - upliance_ai

## Overview

This repository contains the code and findings from the upliance.ai assignment for the Data Analytics Intern position. The project involves analyzing user data, cooking sessions, and order details to derive insights and recommendations for improving service efficiency and user engagement.

## Files Included

- **UserDetails.csv**: Contains user demographic information.
- **CookingSessions.csv**: Records details of cooking sessions conducted by users.
- **OrderDetails.csv**: Contains information about user orders, including meal types and ratings.
- **upliance_ai_Assignment_for_Data_Analytics_Intern.pdf**: Contains actual code and visualisations of the project.
- **upliance_ai_Assignment_for_Data_Analytics_Intern.ipynb**: Contains actual code and visualisations of the project.

## Requirements

To run the analysis, ensure you have the following libraries installed:

```bash
pip install numpy pandas matplotlib seaborn
```

## Data Processing Steps

1. **Reading CSV Files**:
   - Import necessary libraries.
   - Load the CSV files using Pandas.

   ```python
   import numpy as np
   import pandas as pd
   import matplotlib.pyplot as plt
   import seaborn as sns

   user_details = pd.read_csv('UserDetails.csv')
   cooking_sessions = pd.read_csv('CookingSessions.csv')
   order_details = pd.read_csv('OrderDetails.csv')
   ```

2. **Data Cleaning**:
   - Handle missing values in the `Rating` column by filling them with the average rating.
   - Remove duplicates from all datasets.
   - Convert date columns to datetime format.

3. **Data Merging**:
   - Merge all three datasets for comprehensive exploratory data analysis (EDA).

   ```python
   df = user_details.merge(cooking_sessions, on='User ID').merge(order_details, on='Session ID')
   ```

## Exploratory Data Analysis (EDA)

### Insights & Recommendations

1. **Popular Dishes**:
   - **Insights**: Spaghetti and Grilled Chicken are the most ordered dishes.
   - **Recommendations**: Highlight these dishes in marketing campaigns.

2. **User Demographics**:
   - **Insights**: The highest number of users are aged 28, 35, and 42.
   - **Recommendations**: Focus marketing efforts on these age groups.

3. **Order Trends Over Time**:
   - **Insights**: Limited data shows only two orders per day.
   - **Recommendations**: More data collection is needed for meaningful insights.

4. **Cooking Session Duration**:
   - **Insights**: Longer cooking sessions correlate with certain days.
   - **Recommendations**: Investigate factors contributing to longer sessions for future replication.

5. **Order Amount by Age**:
   - **Insights**: Users aged 25 and 38 spent the most.
   - **Recommendations**: Develop campaigns targeting these age groups to encourage repeat purchases.

## Visualizations

The analysis includes various visualizations such as bar plots and pie charts to represent data insights effectively. Key visualizations include:

- Top 10 Popular Dishes
- User Demographic Distribution
- Order Amount by Age
- Dish Distribution Pie Chart

## Conclusion

This project provides valuable insights into user behavior and preferences within the upliance.ai platform. The recommendations derived from the analysis aim to enhance user engagement, improve service offerings, and drive sales growth.

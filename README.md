# Bike Demand Prediction using Multiple Linear Regression

## Overview
This project aims to predict the demand for shared bikes using a multiple linear regression model. The prediction will help BoomBikes, a US-based bike-sharing company, understand the factors influencing bike demand and devise effective strategies to increase their revenue in a post-COVID-19 world.

## Business Problem
BoomBikes experienced a significant dip in revenues due to the COVID-19 pandemic. To prepare for a rebound in demand, the company wants to:
- Identify significant factors that influence bike demand.
- Build a predictive model to forecast bike demand based on these factors.

## Dataset
The dataset contains daily records of bike rentals, weather conditions, and seasonal information. Key variables include:
- `cnt`: Total bike demand (target variable).
- `season`: Season of the year.
- `weathersit`: Weather situation.
- `temp`: Normalized temperature.
- `yr`: Year (2018 or 2019).

The dataset has been preprocessed to convert numerical categorical values (e.g., `season`, `weathersit`) into meaningful labels.

## Objectives
1. Identify the variables significantly influencing bike demand.
2. Build a robust regression model for prediction.
3. Evaluate the model's performance using metrics such as R-squared and Mean Squared Error.

## Technologies Used
- **Python**: Programming language for data processing and analysis.
- **Libraries**:
  - `pandas`: Data manipulation and preprocessing.
  - `numpy`: Numerical computations.
  - `matplotlib` and `seaborn`: Data visualization.
  - `scikit-learn`: Model building and evaluation.
  - `statsmodels`: Detailed statistical summaries.

## Approach
1. **Data Preprocessing**:
   - Converted numeric categorical variables (`season`, `weathersit`) into string labels.
   - Created dummy variables for categorical features.
   - Split data into training and testing sets.

2. **Exploratory Data Analysis**:
   - Visualized relationships between variables and the target (`cnt`).
   - Identified correlations using a heatmap.

3. **Model Building**:
   - Built a linear regression model using `LinearRegression` from `scikit-learn`.
   - Evaluated feature significance using Variance Inflation Factor (VIF).

4. **Model Evaluation**:
   - Computed R-squared and Mean Squared Error.
   - Performed residual analysis to validate linear regression assumptions.

## Results
- The model achieved a high R-squared value on both training and test datasets, indicating good predictive performance.
- The top three significant features influencing bike demand were:
  1. Temperature (`temp`)
  2. Year (`yr`)
  3. Weather situation (`weathersit`)

## Conclusions
- Favorable weather conditions and higher temperatures significantly increase bike demand.
- Bike-sharing demand has grown year-on-year, highlighting its rising popularity.
- Effective strategies, such as offering promotions during unfavorable weather, can help stabilize demand.

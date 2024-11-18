# Retail Sales Forecasting and Analysis

## Project Overview
This project involves analyzing weekly sales data for various retail outlets to uncover key insights and use predictive modeling techniques to forecast future sales. The project focuses on answering several critical business questions and building a model to predict sales for the next 12 weeks based on historical data. It includes **statistical analysis**, **exploratory data analysis (EDA)**, and **predictive modeling** to support data-driven decision-making.

## Objectives

1. **Exploratory Data Analysis (EDA) and Statistical Analysis**:
   - Analyze weekly sales data to identify patterns and relationships with external factors.
   - Explore the effect of **unemployment rate**, **seasonality**, **temperature**, and **consumer price index (CPI)** on weekly sales.
   - Identify top-performing and worst-performing stores.
   - Handle missing data, detect outliers, and apply statistical techniques for deeper insights.

2. **Predictive Modeling**:
   - Build a forecasting model to predict the **weekly sales** for each store for the next 12 weeks.
   - Use time series analysis and machine learning techniques to make accurate predictions.

## Data Overview
The dataset includes weekly sales data for multiple retail outlets along with additional features such as:
- **Sales data**: Weekly sales numbers for each outlet.
- **Unemployment rate**: Weekly unemployment data by region.
- **Temperature**: Weekly average temperature in the regions of operation.
- **Consumer Price Index (CPI)**: Weekly CPI data indicating inflation or deflation trends.
- **Outlet identifiers**: Information about each store's region and location.

## Steps and Methodology

### 1. **Data Preprocessing**
   - **Missing Value Handling**: Identified and handled missing values using imputation techniques (mean/median imputation or forward-fill).
   - **Outlier Detection**: Used statistical methods (Z-score, IQR) to detect and remove outliers.
   - **Data Normalization**: Scaled numerical data where necessary to ensure consistency and improve model performance.

### 2. **Exploratory Data Analysis (EDA)**
   - **Correlation Analysis**: Checked for relationships between weekly sales and external factors such as unemployment rate, temperature, and CPI.
   - **Seasonality Check**: Used **time series decomposition** to identify seasonal trends in weekly sales.
   - **Store Performance Analysis**: Analyzed sales across stores to determine the top and worst performers.
   - **Visualization**: Plotted time series graphs, heatmaps, and distribution plots to better understand trends, outliers, and correlations.

### Key Insights from EDA:
1. **Effect of Unemployment Rate**:
   - Unemployment rate has a **negative impact** on sales, with certain stores located in high-unemployment regions seeing the **greatest decline**.
   - **Stores in urban areas** with a higher unemployment rate suffer the most.

2. **Seasonality in Sales**:
   - Sales show a **seasonal trend** with significant peaks during **holiday seasons** (e.g., end-of-year holidays, summer).
   - **Promotions, festivals, and holidays** are likely contributing to these peaks.

3. **Temperature and Sales**:
   - **Temperature** influences sales, especially for **seasonal items** (e.g., apparel, beverages). Higher sales are observed during **warmer months**.

4. **Impact of Consumer Price Index (CPI)**:
   - A higher **CPI (inflation)** correlates with **lower sales** in certain stores, particularly for non-essential goods.

5. **Store Performance**:
   - The **top-performing stores** are typically located in **high-traffic urban areas** with a diverse customer base.
   - The **worst-performing stores** often correlate with regions facing **economic downturns or high unemployment rates**.

6. **Store Sales Comparison**:
   - A **significant performance gap** exists between the best and worst-performing stores, with a **3x difference** in average weekly sales.

### 3. **Predictive Modeling**

#### Forecasting Sales for the Next 12 Weeks:
- **Time Series Modeling**: Applied **ARIMA** and **Facebook Prophet** models to predict weekly sales.
- **Machine Learning Models**: Used models such as **Random Forests** and **XGBoost** to predict future sales based on historical data and external features.
- **Hyperparameter Tuning**: Optimized models using **GridSearchCV** for better accuracy.
  
### 4. **Model Evaluation**
   - **Metrics**: Evaluated model performance using **Mean Absolute Error (MAE)**, **Root Mean Squared Error (RMSE)**, and **Mean Absolute Percentage Error (MAPE)**.
   - The time series models (ARIMA and Prophet) outperformed the machine learning models in terms of accuracy for short-term forecasting.

### 5. **Future Sales Prediction**
   - Forecasted weekly sales for each store for the next 12 weeks with 95% confidence intervals for uncertainty in predictions.
   - Generated actionable insights on which stores are expected to perform better and which may need intervention or support.

## Installation

### Prerequisites
- Python 3.x
- Required Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `statsmodels`
  - `scikit-learn`
  - `fbprophet` (for forecasting)
  
### Installing Dependencies

To install the required libraries, run the following:

```bash
pip install -r requirements.txt

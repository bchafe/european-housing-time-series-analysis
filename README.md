# Time Series Data Analysis - European Housing Price Index



## Overview
This project covers the use of time series analysis techniques to identify trends and extract insights from European housing price index data. The goal of this project was to explore how housing prices evolve over time across different countries, and apply appropriate analytical models given the constraints of limited data.

![Price index for lowest 10 countries across sample period](https://raw.githubusercontent.com/bchafe/european-housing-time-series-analysis/refs/heads/main/images/europe-lowest-prices.png)

## Objectives
- Analyze housing price trends across European countries
- Apply time series analysis techniques to extract meaningful patterns
- Create reusable code to apply visualizations and forecasting to any country in the dataset
- Evaluate model suitability under limited data conditions
- Generate insights relevant to macroeconomic and financial analysis

## Dataset
- Source: [European Housing Price Index 2022-2025](https://www.kaggle.com/datasets/ibrahimshahrukh/european-housing-price-index-dataset/) on Kaggle
- Sample Frequency: Quarterly
- Scope: European countries
- Sample Size: ~12 observations per country


## Tools and Technologies
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- SciPy, statsmodels
- Scikit-learn

## Methodology
### 1. Data Preparation
- Filtered dataset to remove aggregate country groups
- Removed records for countries with no recorded price index data
- Created a numeric ID for each distinct quarter to assist in visualization
### 2. Exploratory Data Analysis
- Visualized housing prices over time for countries with highest/lowest price index values
- Compared growth patterns across countries
- Identified variability and potential outliers
### 3. Trend Estimation
- Applied Linear Regression and Rolling Average to visualize long-term trend for Finland
- Selected these methods due to limited number of observations (~12 per country)
- Avoided overfitting associated with more complex models
### 4. Forecasting
- Used Double Exponential Smoothing to predict future price index values for Finland
- Performed cross-validation to select appropriate parameters for forecasting model
- Compared results to actual data to acknowledge limitations in forecasting accuracy
### 5. Correlation Mapping
- Considered limitations in forecasting based solely on previous price index values 
- Visualized correlations between price index and other variables in dataset
- Uncovered meaningful insights about possible predictors of housing prices

## Key Visualizations
### Linear Trend vs Actual Housing Price Index (Finland)
![Visualizing long-term trend for Finland using Linear Regression](https://raw.githubusercontent.com/bchafe/european-housing-time-series-analysis/refs/heads/main/images/finland_linear_regression.png)

### Forecasting Future Price Index (Finland)
![Forecasting future price index values for Finland](https://raw.githubusercontent.com/bchafe/european-housing-time-series-analysis/refs/heads/main/images/finland_forecast.png)

### Correlation with Price Index
![Visualizing correlation with price index](https://raw.githubusercontent.com/bchafe/european-housing-time-series-analysis/refs/heads/main/images/correlation-heatmap.png)

## Results and Insights
- Growth rates in housing prices vary significantly across European countries
- Most countries see prices trending upwards, some see prices trending downwards
- Limited data for each country restricts detection for seasonal patterns
- EU and Eurozone members have generally shown **lower price index values** than non-members
- Türkiye shows the **most extreme increase** in housing prices across Europe since 2015
- Finland is the only European country to maintain housing prices **lower than in 2015**
- Forecasting suggests that Finland's housing prices **will continue to fall** in the next few quarters

## Limitations
- Small sample size (~12 data points per country)
- Limited ability to apply advanced time series models (STL decomposition, machine learning)
- Forecasting accuracy constrained by data availability

## Future Improvements
- Incorporate additional historical data to improve model reliability
- Apply more advanced time series forecasting models (Triple Exponential Smoothing, Gradient Boosted Regression) with larger datasets
- Expand analysis to incorporate external economic indicators (interest rates, inflation)

## Key Takeaways
This project emphasizes the importance of selecting appropriate analytical techniques based on data constraints. Rather than applying overly complex models, the focus was on uncovering interpretable and reliable insights from limited real-world data.

## How to Run
### Method 1: Google Colab (Recommended)
1. [Open this notebook](https://colab.research.google.com/drive/18728gyZcs7p4vDUWDDNaZSOrQjpkMd8j?usp=sharing) in Google Colab
2. Run each code cell in order, or click 'Run All' to automatically run all cells
### Method 2: Run the notebook locally
1. Clone this repository
2. Open a shell in the cloned directory and install dependencies:
```
python -m venv venv

source venv/bin/activate    # Mac/Linux
venv\Scripts\activate       # Windows

pip install -r requirements.txt
```
3. Open the notebook in JupyterLab or VS Code
4. Run each code cell in order, or click 'Run All' to automatically run all cells



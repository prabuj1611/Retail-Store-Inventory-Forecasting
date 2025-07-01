
🛒 **Retail Sales Forecasting with Prophet**

- This project focuses on analyzing and forecasting daily item-level retail sales using time series techniques, primarily leveraging Facebook Prophet. 

- The dataset contains over 900,000 records of sales for 50 items across 10 stores from 2013 to 2017.

📌 **Objective**

- Perform exploratory data analysis (EDA) to understand sales patterns.

- Visualize growth trends and seasonality at multiple granularities (daily, monthly, yearly).

- Forecast future sales using Prophet, incorporating holidays and external regressors.

- Evaluate model performance using SMAPE (Symmetric Mean Absolute Percentage Error).

📁 **Dataset**

**Source:** Kaggle Store Item Demand Forecasting Challenge

**Rows:** ~913,000

**Columns:** date, store, item, sales

🔧 **Libraries Used**

pandas, numpy — Data manipulation

matplotlib, seaborn — Visualization

fbprophet — Time series forecasting

scikit-learn — (Optional) model evaluation metrics

📊 **Key Steps**

1. Data Preparation
   
Added derived features: year, month, month_year

Checked for missing values (none found)

Created aggregation views for item/store-level summaries

2. Exploratory Data Analysis (EDA)
   
Visualized sales distributions and trends over time

Analyzed seasonality and volatility in monthly/yearly growth

Generated store-wise and item-wise sales heatmaps and line plots

3. Time Series Forecasting with Prophet
   
Built forecasting model for a specific item-store combination (e.g., Store 1, Item 1)

Modeled trend, seasonality, and holiday effects

Added NFL-related regressors to capture special day impacts

Performed rolling predictions for automation

4. Holiday Effects & Regressors
   
Included key dates like Super Bowl and summer sales

Engineered custom features like nfl_sunday for enhanced seasonality detection

5. Model Evaluation
   
Back-transformed predictions using expm1

Merged predicted and actual data

Calculated SMAPE to evaluate performance (≈ 41%)

📈 **Results**

Clear upward sales trend with seasonal peaks (notably in July and during holidays)

Daily and yearly seasonality captured accurately by Prophet

Sales showed holiday effects, especially for specific store-item combinations

Forecasting performance was reasonably accurate with potential for further refinement

🧪 **Next Steps**

Tune hyperparameters for each store-item combination

Integrate external datasets like weather or economic indicators

Deploy a forecasting pipeline to support inventory planning



---


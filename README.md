🚲 Bike Rental Demand Prediction & Business Analysis
📌 Project Overview

This project analyzes bike rental demand and develops a predictive model to identify the key factors influencing the number of bike rentals.

The objective is to use historical bike rental data to:

Understand demand patterns
Identify the key drivers of bike rental demand
Build a predictive model using KNIME
Evaluate the model on unseen test data
Translate analytical findings into actionable business recommendations
🎯 Business Problem

A bike rental company needs to ensure that sufficient bikes are available when and where demand is high.

However, demand varies based on factors such as:

Time of day
Temperature
Weather conditions
Day of the week
Season
Year
Humidity
Windspeed

The business question is:

Can historical data be used to predict bike rental demand and improve fleet and operational planning?

🛠️ Tools & Techniques

Tool:

KNIME Machine Learning Analytics Platform

Techniques:

Exploratory Data Analysis
GroupBy Analysis
Aggregation
Pivot Analysis
Scatter Plot Analysis
Regression Tree
Train-Test Split
Predictive Modeling
Model Evaluation
Business Interpretation
📊 Dataset

The dataset contains historical bike rental information along with environmental and calendar-related variables.

Target Variable

cnt — Total number of bike rentals.

Key Variables Used
hr — Hour
temp — Temperature
hum — Humidity
windspeed — Windspeed
season — Season
weekday — Day of week
workingday — Working day indicator
weathersit — Weather situation
year — Year

The following columns were excluded from the predictive model:

instant
dteday
casual
registered
🔬 Analytical Approach
1. Exploratory Data Analysis

Different variables were analyzed against bike rental demand to understand their relationship with cnt.

Key analyses included:

Average rentals by hour
Working day vs non-working day demand
Weather vs rental demand
Temperature vs rental demand
Humidity vs rental demand
Windspeed vs rental demand
2. Predictive Modeling

A 70:30 train-test split was used.

70% of the data → Model training
30% of the data → Model testing

A Regression Tree was developed to predict cnt.

3. Model Evaluation

The trained model was applied to the 30% unseen test dataset.

Model performance:

Metric	Result
R²	0.875 / 87.5%
RMSE	63.97 bikes

The model explains approximately 87.5% of the variation in bike rental demand on the unseen test data.

🔎 Key Findings
1. Hour is the strongest predictor

hr was the first major splitting variable in the Regression Tree.

The analysis also showed that 4 PM–6 PM had particularly high average bike rental demand.

2. Temperature is a major demand driver

temp appeared as the next major splitting variable.

The analysis showed a generally positive relationship between temperature and bike rental demand.

3. Year influences demand

year appeared prominently in the Regression Tree, indicating a longer-term change in demand patterns.

4. Weekday affects demand

Rental demand varies across different days of the week, making weekday-specific planning useful.

5. Season influences demand

Seasonal conditions contribute to differences in rental demand.

6. Weather has a significant business impact

Better weather conditions were associated with higher average bike rental demand.

Weather situation 1 showed the highest average demand, while the poorest weather condition showed the lowest.

7. Humidity negatively affects demand

The analysis indicated that higher humidity was generally associated with lower bike rental demand.

8. Windspeed showed limited clear impact

No strong or consistent relationship between windspeed and rental demand was observed in the exploratory analysis.

💡 Business Recommendations
🚲 1. Optimize fleet availability by hour

Since time of day is the strongest predictor, fleet availability should be optimized around peak demand periods.

Particular attention should be given to the 4 PM–6 PM period.

🌡️ 2. Incorporate temperature into demand planning

Temperature forecasts can be used to anticipate changes in demand and adjust bike availability accordingly.

📅 3. Use weekday-specific planning

Different days can have different demand patterns.

Fleet allocation and operational planning should therefore consider the expected demand for each weekday.

🌦️ 4. Use weather-based planning

Weather forecasts can help the company anticipate demand increases or decreases and adjust fleet availability accordingly.

🍂 5. Incorporate seasonal patterns

Seasonality should be considered when planning fleet capacity, maintenance schedules and operational resources.

📈 6. Monitor long-term demand trends

The influence of year suggests that demand patterns change over time.

The company should regularly review historical trends to support future capacity planning.

📌 Business Value

The analysis demonstrates how predictive analytics can support practical business decisions.

The model and analysis can help a bike rental company:

Improve fleet utilization
Prepare for peak-demand periods
Reduce idle bike capacity
Improve operational planning
Incorporate weather conditions into demand planning
Support future fleet expansion decisions
🧠 Key Learning

This project demonstrates the complete analytics journey:

Business Problem → Data Analysis → Predictive Modeling → Model Evaluation → Business Recommendations

The project also highlights the importance of moving beyond model accuracy and translating analytical results into actionable business decisions.

📁 Project Structure
bike-rental-demand-analysis/
│
├── README.md
│
├── data/
│   └── bike_sharing.csv
│
├── knime/
│   └── Bike_Rental_Regression.knwf
│
├── screenshots/
│   ├── regression_tree.png
│   ├── model_performance.png
│   └── demand_by_hour.png
│
└── analysis/
    └── Business_Analysis.pdf
👤 Author

Sitesh Anand

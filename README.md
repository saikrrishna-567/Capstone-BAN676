**Enhanced EV Charging Optimization Framework**

This repository contains a comprehensive framework for optimizing energy allocation at EV charging stations over a 24-hour horizon. The framework uses machine learning models, time series forecasting, and optimization algorithms to maximize revenue, promote renewable energy usage, and ensure grid stability.

**Features**

* Data Preprocessing: Handles missing values, feature engineering, and lag feature creation for temporal dependencies.
* Forecasting Models: ARIMA and SARIMA models for forecasting solar and wind energy production.
* Predictive Modeling: Machine learning models (Random Forest, Gradient Boosting, Linear Regression) for predicting EV charging demand.
* Optimization: Combines global optimization (differential evolution) and local optimization (SLSQP) to allocate energy for maximum revenue while adhering to constraints.
* Visualization: Graphs for unmet demand, renewable energy usage, and grid stability before and after optimization.
* Environmental and Financial Impact Analysis: Quantifies changes in renewable energy usage and revenue after optimization.

**Workflow**

**1. Data Preparation**
* Cleans and preprocesses data from the input CSV file.
* Creates lag features for time-series analysis.
  
**2. Forecasting**

**ARIMA and SARIMA models predict:**

* Solar energy production.
* Wind energy production.
* Battery storage availability.
* Forecasts electricity prices using machine learning models.
  
**3. Predictive Modeling**

* Machine learning models (Random Forest, Gradient Boosting, Linear Regression) predict EV charging demand.
* The best model is selected based on the lowest Mean Squared Error (MSE).
  
**4. Optimization**
**Objective**

Maximize revenue while minimizing unmet demand and promoting renewable energy use.

**Constraints**

* Supply-demand balance.
* Demand constraints for each hour.
* Grid stability thresholds.
* Unmet demand limitations.

**Optimization is performed in two stages:**
1. Global Optimization: Uses differential evolution to find an approximate solution.
2. Local Optimization: Refines the solution using SLSQP with additional constraints.


**5. Visualization**

**Generates plots for:**
* Unmet demand before and after optimization.
* Renewable energy usage before and after optimization.
* Battery usage after optimization.
* Grid stability before and after optimization.

**Results**
* Optimized Energy Allocation: Energy allocation for each hour of the next 24 hours.
* Revenue Impact: Comparison of total revenue before and after optimization.
* Environmental Impact: Analysis of renewable energy usage before and after optimization.
* Grid Stability: Ensures grid stability remains above the acceptable threshold.

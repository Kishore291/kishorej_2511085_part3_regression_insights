# PART-3
## Task 1: Understand the Dataset

An initial audit of the `business_regression_data.xlsx` dataset was conducted to classify the variables and prepare the data for regression modeling.

### Variable Classification

* **Dependent Variable (Target):** * `monthly_sales`: The primary metric the business seeks to predict and optimize.
* **Potential Independent Variables (Predictors):** * `marketing_spend`, `footfall`, `avg_discount_pct`, `staff_count`, `inventory_availability_pct`, `competitor_distance_km`, `holiday_flag`, `customer_rating`.
* **Numerical Variables (Ready for modeling):** * `marketing_spend`, `footfall`, `avg_discount_pct`, `staff_count`, `inventory_availability_pct`, `competitor_distance_km`, `holiday_flag` (binary integer), `customer_rating`.
* **Categorical Variables (Require dummy transformation):** * `region` (East, North, South, West)
  * `store_type` (Residential, High Street, Airport, Mall)

### Data Quality & Transformation Needs
* **Missing Values:** Blank entries were identified in the `customer_rating` and `inventory_availability_pct` columns. These must be addressed (via imputation or row deletion) before running the regression, as analytical models cannot process null values.
* **Feature Engineering:** The categorical variables (`region`, `store_type`) must be transformed into binary "dummy variables" (0 or 1) before they can be included in a multiple regression model.

### Variables Excluded from Regression
* `store_id`: A unique categorical identifier offering no mathematical predictive value across the broader dataset.
* `month`: Date strings require specialized time-series forecasting models and are incompatible with standard linear regression. Seasonal variance is instead captured by the `holiday_flag`.
* `monthly_profit`: Excluded as a predictor to prevent data leakage, as the direct business objective is to model top-line sales.

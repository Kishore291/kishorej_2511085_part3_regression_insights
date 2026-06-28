# Model Comparison Analysis

This document compares the simple and multiple linear regression models built to predict `monthly_sales`.

### Comparison Table

| Model Name | Variables Used (Dependent ~ Independent) | R-squared | Significant Variables (p < 0.05) | Business Usefulness | Limitations |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Simple Model 1** | `monthly_sales` ~ `marketing_spend` | [0.45] | `marketing_spend` | Provides a basic baseline for marketing ROI. Easy to explain to stakeholders. | Ignores other massive drivers of sales like footfall or stock levels, leading to omitted variable bias. |
| **Simple Model 2** | `monthly_sales` ~ `footfall` | [0.38] | `footfall` | Helps set expectations for sales based purely on store traffic. | Cannot be directly controlled by management (unlike marketing or inventory). |
| **Multiple Model 1 (Final)** | `monthly_sales` ~ `marketing_spend`, `footfall`, `inventory_availability_pct`, `is_premium_store` | [0.72] | `marketing_spend`, `inventory_availability_pct`, `is_premium_store` | Highly useful. Allows leadership to see the isolated impact of inventory improvements while controlling for marketing and footfall. | Assumes linear relationships. Does not capture external macroeconomic factors or competitor pricing. |

### Summary of Findings
The multiple regression model significantly outperforms both simple models, as evidenced by the jump in R-squared from roughly [0.45] to [0.72]. This indicates that sales are driven by a combination of factors rather than a single silver bullet.

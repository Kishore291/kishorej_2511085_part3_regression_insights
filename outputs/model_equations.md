# Model Equations & Variable Explanations

### 1. Dummy Variable Approach
To include the categorical variable `storetype` in the regression, dummy variables were created.
* **Categories present:** Standard, Premium, Outlet.
* **Reference Category:** `Standard` was chosen as the reference category because it represents the majority of our locations.
* **Variables created:** `ispremium` (1 if Premium, 0 otherwise) and `isoutlet` (1 if Outlet, 0 otherwise).

### 2. Simple Regression Equations
**Model 1 (Marketing Spend):**
$$\text{Monthly Sales} = [15,000] + [3.25] \times (\text{Marketing Spend})$$
* **Interpretation:** For every additional $1 spent on marketing, monthly sales are expected to increase by $[3.25], ignoring all other factors.

**Model 2 (Footfall):**
$$\text{Monthly Sales} = [20,000] + [45] \times (\text{Footfall})$$
* **Interpretation:** Every additional 1,000 visitors (footfall) is associated with a $[45]$ increase in monthly sales.

### 3. Final Multiple Regression Equation
$$\text{Monthly Sales} = [10,500] + [2.10] \times (\text{Marketing Spend}) + [15] \times (\text{Footfall}) + [500] \times (\text{Inventory Availability \%}) + [8,000] \times (\text{ispremium})$$

### 4. Coefficient Explanations for Final Model
* **Intercept ($[10,500]$):** The theoretical baseline sales if marketing, footfall, and inventory were all zero, for a Standard store.
* **Marketing Spend ($[2.10]$):** Holding other factors constant, every $1 increase in marketing spend yields a $[2.10]$ increase in sales. (Notice this is lower than the simple model, as the simple model was artificially inflated by not accounting for footfall).
* **Inventory Availability \% ($[500]$):** Holding other factors constant, a 1% increase in inventory availability is associated with a $[$500$]$ increase in monthly sales.
* **ispremium ($[8,000]$):** Holding other factors constant, being a Premium store is associated with $[$8,000$]$ more in monthly sales compared to a Standard store (the reference category).

### 5. Final Model Selection
The Multiple Regression model was chosen as the final model because it provides a much higher R-squared ($[0.72]$) and paints a more realistic picture of business operations by isolating the impact of controllable variables (marketing, inventory) while controlling for environmental variables (footfall, store type).

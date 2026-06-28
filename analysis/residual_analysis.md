# Residual Analysis

### Methodology
Residuals were calculated based on the predictions from the Final Multiple Regression Model. The formula used is:
$$\text{Residual} = \text{Actual Sales} - \text{Predicted Sales}$$

### Top 5 Positive Residuals (Under-predicted by Model)
These are stores where actual sales were significantly *higher* than what our model predicted.

1. **Record ID [142]:** Residual = +$[12,500]
2. **Record ID [89]:** Residual = +$[11,200]
3. **Record ID [34]:** Residual = +$[10,850]
4. **Record ID [210]:** Residual = +$[9,400]
5. **Record ID [17]:** Residual = +$[8,900]

**Business Interpretation:** The model is under-predicting sales for these locations. This suggests there is a "hidden factor" driving success at these stores that is not in our dataset (e.g., exceptional store management, a localized event, or a highly skilled sales team). We should investigate these stores to learn from their best practices.

### Top 5 Negative Residuals (Over-predicted by Model)
These are stores where actual sales were significantly *lower* than what our model expected given their marketing, footfall, and inventory.

1. **Record ID [56]:** Residual = -$[15,300]
2. **Record ID [112]:** Residual = -$[14,100]
3. **Record ID [203]:** Residual = -$[12,900]
4. **Record ID [8]:** Residual = -$[11,500]
5. **Record ID [77]:** Residual = -$[10,200]

**Business Interpretation:** The model is over-predicting sales for these locations. Despite having good fundamentals (high inventory, decent marketing spend), they are underperforming. This could indicate localized issues such as poor customer service, aggressive local competition, or unfavorable store layouts. These stores require immediate management review.

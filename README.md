# Retail Performance & Profitability Dataset

## Project Overview
This project analyzes 9,994 transactions from a U.S. retail chain (2014–2017) to uncover hidden drivers of profit leakage. While the business maintains an overall profit margin of 12.47%, nearly 18.72% of all transactions are loss-making. This analysis provides a structured decision-support framework to optimize pricing and discount strategies.


## File Details

**Filename:** superstore_retail_sales_dataset.csv 
**Total Records:** 9,994 core transactions 
**Primary Keys:** Row_ID, Order_ID

--- 

## Data Dictionary

| Column Name | Description | Data Type |
|-------------|------------|-----------|
| Order Date | Date of original customer transaction. | Date |
| Category | High-level product group (Furniture, Technology, etc.). | Categorical |
| Sub-Category | Specific product type (Tables, Chairs, Phones). | Categorical |
| Sales | Total revenue per transaction. | Float |
| Profit | Net earnings after costs and discounts. | Float |
| Shipping Delay | Days between order and shipment. | Integer |
| Sales Impact Score | Weighted ranking metric (Profit × Quantity). | Float |
| Loss Flag | Binary indicator for negative-margin sales. | Categorical |

--- 

## Key Insights & Statistics

- **The 30% Threshold:** 60.93% of all loss-making transactions occur when discounts exceed 30%, identifying a critical "break-even" ceiling.
- **Category Divergence:** Technology leads with a 17.40% margin, while Furniture struggles at a critically low 2.49%.
- **Regional Stability:** The West Region serves as the most stable profit contributor, whereas the Central region shows higher loss volatility.
- **Seasonal Volatility:** Sales peak significantly in Q4, but aggressive holiday discounting often leads to "hollow growth" where margins flatten.

---

## Analysis Suggestions

1. **Discount Control:** Use the Loss Flag to identify the exact discount percentage where a sub-category transitions from profitable to loss-making.
2. **Logistics Efficiency:** Analyze how `Shipping Delay` affects the `Profit Margin` across different geographic regions.
3. **Retention Health:** Compare Average Tenure vs. Churn to determine if delivery friction is driving away long-term loyalists.
4. **Strategic Mix:** Use the `Sales Impact Score` to rank the Top 10 products that must be protected for business sustainability.

---

## Data Engineering Notes

- **Outlier Treatment:** Validated and treated extreme discount values to ensure a reliable 12.47% overall margin calculation.
- **Feature Engineering:** Created Shipping Delay and Sales Impact Score to provide "new sight" into operational bottlenecks.
- **Data Validation:** Resolved geographic nulls and standardized product naming to ensure 100% categorical accuracy.
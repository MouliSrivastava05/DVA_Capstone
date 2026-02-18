# Retail Performance & Profitability Dataset

## Project Overview
This dataset provides a granular log of retail transactions for a global U.S. chain, covering the period from January 2014 through December 2017. It is engineered to move beyond surface-level metrics to identify critical profit leakage and support executive-level strategic decisions. By analyzing high-volume but low-margin sub-categories like Furniture, this data enables targeted interventions in pricing and logistics.

---

## File Details

**Filename:** superstore_retail_sales_dataset.csv 
**Total Records:** ~10,000 core transactions 
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

- **Profit Leakage:** Identified a critical **-$17,725 loss** within the Tables sub-category despite high sales volume.
- **Logistics Friction:** A direct correlation exists between high shipping delays and margin erosion in bulky product categories.
- **Top Performer:** The Technology category consistently outperforms others, contributing approximately **30% of total profit**.
- **Seasonal Volatility:** Sales spikes occur in **Q4 (Quarter 4)**, but profit margins often flatten due to aggressive holiday discounting.

---

## Analysis Suggestions

1. **Discount Sensitivity:** Calculate the correlation between `Discount %` and `Net Profit` to find the "Break-Even" discount ceiling.
2. **Logistics Efficiency:** Analyze how `Shipping Delay` affects the `Profit Margin` across different geographic regions.
3. **Customer Lifecycle:** Compare **Average Tenure vs. Churn** to see if delivery delays are driving away long-term loyalists.
4. **Strategic Mix:** Use the `Sales Impact Score` to rank the Top 10 products that must be protected for business sustainability.

---

## Data Cleaning Notes

- **Outlier Treatment:** Extreme discount values exceeding **80%** were capped to prevent skewing average profitability.
- **Normalization:** All `Order Date` fields must be converted to datetime objects before performing time-series or seasonal analysis.
- **Null Values:** Missing postal codes or customer IDs were resolved using cross-referencing to ensure geographic accuracy.
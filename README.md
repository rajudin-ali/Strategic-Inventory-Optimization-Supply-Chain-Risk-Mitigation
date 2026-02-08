# Strategic-Inventory-Optimization-Supply-Chain-Risk-Mitigation
Developed a Python-based Logistics System to optimize 1,000+ SKUs using ABC Analysis and automated replenishment logic. I engineered a proactive risk radar for stockouts and expiration (FEFO strategy), transforming raw data into actionable insights that reduce capital tie-up and operational waste. Ideal for data-driven supply chain management

# Dataset Link : https://www.kaggle.com/datasets/salahuddinahmedshuvo/grocery-inventory-and-sales-dataset 

## EDA (Exploratory Data Analysis)
<img width="940" height="613" alt="image" src="https://github.com/user-attachments/assets/644af097-9539-4f47-86c1-f8fdc0a9db15" />

Key Insights from Bar Chart
- Market Leader: Fruits & Vegetables is the undisputed top performer, achieving a sales volume of approximately 19,000+ units. This is nearly double the volume of the next best category, indicating it is the primary driver of inventory turnover.
- Secondary Performers: Dairy follows in second place (~11,000 units), while Grains & Pulses sits in third (~9,000 units). These represent the core "stable" categories of the business.
- Underperformers: Beverages, Oils & Fats, and Bakery are the lowest-performing segments, all hovering around the 4,500–5,000 unit mark.
- Data Reliability: The black vertical lines (error bars) at the top of each bar indicate confidence intervals or variability. The relatively short bars suggest that sales for these categories are stable and the data is consistent, with the highest variance seen in the Fruits & Vegetables category.

<img width="847" height="716" alt="image" src="https://github.com/user-attachments/assets/bf144557-a9cd-4e51-8cc6-e2d328b9a0f5" />

Data Insights From Heatmap Correlation
- Weak Positive Correlations: The highest correlation in the dataset is between Sales Volume and Inventory Turnover Rate at 0.062. While logically we expect high sales to drive turnover, this value is so close to zero that the relationship is statistically negligible in this specific dataset.
-Negligible Relationship between Stock and Sales: The correlation between Stock Quantity and Sales Volume is only 0.032. This suggests that high stock levels do not necessarily result in higher sales volumes, or vice versa, for this period.
- Price Neutrality: Unit Price shows almost zero or slightly negative correlations with all other factors, such as -0.009 with Sales Volume and -0.027 with Turnover Rate. This implies that price fluctuations (within the current range) are not significantly impacting the volume of goods sold or the speed of inventory movement.

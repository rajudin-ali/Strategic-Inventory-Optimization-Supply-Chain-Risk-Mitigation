# Strategic-Inventory-Optimization-Supply-Chain-Risk-Mitigation
Developed a Python-based Logistics System to optimize 1,000+ SKUs using ABC Analysis and automated replenishment logic. I engineered a proactive risk radar for stockouts and expiration (FEFO strategy), transforming raw data into actionable insights that reduce capital tie-up and operational waste. Ideal for data-driven supply chain management

# Dataset Link : 
https://www.kaggle.com/datasets/salahuddinahmedshuvo/grocery-inventory-and-sales-dataset 

## EDA (Exploratory Data Analysis)
<img width="940" height="613" alt="image" src="https://github.com/user-attachments/assets/644af097-9539-4f47-86c1-f8fdc0a9db15" />

Key Insights from Bar Chart
- Market Leader: Fruits & Vegetables is the undisputed top performer, achieving a sales volume of approximately 19,000+ units. This is nearly double the volume of the next best category, indicating it is the primary driver of inventory turnover.
- Secondary Performers: Dairy follows in second place (~11,000 units), while Grains & Pulses sits in third (~9,000 units). These represent the core "stable" categories of the business.
- Underperformers: Beverages, Oils & Fats, and Bakery are the lowest-performing segments, all hovering around the 4,500–5,000 unit mark.
- Data Reliability: The black vertical lines (error bars) at the top of each bar indicate confidence intervals or variability. The relatively short bars suggest that sales for these categories are stable and the data is consistent, with the highest variance seen in the Fruits & Vegetables category.

<img width="847" height="716" alt="image" src="https://github.com/user-attachments/assets/bf144557-a9cd-4e51-8cc6-e2d328b9a0f5" />

Data Insights From Heatmap Correlation
- Metric Independence: The heatmap reveals an extremely low correlation across all variables. The highest correlation (Sales Volume vs. Inventory Turnover) is only 0.062, which is statistically negligible.
- Stock vs. Sales Gap: The correlation between Stock Quantity and Sales Volume is nearly zero (0.032). This indicates that current inventory levels are not aligned with actual sales demand.
- Price Inelasticity: Unit Price shows no significant impact on sales volume (-0.009) or turnover (-0.027). This suggests that for these specific items, price changes are not currently driving customer behavior.

## Output Result
<img width="639" height="245" alt="image" src="https://github.com/user-attachments/assets/40ad2506-a82e-4d41-a373-556cfee7280a" />

### Action Plan: Top Priority Reorders
This table identifies critical stock shortages where the Stock Quantity has fallen below the defined Reorder Level.
- Inventory Deficit: Several high-value products are at risk of stockouts. For instance, Halibut (Wikiiz) has only 14 units left against a reorder level of 67, and Black Coffee (Quamba) has 37 units against a requirement of 94.
- Supplier Concentration: Multiple "White Tea" and "Arabica Coffee" SKUs from different suppliers (Viva, Agivu, Jayo, Feedmix) are all hitting reorder triggers simultaneously.

### Professional Recommendations & Strategy
Based on the data provided, I recommend the following actions:
- Immediate Tactical Responses (Inventory) Execute Emergency Reorders: Prioritize reordering Halibut and Black Coffee immediately, as they show the largest gaps between current stock and safety levels.
- Supplier Review: Since several tea and coffee products are low across different suppliers, consolidate these orders to negotiate better shipping rates or bulk discounts.

### Strategic Adjustments (Data Science)
- Optimize Reorder Levels: The heatmap shows that stock levels and sales volume are not correlated (0.032). This is a red flag suggesting your "Reorder Levels" might be set based on arbitrary numbers rather than actual sales velocity. You should recalculate these levels using a Demand-Driven Lead Time formula.
- Segmented Analysis: Perform a separate correlation analysis for each category (e.g., Beverages vs. Seafood). High-volume items like "Fruits & Vegetables" (from the previous chart) likely have different dynamics than "Seafood" (Halibut), and treating them as one dataset masks important trends.


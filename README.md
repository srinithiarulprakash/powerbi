Power BI Retail Sales Analytics Platform

About Dataset
1. Source & Scope:           Built upon a comprehensive commercial retail transactions dataset containing 9,994 records across multiple regions and product categories.
2. Volume Metrics:           Captures total gross sales revenue of $2,297,201.07, net profit of $286,397.79, and a cumulative physical inventory movement of 37,873 units.
3. Dimensions & Granularity: Tracks order-level data including order dates, monthly breakdowns, customer names, US states, product categories, sub-categories, and specific product names.

What We Focused On
1. Data Cleansing & Structuring:        Standardized raw transactional records, handled data anomalies, and prepared clean dimensional hierarchies for robust modeling.
2. Semantic Data Modeling:              Designed a scalable data structure integrating secure bindings and modern theme definitions (Fluent2-CY26SU08.json and Divergent.json).
3. Multi-Dimensional Business Analysis: Focused on uncovering regional sales drivers, high-margin product sub-categories, seasonal performance surges, and profitability bottlenecks.

Highlights: Cleaning, DAX Calculations, & Power BI Implementation
Data Cleaning & Preparation: Ensured schema integrity, resolved null values in categorical fields, and structured data types to support efficient aggregations.

Custom DAX Calculations: Developed core semantic measures to power dynamic reporting:

1. Total Sales Revenue: Total Sales = SUM(salesdata[Sales])
2. Total Net Profit: Total Profit = SUM(salesdata[Profit])
3. Total Order Count: Total Orders = COUNTROWS(salesdata)
4. Total Quantity Sold: Total Quantity = SUM(salesdata[Quantity])
5. Overall Net Profit Margin: Profit Margin % = DIVIDE([Total Profit], [Total Sales], 0)
6. Average Order Value (AOV): Average Order Value = DIVIDE([Total Sales], [Total Orders], 0)
7. Time Intelligence: YTD Sales = TOTALYTD([Total Sales], salesdata[Order Date]) and Previous Month Sales = CALCULATE([Total Sales], DATEADD(salesdata[Order Date], -1, MONTH))

Power BI Architecture: Configured modular page layouts (Report/definition/) and visual containers (visual.json) delivering clean card metrics, geographic distributions, and trend lines.

Findings, Results, & Business Value
1. Revenue Drivers: High-value sub-categories like Phones ($330,007.10) and Chairs ($328,449.13) serve as the primary monetary pillars of the business.
2. Geographic Concentration: Commercial demand is heavily weighted toward key urban hubs, led by California (2,001 orders) and New York (1,128 orders).
3. Inventory Movement: Office Supplies drive high-frequency physical replenishment with 22,906 units sold out of 37,873 total items.
4. Seasonality Surges: Performance peaks sharply in late Q3 and Q4, highlighted by September (1,383 orders) and November ($352,461.09 in sales).
5. Strategic Business Value: Empowers stakeholders with instant, interactive visibility into margins and regional performance, enabling optimized warehouse inventory allocation, targeted marketing campaigns, and disciplined pricing strategies.

Conclusion
This project successfully bridges raw transactional data and executive decision-making through an end-to-end Power BI analytics platform. By combining rigorous data cleansing, advanced DAX modeling, and intuitive visual storytelling, the solution provides clear operational insights that help businesses optimize inventory logistics, maximize category profitability, and capitalize on seasonal revenue trends.

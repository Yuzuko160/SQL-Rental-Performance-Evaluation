# SQL Database Management Coursework: Rental Performance Evaluation
This repository contains a comprehensive performance evaluation of a movie rental system, utilizing SQL and Python to derive actionable business insights. The project focuses on identifying revenue drivers, optimizing inventory, and segmenting customer behavior through advanced relational database querying.

## 📋 Project Outline
- The evaluation is structured into eight key analytical modules:

- Genre Analysis: Ranking film genres by rental frequency to identify market demand.

- Geospatial Distribution: Mapping rental volumes by city to identify high-performing regions.

- Performance Heatmapping: A 2D evaluation of Genre vs. City to pinpoint localized preferences.

- Customer Segmentation: Identifying the "Top 20" most valuable customers by lifetime value.

- Revenue Proportions: Analyzing the contribution of premium customers to total revenue.

- Inventory Optimization: Identifying the "bottom 20" and zero-rental films for platform pruning.

## 🛠️ Technical Skills Acquired
As a SQL Programmer, this project demonstrated proficiency in:

- Complex Joins: Connecting multiple relational tables (Inventory, Rentals, Payments, Customers, and Addresses).

- Aggregations & Window Functions: Using COUNT, SUM, and RANK() to generate competitive leaderboards.

- Data Cleaning: Filtering and handling null values, specifically focusing on excluding/identifying non-performing assets.

- Python Integration: Using Python for data visualization (Pie charts and Heatmaps) to complement SQL query outputs.

- CTE & Subqueries: Structuring readable, modular SQL code for multi-step data transformations.

## 💡 Key Insights
Inventory Pruning: Identified 42 films with zero rentals, recommending their removal to reduce database overhead and platform clutter.

- Customer Concentration: Quantified the revenue proportion of high-value customers, providing a baseline for loyalty program ROI.

- Regional Dominance: Pinpointed specific cities with the highest rental density, suggesting targeted marketing spend for those demographics.

- Genre Trends: Established a clear hierarchy of film genres, allowing for data-driven procurement of new titles.

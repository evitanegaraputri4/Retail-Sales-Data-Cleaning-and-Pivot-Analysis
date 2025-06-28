# Retail Data Cleaning and Pivot Analysis Project
## Project Overview
This project focuses on cleaning and standardizing a retail sales dataset that initially contained inconsistent data formats, missing values, duplicate entries, and formatting irregularities across multiple columns. The raw dataset posed challenges such as inconsistent date formats, names with extra spaces and varied capitalization, and missing critical values that hindered accurate analysis and reporting. Using Microsoft Excel, I meticulously consolidated, cleaned, and standardized the dataset to enhance data quality, consistency, and integrity, preparing it for reliable analysis and visualization. In addition to data cleaning, the project includes comprehensive **PivotTable-based analysis** to uncover key insights into product performance, customer behavior, seasonal trends, city-wise distribution, and discount patterns. These summaries support actionable business recommendations across sales, marketing, product, and fulfillment strategies.

---

## Tools Used

- Microsoft Excel (Data Cleaning and Pivot Tables)
- Power Query (for date parsing and transformation)
---

## Cleaning Process

### Initial Data

The dataset consisted of a single table containing 10 columns, with multiple data quality issues including missing values, inconsistent text formatting, inconsistent date formats (some dates were stored as text or General format instead of proper Date format), and duplicate rows.

### Data Cleaning & Standardization Steps

1. **Standardizing Customer Names**
   - Trimmed extra spaces and unified name casing.
   - Replaced 12 missing names with `"Na"` placeholder.

2. **Handling Missing Products**
   - Replaced 30 missing product names with `"Na"`.

3. **Fixing Quantity Format**
   - Converted all quantity values from words (e.g., “Two”) to numeric values (e.g., `2`) for 1990 rows.

4. **Date Standardization**
   - Used Excel parsing functions to convert all dates to `DD/MM/YYYY` format.
   - Supported formats like `2024-10-15`, `14-Aug-2024`, and `03/04/2025`.

5. **Location Name Cleanup**
   - Standardized city names using a reference table and `XLOOKUP`, resolving abbreviations like `LA`, `Chi-Town`, and `SF`.

6. **Fixing Payment Method Inconsistencies**
   - Replaced 12 missing values with `"Na"`.
   - Standardized capitalization (e.g., `paypal` → `PayPal`) for 1003 records.

7. **Adding New Calculated Columns**
   - `Sales = Quantity × Price`
   - `Net Sales = Quantity × Price × (1 - Discount%)`

**Access the cleaned dataset here:**  
[Google Sheets - Retail Sales Cleaned Data]

---

## Dataset Summary
| Aspect                      | Before Cleaning                          | After Cleaning                                |
|-----------------------------|-------------------------------------------|-----------------------------------------------|
| Total Rows                  | 1990                                      | 1990                                          |
| Missing Customer Names      | 12                                        | Replaced with `"Na"`                          |
| Missing Product Names       | 30                                        | Replaced with `"Na"`                          |
| Quantity as Words           | e.g., "Two", "Three"                      | Converted to numeric                          |
| Inconsistent Date Formats   | Mixed (Text, General, Various styles)     | Unified to DD/MM/YYYY                         |
| Inconsistent City Names     | Abbreviations (LA, SF, Chi-Town)          | Standardized full names                       |
| Inconsistent Payment Names  | Capitalization and typos                  | Proper case applied                           |
| New Columns Added           | Sales, Net Sales                          | Calculated and validated                      |

---

## Data Cleaning Documentation

| No | Table           | Issue                                                                 | Row Count | Solvable? | Resolution                                                                 |
|----|------------------|------------------------------------------------------------------------|-----------|-----------|----------------------------------------------------------------------------|
| 1  | Customer Name     | Inconsistent names and spacing                                         | 1990      | Yes       | Trimmed and standardized capitalization                                   |
| 2  | Customer Name     | Missing values                                                         | 12        | Yes       | Replaced with `"Na"`                                                       |
| 3  | Product           | Missing values                                                         | 30        | Yes       | Replaced with `"Na"`                                                       |
| 4  | Quantity          | Text format ("Two", "One") instead of numbers                          | 1990      | Yes       | Converted to numbers                                                       |
| 5  | Date              | Inconsistent formats (DD/MM/YYYY, YYYY-MM-DD, etc.)                    | 1990      | Yes       | Standardized using parsing functions                                      |
| 6  | City              | Abbreviations and inconsistent names (e.g., "LA", "Chi Town")          | 103       | Yes       | Standardized via `XLOOKUP` and reference list                             |
| 7  | Payment Method    | Missing values                                                         | 12        | Yes       | Replaced with `"Na"`                                                       |
| 8  | Payment Method    | Inconsistent casing (e.g., "paypal", "cash")                           | 1003      | Yes       | Standardized to proper case                                                |
| 9  | Sales             | Not originally present                                                 | 1990      | Yes       | Added `Sales = Quantity × Price`                                           |
| 10 | Net Sales         | Not originally present                                                 | 1990      | Yes       | Added `Net Sales = Quantity × Price × (1 - Discount / 100)`               |

---
## 
## 📈 Pivot Table Analysis & Insights

### 1. Net Sales vs. Total Sales by Product Category
- Blender leads both total and net sales, indicating it is a consistently high-performing item, even after discounts.
- Jeans and Watch follow closely, with minimal difference between sales and net sales.
- Smartphone shows the largest relative drop between sales and net sales.
- Product categories exhibit consistent discount behavior, as the gap between sales and net sales remains relatively narrow across the board.

---

### 2. Average Discount by Category
- Most product categories receive an average discount of 8%, indicating a uniform pricing strategy.
- Headphones, Jeans, and Blender are offered at 7% on average , slightly below other
- The overall average discount across all categories is stable at 8%, which suggests a controlled promotional policy.
---

### 3. Top 5 Customers by Net Sales
- Jason Bond, Dillon King, and Casey Diaz are the top contributors to revenue, collectively accounting for more than 20% of the top 5 segment's sales.
- The highest individual net sale is over 61,000 units, highlighting strong customer loyalty or bulk purchasing.

---

### 4. Average Net Sales by Top 10 Customers
- Ryan Moore leads the average net sales per order, followed closely by Jason Bond and Austin Perry.
- All top 10 customers have average sales within a narrow band (around 2,700–3,000), showing consistent spending patterns.
- This suggests a stable high-value customer group that could be targeted for premium offers or loyalty incentives.

---

### 5. Monthly Net Sales Summary
- April is the top-performing month, followed by March and June, indicating strong sales activity in Q2.
- November and December are the lowest-performing months, possibly due to seasonality.
- The overall distribution shows a steady mid-year peak with a gradual decline toward year-end, indicating potential for seasonal promotion planning.

---

### 7. Net Sales by Category & City
- New York is the leading city across all product categories, driven by strong performance in Sports, Electronics, and Clothing.
- Los Angeles and San Francisco follow, with relatively even category performance, though LA shows stronger sales in Toys and Electronics.
- Houston contributes the least, reflecting either a smaller customer base or lower promotional penetration in that region.
---

### 8. Payment Method by City
- Cash is still dominant in New York, while Debit Card and PayPal see widespread use across all cities.
- Credit Card is slightly less used overall, but remains consistent across cities.
- Houston has the lowest total number of transactions, across all payment types — possibly correlating with its overall lower sales volume.
---

### 9. Product Sales Volume by City
- New York again leads with the highest product volume across all categories, especially in Blender, Headphones, and Watch.
- Los Angeles and San Francisco follow closely with strong performance in Smartphones and T-shirts.
- Houston shows notably lower volumes, particularly in Jeans and Watch, which may indicate either lower demand or inventory constraints.

---

## Recommendations

### 1. Sales Trend Optimization
- Boost November Performance: November is the lowest net sales month. Launch aggressive sales events like Black Friday flash deals and “Buy More, Save More” offers to reverse the dip.
- Pre-April Campaigns: April ranks highest in net sales—test pre-spring exclusives or loyalty-first launches in March to build momentum.
- Created Monthly Email Calendar: Align discount depth with seasonal trends. Use a rotating monthly schedule (e.g., % off in slow months, bundles in peak months).
- Retargeting Strategy: Reactivate low-engagement months via Meta/Google ads that promote high-appeal products like Blender and Jeans.
---

### 2. Product Line Optimization
- Upsell High Revenue Products: Promote Blender, Jeans, and Watch using tiered bundles, seasonal kits, or influencer tutorials (especially for Blender).
- Address Low Net Margin Items: Products like Smartphone show high discounts. Consider revising pricing or bundling with low-cost accessories to protect margin.

---

### 3. Customer Retention & Growth
- Reward High-Value Customers: Jason Bond and Dillon King lead in net sales. Target your top 5% of customers with VIP campaigns and early-bird promos.
- Maximize Customer Lifetime Value: Use average net sales data to offer subscription-like product refreshes (e.g., biannual clothing bundles).
- Revive Lapsed Buyers: Identify one-time buyers from Jan–Mar and create personalized email flows offering discounts based on prior items.

---

### 4. City-Focused Marketing
- Double Down on New York: NY leads in product volume and net sales. Offer same-day shipping, city-specific promo codes, and pickup points to reinforce dominance.
- Expand in Houston & Chicago: These cities show strong product diversity but lower totals—test “Free Shipping Week” or local influencer collabs.
- Geo-Test Bundled Discounts: Launch combo offers (e.g., Watch + Jeans) in Los Angeles to drive higher order values.
---

### 5. Discount Strategy
- Limit Blanket Discounts: With average discounts hovering around 8%, reserve high discounts for low-performing products. 
- Run “Limited Quantity” Drops: T-shirt and Smartphone categories should feature exclusive short-run discounts to create urgency.
---


# Contact
For any questions or inquiries, please contact evitanegara@gmail.com


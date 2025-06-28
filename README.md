# Retail Sales Data Cleaning using Excel
## Project Overview

This project focuses on cleaning and standardizing a retail sales dataset that initially contained inconsistent data formats, missing values, duplicate entries, and formatting irregularities across multiple columns. The raw dataset posed challenges such as inconsistent date formats, names with extra spaces and varied capitalization, and missing critical values that hindered accurate analysis and reporting. Using Microsoft Excel, I meticulously consolidated, cleaned, and standardized the dataset to enhance data quality, consistency, and integrity, preparing it for reliable analysis and visualization.

---

## Tools Used

- Microsoft Excel

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

## Next Steps & Recommendations

- Review remaining placeholder `"Na"` or missing numeric fields with stakeholders for clarification.
- Apply data validation rules or automated Power Query/Macros for future data collection consistency.
- Extend analysis with Power BI dashboards or pivot charts for more insightful reporting.
- Export cleaned data into a database or cloud storage for scalable access.

---

## Screenshots

- Initial raw dataset with inconsistent formats and missing values.
  ![image](https://github.com/user-attachments/assets/886ca3df-b557-4ce8-b6ea-5ac133042af4) 
- Final cleaned dataset with standardized columns, consistent date formats, and removed duplicates.
- ![image](https://github.com/user-attachments/assets/1253c3b1-6ed4-4a7d-bfb8-3c30f338b5ac)


---

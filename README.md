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

1. **Handling Missing Values**  
   - Recategorized missing values in categorical columns such as `Customer_Name`, `Product_Name`, and `Payment_Method` as `"Unknown"` to clearly mark incomplete records.  
   - Left missing numeric values like `Quantity`, `Price_Per_Unit`, and `Discount_Percentage` as is with `"Unknown"` placeholders where inference was not possible, noting these for further stakeholder review.

2. **Standardizing Text Data**  
   - Removed leading or trailing spaces and standardized capitalization in columns like `Customer_Name` and `Payment_Method` using Excel's `TRIM` and text functions to ensure uniformity.

3. **Fixing Quantity Formats**  
   - Converted all quantity values from text (example : "one") to numeric values (example :1) for consistent quantitative analysis.

4. **Date Column Cleanup**  
   - Identified columns such as Transaction_ID stored as General or Text data types instead of Number format, which can cause issues in data analysis, sorting, and calculations.
   - Dates were stored in General or Text formats rather than Excel’s proper Date format, leading to challenges in date-based operations like sorting, filtering, and calculations.
   - Applied Excel’s date conversion functions to transform text dates into standardized Date format, enabling accurate time-based analysis.  
   - Unified various date formats such as `"14-Jul-2023"`, `"23/12/2023"`, and `"2023-06-14"` into a consistent format.

5. **Standardizing Store Location**  
   - Corrected inconsistent spellings and abbreviations of store locations (e.g., `"LA"` vs `"Los Angeles"`, `"Chi Town"` vs `"Chicago"`), unifying them for accurate grouping and reporting.

6. **Removing Duplicates**  
   - Identified and removed 20 fully duplicated rows to improve data integrity.

---

## Dataset Summary

| Aspect                  | Before Cleaning                 | After Cleaning                                |
|-------------------------|--------------------------------|-----------------------------------------------|
| Total Columns           | 10                             | 12 (after adding cleaned and standardized columns)  |
| Duplicate Rows          | Present (20 duplicates)         | Removed duplicates                            |
| Missing Values          | Present in multiple columns     | Recategorized or documented for stakeholder input |
| Inconsistent Date Format| Dates stored as Text/General   | Converted to uniform proper Date format      |
| Inconsistent Text Format| Extra spaces, inconsistent caps| Trimmed and standardized capitalization      |
| Quantity Format         | Mixed numeric and text         | Converted all to numeric format               |
| Store Location Names    | Multiple inconsistent spellings| Standardized names                            |

---

## Data Cleaning Documentation

| No | Table        | Column             | Issue                                                        | Row Count | Solvable? | Resolution                                                                                      |
|-----|--------------|--------------------|--------------------------------------------------------------|-----------|-----------|-------------------------------------------------------------------------------------------------|
| 1   | Retail Sales | Customer_Name      | Missing values                                               | 51        | Yes       | Recategorized missing values as "Unknown"                                                     |
| 2   | Retail Sales | Customer_Name      | Inconsistent names, extra spaces, and capitalization         | -         | Yes       | Standardized names by trimming spaces and unifying capitalization                             |
| 3   | Retail Sales | Product_Name       | Missing values                                               | 51        | Yes       | Recategorized missing values as "Unknown"                                                     |
| 4   | Retail Sales | Quantity           | Missing values                                               | 3         | No        | Left as is, with "Unknown" placeholders, requires stakeholder review                          |
| 5   | Retail Sales | Quantity           | Inconsistent formats: words ("one") vs numbers ("1")         | 347       | Yes       | Converted all quantity values to numeric format                                               |
| 6   | Retail Sales | Price_Per_Unit     | Missing values                                               | 164       | No        | Left as is; missing prices marked "Unknown"                                                  |
| 7   | Retail Sales | Purchase_Date      | Missing values and inconsistent data type (dates stored as text/General) | 50        | No        | Left as is with "Unknown"; converted text dates to proper Date format                         |
| 8   | Retail Sales | Purchase_Date      | Inconsistent date formats                                     | 814       | Yes       | Standardized dates to consistent format using Excel date functions                            |
| 9   | Retail Sales | Store_Location     | Inconsistent spelling and abbreviations                      | -         | Yes       | Standardized store location names                                                            |
| 10  | Retail Sales | Payment_Method     | Missing values                                               | 128       | Yes       | Recategorized missing values as "Unknown"                                                    |
| 11  | Retail Sales | Payment_Method     | Inconsistent capitalization                                  | 724       | Yes       | Standardized payment method capitalization                                                   |
| 12  | Retail Sales | Discount_Percentage| Missing values                                               | 193       | No        | Left as is with "Unknown"; zero retained for no discount                                     |
| 13  | Retail Sales | -                  | Duplicate rows                                              | 20        | Yes       | Removed duplicates to ensure data quality                                                    |

---

## Next Steps & Recommendations

- Collaborate with stakeholders to clarify missing and ambiguous data points, especially for numeric and date columns with incomplete values.  
- Normalize currency values or convert all amounts to a consistent currency format for financial analysis.  
- Implement automated validation and cleaning workflows using Excel macros or Python scripts for future data ingestion to reduce manual effort.  
- Conduct exploratory data analysis (EDA) and build interactive dashboards to visualize sales trends and customer behavior insights.

---

## Screenshots

- Initial raw dataset with inconsistent formats and missing values.
  ![image](https://github.com/user-attachments/assets/886ca3df-b557-4ce8-b6ea-5ac133042af4) 
- Final cleaned dataset with standardized columns, consistent date formats, and removed duplicates.
- ![image](https://github.com/user-attachments/assets/1253c3b1-6ed4-4a7d-bfb8-3c30f338b5ac)


---

## Access the Cleaned Dataset

[Link to Google Sheets - Retail Sales Cleaned Data](#)  *(https://docs.google.com/spreadsheets/d/1q9r5iwsUrB6ugBb35FmyVoIVZBihf6l-/edit?usp=sharing&ouid=111790817268098102104&rtpof=true&sd=true)*

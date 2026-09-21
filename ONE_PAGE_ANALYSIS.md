# Capstone Candidate Workbook Analysis

## 1. Workbook Identity & Context
This analysis evaluates the **Sanitized Inventory Reorder Tool**, derived from a retail inventory management process used by small business store operations. 

## 2. Operational Functionality
The workbook calculates safety stock levels, determines reorder points, and generates recommended purchase quantities based on weekly sales demand, current stock on hand, and supplier lead times.

## 3. Users and Stakeholders
The primary user is the **Store Operations Manager**, who inputs weekly stock counts. The **Purchasing Assistant** depends directly on the output to place orders with suppliers.

## 4. Operational Risk & Consequences
If the calculations in this workbook fail or are misconfigured:
- **Under-ordering:** Results in stockouts of critical items, leading to lost revenue and customer dissatisfaction.
- **Over-ordering:** Leads to excess inventory, tying up cash flow and increasing warehouse holding costs.

## 5. Suspected Fragilities & Vulnerabilities
1. **Hard-coded constants:** Safety stock multipliers are embedded inside individual cell formulas rather than centralized parameters.
2. **Inconsistent SUM ranges:** Aggregation formulas in footer rows fail to capture newly appended data rows.
3. **Absence of boundary validation:** Negative stock inputs or zero lead-times produce mathematically possible but operationally absurd order recommendations.

## 6. Proposed Python Improvement Direction
Converting this process into a Python tool will allow:
- Centralized configuration parameters separated from calculation logic.
- Automated `pytest` coverage for edge-case inventory thresholds.
- Strict input validation raising explicit exceptions for invalid stock entries.
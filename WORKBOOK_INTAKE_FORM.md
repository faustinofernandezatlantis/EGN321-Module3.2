# Capstone Workbook Intake Form

## 1. General Information
- **Workbook Name:** Inventory_Reorder_Tool_Sanitized.xlsx
- **Source / Setting:** Small Business / Retail Inventory Management
- **Primary User Role:** Store Operations Manager & Purchasing Assistant
- **Usage Frequency:** Weekly

## 2. Operational Purpose
This workbook tracks inventory stock levels, calculates weekly usage rates, estimates lead-time demand, and automatically highlights items that require reordering to prevent stockouts.

## 3. Core Inputs and Outputs
### Primary Inputs
1. `Current_Stock` (units) - Manual count entered weekly.
2. `Weekly_Demand` (units/week) - Historical average sales rate.
3. `Lead_Time_Weeks` (weeks) - Supplier delivery time.
4. `Safety_Stock_Factor` (multiplier) - Business rule constant.

### Primary Outputs
1. `Reorder_Point` (units) - Minimum inventory threshold before placing a new order.
2. `Order_Quantity` (units) - Recommended replenishment quantity.
3. `Reorder_Status` (Flag/Text) - Action indicator ("REORDER NOW" vs "OK").

## 4. Dependencies & Impact
The Purchasing Assistant relies on this sheet to issue purchase orders to suppliers. If calculations are wrong, the store either faces stockouts (lost sales) or overpurchasing (tied-up cash flow).
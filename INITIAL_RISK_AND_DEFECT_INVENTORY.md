# Initial Risk and Suspected Defect Inventory

*Note: The items listed below are suspected risks identified during initial audit and are subject to verification during capstone development.*

### Suspected Area 1: Hard-Coded Business Rules
- **Location:** Columns F and G (Safety Stock Calculation)
- **Observation:** A fixed multiplier `1.5` is hard-coded directly inside the formula `=C2*D2*1.5` rather than referencing a configurable parameter cell.
- **Risk:** Changing safety stock policy requires manually editing every row formula, creating risk of formula drift.

### Suspected Area 2: Inconsistent Range Reference
- **Location:** Summary Row 45 (`TOTAL_DEMAND`)
- **Observation:** The `=SUM(D2:D42)` range stops at row 42, but data continues through row 44.
- **Risk:** New inventory items added at the bottom are omitted from total purchasing demand estimates.

### Suspected Area 3: Lack of Input Validation
- **Location:** Column C (`Current_Stock`)
- **Observation:** Entering negative values or non-numeric strings does not trigger an error; formulas produce invalid negative order quantities.
- **Risk:** User data entry errors lead to invalid purchasing recommendations without warning.
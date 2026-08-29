# DecodeLabs Data Analytics – Project 1

## Data Cleaning & Preparation

### Overview

This project was completed as part of the DecodeLabs 2026 Data Analytics Internship.

The objective was to clean and prepare a raw dataset by identifying and handling missing values, duplicates, and data-format issues.

### Tools Used

- Python
- Pandas
- Jupyter Notebook

### Dataset Overview

- Rows: 1,200
- Columns: 14

### Data Cleaning Process

#### 1. Missing Values

The dataset initially contained 309 missing values in the `CouponCode` column.

These were replaced with `NO COUPON` to represent orders without a recorded coupon code.

After cleaning:

- Missing values: 0

#### 2. Duplicate Records

The dataset was checked for duplicate rows.

- Duplicate rows: 0
- Duplicate `OrderID`s: 0

#### 3. Date Validation

The `Date` column was inspected and validated.

- Missing dates: 0
- Invalid dates: 0
- Date data type: `datetime64[ns]`

#### 4. Numerical Data Validation

The numerical columns were inspected for unusual values.

The relationship between `Quantity`, `UnitPrice`, and `TotalPrice` was also validated:

`TotalPrice = Quantity × UnitPrice`

The calculated values matched the recorded `TotalPrice`, apart from negligible floating-point precision differences.

#### 5. Text Standardization

Text-based columns were inspected for inconsistencies.

The `CouponCode` values were standardized to uppercase:

- `Freeship` → `FREESHIP`
- `Winter15` → `WINTER15`
- `Save10` → `SAVE10`
- `No Coupon` → `NO COUPON`

### Final Validation

After cleaning, the dataset contained:

- 1,200 rows
- 14 columns
- 0 missing values
- 0 duplicate rows
- 0 duplicate `OrderID`s
- 0 invalid dates

### Conclusion

The dataset was successfully cleaned and validated using Python and Pandas, producing a consistent dataset ready for further analysis.

## Internship

**DecodeLabs – Data Analytics Internship, Project 1**

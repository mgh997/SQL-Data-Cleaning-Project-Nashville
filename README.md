# SQL-Data-Cleaning-Project

## Overview
This project shows data cleaning and transformation using SQL on a real estate dataset for Nashville. The goal was to prepare the data for analysis by standardizing dates, handling missing values, structuring address fields, cleaning categorical data, removing duplicates, and removing unnecessary columns.  

---

## Dataset
The dataset contains housing sale records with fields such as:

- `ParcelID` – Unique property identifier
- `PropertyAddress` – Full property address
- `OwnerAddress` – Owner’s address
- `SaleDate` – Date of property sale
- `SalePrice` – Sale price of the property
- `SoldAsVacant` – Indicator if the property was sold as vacant
- `LegalReference` – Legal property details
- Other related property and tax information

---

## Steps Performed

1. **Standardized Sale Date**
   - Converted inconsistent date formats into a uniform `DATE` type for consistency and analysis readiness.

2. **Filled Missing Property Addresses**
   - Used `JOIN` and `ISNULL` to populate missing addresses by matching records with the same `ParcelID`.

3. **Split Address Fields**
   - Separated `PropertyAddress` into `Street` and `City`.
   - Separated `OwnerAddress` into `Street`, `City`, and `State` for cleaner, structured data.

4. **Standardized Categorical Values**
   - Converted `Y`/`N` values in the `SoldAsVacant` column to `Yes`/`No` for better readability.

5. **Removed Duplicates**
   - Identified duplicate rows based on key property attributes and removed them to ensure clean analysis.

6. **Dropped Unnecessary Columns**
   - Removed redundant columns (`OwnerAddress`, `TaxDistrict`, `PropertyAddress`, `SaleDate`) to simplify the dataset.

---

## Key SQL Concepts Demonstrated
- `ALTER TABLE` and column creation
- `UPDATE` with `JOIN` and `ISNULL`
- String functions: `SUBSTRING`, `CHARINDEX`, `PARSENAME`
- Conditional updates using `CASE`
- Handling duplicates using `ROW_NUMBER()` and Common Table Expressions (CTEs)
- Cleaning and structuring real-world datasets

---

## How to Use
1. Clone this repository:  
   ```bash
   git clone https://github.com/mgh997/SQL-Data-Cleaning-Project.git

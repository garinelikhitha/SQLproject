# Nashville Housing Data Cleaning Project

## Overview
This project focuses on cleaning and transforming the Nashville Housing dataset using SQL. The dataset contains property sale records, including details like sale dates, property addresses, owner information, and sales prices. By applying various SQL data cleaning techniques, we improve the dataset's quality, making it more structured and suitable for analysis.

## Objectives
- Standardize date formats
- Populate missing property addresses
- Split address fields into separate columns (Address, City, State)
- Standardize categorical values (e.g., converting 'Y' and 'N' to 'Yes' and 'No')
- Remove duplicate records
- Delete unnecessary columns
- Demonstrate data import techniques using `OPENROWSET` and `BULK INSERT`

## Dataset
The dataset used in this project is `NashvilleHousing`, stored in the `PortfolioProject.dbo` schema.

## SQL Cleaning Steps
### 1. Standardizing Date Format
Converted the `SaleDate` column to a proper `Date` format using the `CONVERT` function. If direct updates failed, a new column `SaleDateConverted` was added to store the standardized values.

### 2. Populating Missing Property Addresses
Used self-joins on `ParcelID` to fill in missing `PropertyAddress` values by matching records with the same `ParcelID` but different `UniqueID` values.

### 3. Splitting Address into Individual Columns
Extracted `Address` and `City` from `PropertyAddress` using `SUBSTRING` and `CHARINDEX`. For `OwnerAddress`, used `PARSENAME` to separate `Address`, `City`, and `State` values.

### 4. Standardizing Categorical Data
Converted the `SoldAsVacant` field from 'Y' and 'N' to 'Yes' and 'No' using a `CASE` statement.

### 5. Removing Duplicates
Implemented `ROW_NUMBER()` with `PARTITION BY` to identify and remove duplicate records based on key attributes like `ParcelID`, `PropertyAddress`, `SalePrice`, `SaleDate`, and `LegalReference`.

### 6. Deleting Unused Columns
Dropped unnecessary columns such as `OwnerAddress`, `TaxDistrict`, `PropertyAddress`, and `SaleDate` to optimize the dataset.

## Tools & Technologies
- **SQL Server** (T-SQL)
- **SQL Server Management Studio (SSMS)**


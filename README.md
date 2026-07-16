# E-Commerce Order Data Analysis

## Description

This project analyzes an e-commerce orders dataset (1,200 records) covering order details, customer behavior, payment methods, referral sources, and sales trends. It walks through the full analytics workflow — from raw data cleaning to exploratory analysis, feature engineering, and SQL-based querying.

**What it covers:**
- **Data Cleaning** — inspecting structure, handling missing values, checking duplicates, and filtering/sorting records.
- **EDA & Feature Engineering** — monthly sales trends, outlier detection (IQR and Z-score methods), correlation analysis between numeric fields, and engineered features such as:
  - `LargeOrder` — flags orders with quantity ≥ 5
  - `CustomerOrderCount` — number of orders per customer
  - `CustomerLifetimeValue` — total spend per customer
  - `AvgCustomerOrderValue` — average order value per customer
  - `CustomerTotalItems` — total items purchased per customer
  - `IsWeekend` — flags whether an order was placed on a weekend
- **SQL Analysis** — the cleaned dataset is loaded into a SQLite database, then queried directly with SQL to answer business questions: top-selling products, revenue by product, order status breakdown, most common referral sources, average order value by payment method, and top revenue months.

## Dataset

`Dataset for Data Analytics.xlsx` — order-level e-commerce data with fields including `OrderID`, `Date`, `CustomerID`, `Product`, `Quantity`, `UnitPrice`, `ShippingAddress`, `PaymentMethod`, `OrderStatus`, `TrackingNumber`, `ItemsInCart`, `CouponCode`, `ReferralSource`, and `TotalPrice`.

## How to Run

1. Clone this repository and open `DecodeLabs_Project.ipynb` in Jupyter Notebook, JupyterLab, or Google Colab.
2. Install the required packages:
   ```bash
   pip install pandas numpy matplotlib scipy
   ```
3. Place `Dataset for Data Analytics.xlsx` in the same directory referenced in the notebook (or update the file path in the data-loading cell).
4. Run all cells in order, from top to bottom.

## Tech Stack

- Python (pandas, numpy, matplotlib, scipy)
- SQLite (via Python's built-in `sqlite3` module)
- Google Colab

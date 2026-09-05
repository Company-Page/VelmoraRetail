# VelmoraRetail
## Project
**Retail Billing & Inventory Assistant**

### `products.csv`
The Product Master. It contains 30 products across:
- Grocery
- Beverages
- Dairy
- Packaged Food
- Personal Care
- Household & Cleaning

Frozen columns:
`product_id, product_name, category, unit_price, stock_qty, reorder_level`

The dataset intentionally includes:
- normal stock
- stock below reorder level
- stock exactly at reorder level
- zero-stock products

### `sales_transactions.csv`
Contains historical sales transaction lines so the business environment is not blank on day one.

Frozen columns:
`transaction_id, transaction_date, product_id, product_name, quantity, unit_price, item_total`

New successful sales should be appended to this file.

### `starter_code.py`
A guided Python skeleton containing function placeholders and comments.

The learner must complete the business logic.

## Recommended Student Project Folder

```text
Velmora_Retail_Billing_Inventory/
├── retail_billing_inventory.py
├── products.csv
├── sales_transactions.csv
└── evidence/
```

Students may rename `starter_code.py` to `retail_billing_inventory.py` when they start development.

## Required Main Menu

1. View Products
2. Create Customer Bill
3. View Inventory
4. View Low-Stock Products
5. View Sales Summary
6. Exit

## Core Business Rules

- Product ID must exist before billing.
- Quantity must be a positive integer.
- Requested quantity cannot exceed current stock.
- Inventory must never become negative.
- Stock is reduced only after a successful sale.
- Item Total = Unit Price × Quantity.
- A product is low stock when `stock_qty <= reorder_level`.
- Successful sales only should be added to the transaction file.
- New transactions must be appended; old history must not be overwritten.
- Updated inventory must persist in `products.csv`.

## Technical Boundary

Use:
- Core Python
- `csv`
- `datetime`
- `os`
- Lists / Dictionaries
- Functions
- Loops
- Conditions
- `try / except`

Not required:
- pandas
- SQL
- Flask / Django / Streamlit
- GUI
- APIs
- cloud
- authentication
- machine learning

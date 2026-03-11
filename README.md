# Supermarket Sales Data Analysis

## Project Overview
This project explores retail sales data from a supermarket dataset to identify patterns in customer behaviour, product pricing, and revenue distribution. The analysis combines Python-based data analytics with SQL database storage to demonstrate a complete data analysis workflow.

## Objectives
- Clean and preprocess transactional retail data
- Store the processed dataset in a MySQL database
- Perform exploratory data analysis (EDA)
- Identify key sales trends and customer behaviour patterns
- Visualize insights using Python libraries

## Dataset Description

The dataset contains transactional records with the following attributes:

| Feature | Description |
|------|------|
| Invoice | Unique identifier for each transaction |
| StockCode | Unique product identifier |
| Description | Product name |
| Quantity | Number of items purchased |
| InvoiceDate | Date and time of purchase |
| Price | Price per unit |
| Customer ID | Unique customer identifier |
| Country | Customer location |

## Data Preprocessing

The following preprocessing steps were performed:

- Removed duplicate transactions
- Handled missing values in the dataset
- Removed cancelled orders
- Created a **Revenue column (Price × Quantity)**
- Extracted **month information** from transaction dates

## Database Storage

The cleaned dataset was stored in a **MySQL database** using SQLAlchemy.

Steps:
1. Create MySQL database `supermarket`
2. Connect Python to MySQL
3. Upload dataframe using `df.to_sql()`

Example code:

```python
df.to_sql("sales_data", con=engine, if_exists="replace", index=False)

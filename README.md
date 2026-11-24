# Ecommerce Transaction Analysis

## Project Overview

This project focuses on data inspection, data cleaning, preprocessing, and exploratory data analysis (EDA) using the **UCI Online Retail II Dataset**.

The project is developed using Python in Google Colab. It demonstrates practical data preparation techniques, numerical analysis using NumPy, data manipulation using Pandas, and data visualization using Matplotlib and Seaborn.

The analysis explores online retail transactions to understand product sales, revenue trends, customer purchasing behaviour, country-wise sales performance, and product returns.

## Dataset Information

- **Dataset Name:** Online Retail II
- **Source:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/502/online+retail+ii)
- **Format:** Excel (.xlsx)
- **Sheets:** Two Excel sheets combined into one DataFrame
- **Data Type:** Online retail transaction records

### Dataset Features

| Column | Description |
|---|---|
| Invoice | Invoice number identifying a transaction |
| StockCode | Unique product code |
| Description | Product description |
| Quantity | Number of items purchased or returned |
| InvoiceDate | Date and time of the transaction |
| Price | Unit price of the product |
| Customer ID | Unique customer identifier |
| Country | Customer's country |

### Additional Features Created

- **TransactionType:** Classifies transactions as Sale, Return, or Zero based on quantity.
- **TotalAmount:** Calculates transaction amount using Quantity × Price.
- **Month:** Extracts the month from InvoiceDate for monthly revenue analysis.

## Project Objectives

- Understand and inspect the dataset.
- Identify missing values and duplicate records.
- Clean and preprocess transaction data.
- Handle missing values and incorrect data types.
- Identify cancelled invoices and returned transactions.
- Perform numerical analysis using NumPy.
- Calculate transaction amounts and revenue.
- Analyze product sales performance.
- Explore customer purchasing behaviour.
- Analyze monthly and country-wise revenue.
- Visualize important patterns using Seaborn and Matplotlib.

## Tools and Technologies

| Tool / Library | Purpose |
|---|---|
| Python | Programming language |
| Google Colab | Development environment |
| Pandas | Data manipulation and cleaning |
| NumPy | Numerical operations and calculations |
| Matplotlib | Data visualization |
| Seaborn | Statistical data visualization |
| Requests | Downloading the dataset |
| Zipfile | Extracting the downloaded dataset |

## Project Workflow

### 1. Data Collection

- Download the Online Retail II dataset from the UCI Machine Learning Repository.
- Extract the downloaded ZIP file.
- Load both Excel sheets into Pandas DataFrames.
- Combine both sheets into a single DataFrame.

### 2. Data Inspection

- Check the total number of records and columns.
- Inspect column names and data types.
- Generate summary statistics.
- Identify missing values.
- Check duplicate records.
- Examine unique values and blank text values.
- Inspect negative, positive, and zero quantities.
- Examine negative and zero prices.
- Identify cancelled invoices.

### 3. Data Cleaning

- Remove duplicate records.
- Convert InvoiceDate into datetime format.
- Convert Quantity and Price into numeric data types.
- Convert Customer ID into a nullable integer type.
- Replace missing product descriptions with "Unknown".
- Remove records missing essential transaction fields.
- Clean text columns by removing unnecessary spaces.

### 4. Data Processing Using NumPy

- Convert Quantity and Price columns into NumPy arrays.
- Perform numerical calculations.
- Calculate sum, mean, median, minimum, maximum, and standard deviation of quantities.
- Classify transactions into Sale, Return, and Zero.
- Calculate transaction amounts using Quantity × Price.

### 5. Exploratory Data Analysis

- Analyze valid sales with positive quantities and prices.
- Calculate total revenue.
- Identify unique customers and products.
- Find the top 10 products by quantity sold.
- Analyze the top 10 countries by revenue.
- Examine monthly revenue trends.
- Identify the top 10 customers by revenue.
- Analyze the top 10 most returned products.

### 6. Data Visualization

- Create visualizations using Matplotlib and Seaborn.
- Display product sales performance.
- Visualize monthly revenue trends.
- Compare country-wise revenue.
- Explore customer revenue contribution.
- Analyze transaction types and product returns.
- Visualize sales quantity and product price distributions.
- Display missing values by column.

### 7. Final Data Quality Check

- Check remaining missing values.
- Verify duplicate records.
- Examine negative and zero quantities.
- Examine negative and zero prices.
- Generate a final data quality summary.
- Export the cleaned dataset as a CSV file.

## Project Visualizations

The following 9 visualizations were created using Seaborn and Matplotlib.

### 1. Missing Values by Column

Displays the number of missing values in each column to understand the data quality of the cleaned dataset.

![Missing Values by Column](Missing%20value%20by%20coloumn.png)

### 2. Monthly Retail Revenue Trend

Shows how retail revenue changes over time and helps identify monthly sales patterns.

![Monthly Retail Revenue Trend](Monthly%20retail%20revenue%20trend.png)

### 3. Product Price Distribution

Displays the distribution of product prices using a box plot with a logarithmic scale.

![Product Price Distribution](Product%20price%20distribution.png)

### 4. Sales Quantity Distribution

Shows the distribution of quantities per sale. The visualization uses data up to the 99th percentile to reduce the effect of extreme bulk orders on the displayed pattern.

![Sales Quantity Distribution](Sales%20quality%20distribution.png)

### 5. Top 10 Countries by Revenue

Compares the top 10 countries based on total revenue generated from valid sales.

![Top 10 Countries by Revenue](Top%2010%20countries%20by%20revenue.png)

### 6. Top 10 Customers by Revenue

Identifies the 10 customers who generated the highest total revenue.

![Top 10 Customers by Revenue](Top%2010%20customers%20by%20revenue.png)

### 7. Top 10 Products by Quantity Sold

Displays the 10 products with the highest total sales quantities.

![Top 10 Products by Quantity Sold](Top%2010%20product%20by%20Quantity%20sold.png)

### 8. Top 10 Most Returned Products

Highlights the products with the highest returned quantities based on negative transaction quantities.

![Top 10 Most Returned Products](top%2010%20most%20returned%20products.png)

### 9. Transaction Type Distribution

Shows the distribution of transactions classified as Sale, Return, and Zero.

![Transaction Type Distribution](Transaction%20type%20discription.png)

## Key Analysis Areas

**Sales Analysis**
- Product sales quantities.
- Total sales revenue.
- Top-selling products.

**Revenue Analysis**
- Monthly revenue trends.
- Country-wise revenue comparison.

**Customer Analysis**
- Top 10 customers by revenue.
- Customer purchasing patterns.

**Product Return Analysis**
- Returned transaction records.
- Total returned quantities.
- Top 10 most returned products.

**Data Quality Analysis**
- Missing values.
- Duplicate records.
- Negative and zero quantities.
- Negative and zero prices.

## How to Run the Project

1. Clone or download this repository.
2. Open `Ecommerce_Transaction_Analysis.ipynb` in Google Colab.
3. Run the notebook cells sequentially.
4. The notebook automatically downloads the Online Retail II dataset from the UCI repository.
5. The dataset is extracted and loaded into Pandas.
6. Complete the data cleaning and analysis steps.
7. The cleaned dataset is exported as `DataPrep_Cleaned_Transactions.csv`.

**Requirements:**
- Python
- Google Colab or Jupyter Notebook
- Internet connection to download the original dataset

## Project Structure

```text
Ecommerce-Transaction-Analysis/
│
├── Ecommerce_Transaction_Analysis.ipynb
│
├── README.md
│
├── Missing value by coloumn.png
├── Monthly retail revenue trend.png
├── Product price distribution.png
├── Sales quality distribution.png
├── Top 10 countries by revenue.png
├── Top 10 customers by revenue.png
├── Top 10 product by Quantity sold.png
├── Transaction type discription.png
└── top 10 most returned products.png
```

**Note:** The cleaned CSV file is generated when the notebook is executed and downloaded from Google Colab.

## Conclusion

This project demonstrates a practical data preparation and exploratory data analysis workflow using a real-world online retail transaction dataset.

Through Python, Pandas, NumPy, Matplotlib, and Seaborn, the project explores transaction records, handles missing values and duplicates, performs numerical calculations, analyzes revenue trends, and identifies customer and product performance patterns.

The project provides hands-on experience in:

- Data inspection and cleaning
- Data preprocessing
- Numerical analysis using NumPy
- Data manipulation using Pandas
- Exploratory Data Analysis (EDA)
- Data visualization using Matplotlib and Seaborn

## Author

**Ananya N. Puthran**

Data Analytics Project

**Technologies:** Python | Pandas | NumPy | Matplotlib | Seaborn | Google Colab

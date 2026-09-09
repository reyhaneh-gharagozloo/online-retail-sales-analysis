# 🛒 Online Retail Sales Analysis

## 📌 Project Overview

This project analyzes real-world online retail transaction data to discover sales trends, product performance, customer behavior, market performance, and time-based sales patterns.

The project uses **Python, Pandas, NumPy, and Matplotlib** for data cleaning, analysis, statistical analysis, and visualization.

---

## 🎯 Objectives

* Analyze overall sales performance
* Identify top-performing products
* Analyze customer purchasing behavior
* Compare sales performance across countries
* Identify high-performing days and hours
* Analyze revenue and quantity distributions
* Extract meaningful business insights from retail data

---

## 📊 Dataset

The dataset used in this project is the **Online Retail** dataset from the **UCI Machine Learning Repository**.

The original dataset contains **541,909 transaction records** and includes information about invoices, products, quantities, prices, customers, dates, and countries.

### 🔗 Dataset Source

**UCI Machine Learning Repository – Online Retail**

https://archive.ics.uci.edu/dataset/352/online+retail

**Dataset:** Online Retail
**Creator:** Daqing Chen
**DOI:** 10.24432/C5BW33
**License:** CC BY 4.0

---

## 📋 Dataset Features

| Column        | Description                      |
| ------------- | -------------------------------- |
| `InvoiceNo`   | Invoice / transaction number     |
| `StockCode`   | Product code                     |
| `Description` | Product description              |
| `Quantity`    | Quantity of products purchased   |
| `InvoiceDate` | Date and time of the transaction |
| `UnitPrice`   | Price per product                |
| `CustomerID`  | Customer identifier              |
| `Country`     | Customer's country               |

---

## 🧹 Data Cleaning

The dataset was cleaned before performing the main analysis.

The cleaning process included:

* Identifying cancelled transactions
* Removing cancelled transactions
* Removing records with non-positive quantities or prices
* Creating a `Revenue` column
* Removing exact duplicate transactions
* Identifying and handling extreme quantity outliers
* Preserving transactions with missing `CustomerID` for analyses where customer identification was not required

### Revenue Calculation

```python
Revenue = Quantity × UnitPrice
```

For customer-level analysis, only transactions with an available `CustomerID` were used.

---

## 📈 Sales Analysis

The project analyzes:

* Total revenue
* Total quantity sold
* Total orders
* Number of unique products
* Number of identifiable customers
* Average Order Value (AOV)
* Monthly revenue
* Monthly order volume
* Monthly AOV

The analysis also examines changes in sales performance throughout the available period.

---

## 🛍️ Product Analysis

Product-level analysis includes:

* Top products by revenue
* Top products by quantity
* Low-performing products
* Product prices
* Product sales volume

The analysis also excludes postage and manual service entries where appropriate.

---

## 👥 Customer Analysis

Customer-level analysis focuses on transactions with available `CustomerID`.

The analysis includes:

* Highest-value customers
* Most frequent customers
* Total revenue per customer
* Total quantity purchased per customer
* Number of orders per customer
* Average revenue per order for customers

This helps identify valuable and loyal customers.

---

## 🌍 Country Analysis

The project compares different markets based on:

* Number of customers
* Total revenue
* Number of orders
* Average Order Value

The analysis shows that the **United Kingdom is the dominant market by revenue**, while some international markets have considerably higher average order values despite having fewer orders.

---

## 🕒 Time Analysis

Time-based analysis was performed using:

* Year
* Month
* Day of Week
* Hour

The project investigates:

* Monthly revenue trends
* Revenue by day of week
* Revenue by hour

This helps identify periods with higher sales activity.

---

## 🔢 Statistical Analysis with NumPy

NumPy was used to investigate the statistical characteristics of the dataset.

The analysis includes:

* Mean
* Median
* Standard deviation
* Minimum and maximum values
* Percentiles
* Interquartile range (IQR)
* Revenue outlier analysis
* Customer revenue distribution
* Quantity statistics

The analysis shows that transaction revenue has a **right-skewed distribution**, meaning a relatively small number of high-value transactions have a significant effect on the overall revenue distribution.

---

## 📊 Data Visualization

Matplotlib was used to visualize the main findings.

The project includes visualizations for:

* Monthly Revenue Trend
* Top 10 Products by Revenue
* Top 10 Countries by Revenue
* Revenue by Day of Week
* Revenue Distribution

These visualizations make the main patterns and differences in the dataset easier to understand.

---

## 💡 Key Business Insights

Some of the main findings include:

* **November 2011** generated the highest monthly revenue and the highest number of orders.
* The **United Kingdom** generated the largest share of revenue.
* A relatively small group of customers generated a significant amount of revenue.
* Sales activity was concentrated during specific hours of the day.
* Revenue was strongly right-skewed because of a relatively small number of high-value transactions.
* Some products had very low sales volume and may require further investigation.
* Some international markets showed high Average Order Values despite having a much lower number of orders.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Matplotlib**
* **Jupyter Notebook**

---

## 📁 Project Structure

```text
online-retail-sales-analysis/
│
├── online-retail-sales-analysis.ipynb
├── README.md
├── requirements.txt
│
└── data/
    └── Online Retail.xlsx
```

---

## 🚀 Conclusion

This project demonstrates the use of Python for working with real-world retail transaction data.

It covers the complete workflow from **data exploration and cleaning to statistical analysis, visualization, and business insight generation**.

The project provided practical experience with **Pandas, NumPy, and Matplotlib** while applying data analysis techniques to a real retail dataset.

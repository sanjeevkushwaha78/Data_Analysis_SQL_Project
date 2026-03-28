

# 📊 Zepto SQL Data Analysis Project

## 📌 Project Overview

This project simulates how real-world **data analysts in the e-commerce and retail industry** work using SQL to analyze messy, real-world datasets.

The objective is to perform **data exploration, cleaning, and business analysis** on an e-commerce inventory dataset and extract meaningful insights that can support decision-making.

---

## 🎯 Objectives

* 🏗️ Design and set up an e-commerce inventory database
* 🔍 Perform Exploratory Data Analysis (EDA)
* 🧹 Clean and transform inconsistent data
* 📈 Generate business-driven insights using SQL

---

## 📁 Dataset Overview

The dataset is sourced from **Kaggle**, originally scraped from Zepto’s product listings.

It reflects real-world catalog behavior where:

* Products appear multiple times (different SKUs)
* Variations exist in weight, price, discounts, and packaging

👉 Each row represents a unique **SKU (Stock Keeping Unit)**

---

## 🧾 Table Schema

```sql
DROP TABLE IF EXISTS zepto_pro;

CREATE TABLE zepto_pro (
    sku_id INT IDENTITY(1,1) PRIMARY KEY,
    category VARCHAR(120),
    name VARCHAR(150) NOT NULL,
    mrp NUMERIC(8,2),
    discountPercent NUMERIC(5,2),
    availableQuantity INT,
    discountedSellingPrice NUMERIC(8,2),
    weightInGrm INT,
    outofStock BIT,
    quantity INT
);
```

---

## 📌 Column Description

| Column Name              | Description                        |
| ------------------------ | ---------------------------------- |
| `sku_id`                 | Unique identifier for each product |
| `name`                   | Product name                       |
| `category`               | Product category                   |
| `mrp`                    | Maximum Retail Price (₹)           |
| `discountPercent`        | Discount percentage                |
| `discountedSellingPrice` | Final selling price (₹)            |
| `availableQuantity`      | Available inventory units          |
| `weightInGrm`            | Product weight in grams            |
| `outOfStock`             | Stock status (1 = Yes, 0 = No)     |
| `quantity`               | Units per package                  |

---

## 🔧 Project Workflow

### 1️⃣ Database Setup

* Created structured table with proper data types
* Implemented `PRIMARY KEY` using `sku_id`

---

### 2️⃣ Data Import

* Imported dataset using **SQL Server Management Studio (SSMS)**
* Resolved encoding issues by converting dataset to **UTF-8**

---

### 3️⃣ 🔍 Exploratory Data Analysis (EDA)

* Counted total records
* Inspected sample data
* Identified NULL values
* Extracted distinct product categories
* Compared in-stock vs out-of-stock items
* Identified duplicate SKUs

---

### 4️⃣ 🧹 Data Cleaning

* Removed invalid rows (MRP or price = 0)
* Converted price from **paise → rupees**
* Ensured consistency in numeric columns

---

### 5️⃣ 📊 Business Insights

* 🔝 Top 10 highest discount products
* ❌ High-MRP products currently out of stock
* 💰 Estimated revenue by category
* 🛒 Expensive products with low discounts
* 📉 Top categories by average discount
* ⚖️ Price-per-gram analysis
* 📦 Product segmentation (Low / Medium / Bulk weight)
* 🏋️ Total inventory weight per category

---

## 🧠 SQL Concepts Used

* `SELECT`, `WHERE`, `ORDER BY`
* `GROUP BY`, `HAVING`
* Aggregate Functions (`SUM`, `AVG`, `COUNT`)
* `CASE` statements
* `CAST` for handling large values
* Data cleaning & transformation

---

## 🛠️ Tools & Technologies

* Microsoft SQL Server
* SQL Server Management Studio (SSMS)

---

## 🚀 How to Run the Project

1. Clone the repository:

```bash
git clone https://github.com/your-username/zepto-sql-project.git
```

2. Open `zepto_SQL_data_analysis.sql`
3. Create a database in SQL Server
4. Run the SQL script
5. Import dataset (ensure UTF-8 format)

---

## 📌 Key Learnings

* Working with real-world messy datasets
* Writing optimized SQL queries
* Performing EDA using SQL
* Data cleaning techniques
* Extracting business insights from raw data

---

## 📈 Future Improvements

* 📊 Build dashboards using Power BI / Tableau
* ⚡ Optimize performance with indexing
* 📦 Add stored procedures & automation

---

## 👨‍💻 Author

**Sanjeev Kushwaha**
Aspiring Data Analyst | SQL Enthusiast





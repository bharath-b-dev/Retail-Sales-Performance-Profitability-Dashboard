# Retail-Sales-Performance-Profitability-Dashboard

---

# 📊 Sales Data Analysis and Visualization Project

## 📌 Project Overview

This project demonstrates an end-to-end data analysis workflow using **Python, SQL, and Power BI**.

The objective is to transform raw sales data into meaningful business insights through:

* Data cleaning and preprocessing
* Structured database design
* Analytical SQL queries
* Interactive dashboard visualization

The system helps identify revenue trends, top-performing products, and regional performance patterns.

---

## 🎯 Objectives

* Clean and preprocess raw sales data
* Design relational database schema
* Perform data aggregation using SQL
* Build interactive Power BI dashboard
* Generate actionable business insights

---

## 🛠️ Technologies Used

| Tool                 | Purpose                        |
| -------------------- | ------------------------------ |
| Python               | Data cleaning & preprocessing  |
| Pandas               | Data manipulation              |
| Matplotlib & Seaborn | Data visualization             |
| SQL                  | Database management & analysis |
| Power BI             | Dashboard creation             |

---

## 📂 Project Structure

```
Sales-Data-Analysis/
│
├── data/
│   ├── raw_sales_data.csv
│   └── cleaned_sales_data.csv
│
├── python/
│   ├── data_cleaning.py
│   └── advanced_visualizations.py
│
├── sql/
│   ├── schema.sql
│   └── analysis_queries.sql
│
├── powerbi/
│   └── Sales_Dashboard.pbix
│
└── README.md
```

---

## 🔄 Project Workflow

1. Raw dataset collected
2. Data cleaned using Python
3. Cleaned data stored in SQL database
4. SQL queries performed for analysis
5. Data imported into Power BI
6. Interactive dashboard created

---

## 🧹 Data Cleaning Steps (Python)

* Removed duplicate records
* Handled missing values
* Converted date formats
* Created calculated column (TotalAmount = Quantity × UnitPrice)
* Standardized categorical values

Example:

```python
df.drop_duplicates(inplace=True)
df['TotalAmount'] = df['Quantity'] * df['UnitPrice']
```

---

## 🗄️ Database Design

### Sample Table Structure

```sql
CREATE TABLE Sales (
    OrderID INT PRIMARY KEY,
    OrderDate DATE,
    Region VARCHAR(50),
    Category VARCHAR(50),
    ProductName VARCHAR(100),
    Quantity INT,
    UnitPrice DECIMAL(10,2),
    TotalAmount DECIMAL(10,2)
);
```

### Sample Analysis Queries

**Total Revenue**

```sql
SELECT SUM(TotalAmount) AS TotalRevenue FROM Sales;
```

**Revenue by Region**

```sql
SELECT Region, SUM(TotalAmount) 
FROM Sales
GROUP BY Region;
```

---

## 📈 Advanced Python Visualizations

* Correlation Heatmap
* Sales Distribution Histogram
* Monthly Sales Trend Line Plot
* Category-wise Revenue Comparison

These visualizations were used for exploratory data analysis before dashboard creation.

---

## 📊 Power BI Dashboard Features

* KPI Cards (Total Revenue, Orders, Quantity)
* Revenue by Region (Bar Chart)
* Monthly Sales Trend (Line Chart)
* Top Products (Bar Chart)
* Category Distribution (Pie Chart)
* Interactive Slicers (Region, Category, Date)

---

## 🔍 Key Insights

* A small number of products contribute the majority of revenue
* Sales vary significantly across regions
* Monthly trends indicate seasonal patterns
* Category performance differs in contribution

---

## 🚀 Future Enhancements

* Sales forecasting using Machine Learning
* Real-time database integration
* Web-based deployment
* Automated reporting system



## 📌 Conclusion

This project demonstrates a complete data analysis pipeline from raw data preprocessing to interactive business intelligence reporting. It highlights how Python, SQL, and Power BI can be integrated effectively for decision support systems.

on (one paragraph)**

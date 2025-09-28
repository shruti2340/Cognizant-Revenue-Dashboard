<img width="1308" height="746" alt="Screenshot 2025-09-28 131650" src="https://github.com/user-attachments/assets/996516d6-77db-4a2d-939f-1ff8a5b1ae47" />
# Cognizant Revenue Dashboard

This repository contains a Power BI project that analyzes **revenue trends and performance** using the **Cognizant Artificial Intelligence Kaggle dataset**.  
The dashboard provides a clear and interactive way to explore **total revenue, customer types, product categories, and payment methods**.

---

## 📊 Project Overview
The purpose of this dashboard is to help visualize revenue insights for decision-making.  
It highlights how different **customer types (Gold, Premium, Standard, Basic)** and **payment modes (Cash, Debit Card, E-Wallet)** contribute to the overall revenue.

---

## 🚀 Features of the Dashboard
- **KPI Cards**  
  - Total Revenue  
  - Total Transactions  
  - Total Quantity Sold  
  - Average Unit Price  

- **Revenue Analysis**  
  - Revenue by Customer Type  
  - Revenue by Payment Method  
  - Revenue by Product Category  

- **Trend Visuals**  
  - Revenue over Time (Date/Month)  
  - Transactions Trend  

- **Other Visuals**  
  - Bar/Column Charts  
  - Pie/Donut Charts   

---

## 🛠️ Tools & Technologies Used
- **Power BI Desktop** – for creating visuals and reports  
- **DAX (Data Analysis Expressions)** – to build custom measures  
- **Kaggle Dataset** – for source data  

---

## 📂 Files in this Repository
- `Cognizant_Revenue_Dashboard.pbix` → Power BI file with complete dashboard  
- `cognizant_dataset.csv` → Source dataset from Kaggle  
- `screenshot1.png`, `screenshot2.png` → Dashboard preview images  
- `README.md` → Project documentation  

---

## 📈 Key DAX Measures
Some of the DAX measures created in the dashboard:

```DAX
Total_Quantity = SUM(COGNIZANT[quantity])

Total_Transactions = COUNT(COGNIZANT[transaction_id])

Average_Unit_Price = AVERAGE(COGNIZANT[unit_price])

Gold_Revenue = CALCULATE(SUM(COGNIZANT[total]), COGNIZANT[customer_type] = "gold")

Premium_Transactions = CALCULATE(COUNT(COGNIZANT[transaction_id]), COGNIZANT[customer_type] = "premium")

Ewallet_Revenue = CALCULATE(SUM(COGNIZANT[total]), COGNIZANT[payment_type] = "e-wallet")

DebitCard_Revenue = CALCULATE(SUM(COGNIZANT[total]), COGNIZANT[payment_type] = "debit card")

Cash_Revenue = CALCULATE(SUM(COGNIZANT[total]), COGNIZANT[payment_type] = "cash")


# Mobile-Sales-Dashboard-PowerBI
“Power BI Mobile Sales Dashboard analyzing brand-wise performance, customer behavior, and payment methods using CSV data.”
# Mobile-Sales-Dashboard-PowerBI

## 📌 Project Overview
This project is a **Mobile Sales Power BI Dashboard** built using CSV data of smartphone transactions.  
The dashboard provides a complete view of sales performance by **brand, city, mobile model, day, and payment method**, along with customer ratings.

It is designed for business stakeholders to quickly understand:
- Which brands and models are performing best  
- Which cities are generating maximum revenue  
- How customers are paying  
- How daily and weekly patterns impact sales  

---

## 📁 Files Included
| File Name                  | Description                          |
|---------------------------|--------------------------------------|
| `Mobile_Sales_Dashboard.pbix` | Main Power BI report file           |
| `Mobile_Sales_Data.csv`       | Raw transactional data (CSV)       |
| `dashboard.png`               | Main dashboard screenshot           |
| `README.md`                   | Project documentation               |

*(Agar tumhari CSV ka naam abhi kuch aur hai, to GitHub par rename karke yeh naam rakh sakte ho.)*

---

## 📊 Dashboard Preview
![Dashboard Preview](dashboard.png)

---

## 🚀 Key Features of the Dashboard
- 📌 **Top KPIs** at a glance  
  - Total Sales  
  - Total Quantity Sold  
  - Number of Transactions  
  - Average Sales per Transaction  
- 🗺 **Total Sales by City** (Map visual)
- 📆 **Total Quantity by Day** (daily trend)
- ⭐ **Customer Ratings Distribution**
- 💳 **Transactions by Payment Method** (UPI, Debit Card, Credit Card, Cash)
- 🏷 **Brand-wise Sales & Quantity** (Apple, Samsung, Vivo, Xiaomi, OnePlus, etc.)
- 📱 **Total Sales by Mobile Model**
- 📅 **Total Sales by Day Name** (Monday–Sunday pattern)
- 📅 **Month Slicer** on the left panel to quickly switch between months

---

## 🔧 Tools & Techniques Used
- **Power BI Desktop**
- **Power Query** – for data cleaning & transformation  
- **DAX** – for calculated measures & KPIs  
- **Map Visuals** – to show city-wise performance  
- **Custom Formatting & Theming** – branded layout (Motorola styling)  

---

## 🧮 Sample DAX Measures

```DAX
Total Sales = SUM(MobileSales[Total_Amount])

Total Quantity = SUM(MobileSales[Units Sold])

Total Transactions = DISTINCTCOUNT(MobileSales[Transaction ID])

Average Sales per Transaction = DIVIDE([Total Sales], [Total Transactions])

5 Star Rating Count = CALCULATE(COUNTROWS(MobileSales), MobileSales[Customer Ratings] = 5)

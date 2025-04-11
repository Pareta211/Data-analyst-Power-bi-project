# Maven Market Data analysis - (Interactive multi page dashboard creation using Power BI)


---

## 🚀 Key Features

- 📅 Monthly, Quarterly, and Yearly Sales Trends
- 💰 Total Sales, Profit, Quantity, and Discount Metrics
- 🧍 Customer Segmentation & Repeat Rate
- 📦 Top Products & Categories by Revenue
- 🌍 Region-wise Performance Breakdown
- 📈 Dynamic filters & slicers for interactivity

---

## 🧠 Key Insights

- West Region consistently performed best across years
- Office Supplies were the top-selling product category
- Discount strategy needed review as high discounts didn’t always lead to higher sales
- Repeat customers contributed significantly to revenue growth

---

## 🔍 DAX Measures Used

```DAX
Total Sales = SUM(Orders[Sales])

Total Profit = SUM(Orders[Profit])

Profit Margin = DIVIDE([Total Profit], [Total Sales])

Top Customer = RANKX(ALL(Orders[Customer Name]), [Total Sales], , DESC)

Sales YoY Growth = 
VAR CurrentYear = YEAR(MAX(Orders[Order Date]))
VAR PrevYearSales = CALCULATE([Total Sales], YEAR(Orders[Order Date]) = CurrentYear - 1)
RETURN DIVIDE([Total Sales] - PrevYearSales, PrevYearSales)

Customer Insights:

Top Customer: Ida Rodriguez — $2.24K revenue from 290 orders.
8,842 unique customers | $200 revenue per customer.
Most customers are low- and average-income earners, with professionals and skilled manual workers forming key segments.

![Screenshot 2025-03-04 022521](https://github.com/user-attachments/assets/2b43cf03-02ab-481d-a2b5-4e2e5ad30a1d)
![Screenshot 2025-03-04 022537](https://github.com/user-attachments/assets/82ccc281-e5a8-4dc2-8e32-74e07bc2ac15)
![Screenshot 2025-03-04 022629](https://github.com/user-attachments/assets/a83d5f98-a150-4e49-9487-7bb3e8157486)




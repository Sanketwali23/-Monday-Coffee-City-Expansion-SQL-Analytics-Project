# ☕ Monday Coffee — City Expansion SQL Analytics Project

> **"Data-driven decisions over guesswork — because every great cup of coffee deserves the perfect city."**

---

## 🚀 Project Overview

**Monday Coffee** is a data analytics project that leverages the power of **SQL Server** to analyze coffee sales data across multiple Indian cities and answer one burning question:

> ### 🏙️ *Where should Monday Coffee open its next stores?*

This project digs deep into real sales data — revenue trends, customer behavior, rent costs, and market size — to deliver **actionable, profitable expansion recommendations** backed entirely by data.

---

## 🎯 Business Objective

The company was flying blind. Without understanding:
- 📊 How large is the coffee market in each city?
- 💸 Which cities generate the most revenue?
- 👥 Where are our best customers?
- 🏠 Is the rent actually worth it?

...expansion decisions were pure **guesswork**.

This project changes that.

---

## 🔍 10 Business Questions Answered

| # | Question | Technique Used |
|---|----------|---------------|
| 1 | 📈 Estimated coffee consumers per city | Population × 25% estimation |
| 2 | 💰 Total revenue — Q4 2023 | `JOIN` + `WHERE` + date filtering |
| 3 | 🛒 Units sold per product | `GROUP BY` + `COUNT` |
| 4 | 👤 Average sales per customer per city | Aggregations + formatting |
| 5 | 🏘️ Population vs actual customers | Multi-table `JOIN` |
| 6 | 🏆 Top 3 products per city | `DENSE_RANK()` + CTE |
| 7 | 🎯 Unique customers per city | `COUNT DISTINCT` |
| 8 | ⚖️ Avg sales vs avg rent per customer | Dual CTE comparison |
| 9 | 📉 Monthly sales growth rate | `LAG()` window function |
| 10 | 🥇 Final top 3 cities recommendation | Full business summary |

---

## 🧠 SQL Concepts Used

```sql
✅ CTEs (Common Table Expressions)
✅ Window Functions — LAG(), DENSE_RANK()
✅ Multi-table JOINs (3-4 tables)
✅ Aggregate Functions — SUM(), COUNT(), AVG()
✅ Date Functions — YEAR(), MONTH(), DATEPART()
✅ FORMAT() for currency & number display
✅ Subqueries & derived metrics
✅ PARTITION BY for city-level ranking
```

---

## 🏆 Final City Recommendations

After analyzing revenue, customer spend, rent cost, and market size — here are the **top 3 cities** for expansion:

---

### 🥇 City 1 — Pune
> **"The revenue king with room to grow"**

- 🔥 **Highest revenue** across all cities
- 💰 Strong average spend per customer
- 🏠 Moderate, manageable rent
- 📊 Solid and growing customer base

---

### 🥈 City 2 — Chennai
> **"Balanced, profitable, and steady"**

- 💵 **Second highest revenue** city
- 📊 Strong and loyal customer base
- 🏠 Rent is well within profitable range
- ⚖️ Excellent balance between earnings and cost

---

### 🥉 City 3 — Jaipur
> **"The efficiency champion"**

- 👥 **Highest customer count** (69 unique customers)
- 💸 **Lowest rent per customer** — best unit economics
- 📈 Strong revenue relative to operating cost
- ⚖️ Most cost-efficient city in the dataset

---

## ❌ Cities Ruled Out

### 🚫 Bangalore
- 🏠 Rent is **too high**
- Average rent per customer is the **highest** in the dataset
- Serious **profit margin risk** — not worth it yet

### 🚫 Delhi
- 🌆 Huge market size — looks attractive on paper
- But revenue per customer is **lower than expected**
- Rent is relatively high for the return it offers

---

## 📁 Project Structure

```
📦 monday-coffee-sql-project/
 ┣ 📄 SQLQuery1.sql        ← All 10 business queries with annotations
 ┣ 📄 README.md            ← You are here!
 ┗ 📊 (Dataset tables: city, customers, products, sales)
```

---

## 🗄️ Database Schema

```
city         → city_id, city_name, population, estimated_rent
customers    → customer_id, customer_name, city_id
products     → product_id, product_name
sales        → sale_id, customer_id, product_id, total, sale_date
```

---

## ⚡ Key Highlights

- 🔎 **10 end-to-end business queries** — from raw data to final recommendation
- 📅 **Time-series analysis** — monthly growth trends using `LAG()` window function
- 🏙️ **City-level ranking** — top 3 products per city using `DENSE_RANK()`
- 💡 **Business context** included for every query — not just SQL, but *why it matters*
- 🇮🇳 **India-specific formatting** — currency formatted in `en-IN` locale

---

## 🛠️ Tools & Tech

![SQL Server](https://img.shields.io/badge/SQL%20Server-CC2927?style=for-the-badge&logo=microsoft-sql-server&logoColor=white)
![T-SQL](https://img.shields.io/badge/T--SQL-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)

- **Database:** Microsoft SQL Server
- **Language:** T-SQL (Transact-SQL)
- **Techniques:** Window Functions, CTEs, Multi-table JOINs, Aggregations

---

## 💡 What Makes This Project Stand Out

Unlike surface-level SQL projects, this one ties every query back to a **real business problem**:

> Every query answers *"So what?"* — not just "here's the data" but **"here's what to do with it."**

The final recommendation doesn't just pick the city with the highest sales. It weighs **revenue vs rent vs customer reach vs market potential** — just like a real business analyst would.

---

## 🤝 Connect & Contribute

Found a better query? Have suggestions for deeper analysis?

⭐ **Star this repo** if you found it useful!
🍴 **Fork it** and build on top of it!
📬 Open an **Issue** or **Pull Request** anytime

---

> *"Without data, you're just another person with an opinion."* — W. Edwards Deming ☕

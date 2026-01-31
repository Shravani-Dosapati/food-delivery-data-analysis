# Food Delivery Data Integration & Analysis

## 📌 Project Overview
This project demonstrates how to integrate and analyze data coming from **multiple real-world data sources and formats** (CSV, JSON, and SQL).  
The goal is to create a **single source of truth dataset** for analysis and answer business-oriented questions related to food delivery operations.

The project was completed as part of a data internship assessment.

---

## 📂 Datasets Used

| File Name | Format | Description |
|---------|--------|-------------|
| `orders.csv` | CSV | Transactional order data |
| `users.json` | JSON | User master data (city, membership type, etc.) |
| `restaurants.sql` | SQL | Restaurant master data (cuisine, rating, etc.) |

---

## 🔗 Join Logic Used

The datasets were merged using **LEFT JOINs** to ensure that **all orders are retained**.

- `orders.user_id` → `users.user_id`
- `orders.restaurant_id` → `restaurants.restaurant_id`

This approach preserves transactional integrity and avoids loss of order records.

---

## 🛠️ Technologies & Libraries
- Python
- Pandas
- SQLite (`sqlite3`)
- Jupyter Notebook

---

## ⚙️ Data Integration Steps

1. Loaded transactional data from CSV
2. Loaded user master data from JSON
3. Executed SQL script into an in-memory SQLite database
4. Extracted restaurant data into Pandas
5. Performed LEFT JOINs using `pandas.merge()`
6. Generated a consolidated dataset:
   - `final_food_delivery_dataset.csv`

---

## 📊 Final Dataset Details
- **Rows:** 10,000  
- **Columns:** Order details, user information, and restaurant attributes  
- This dataset is used as the **only source of truth** for all analysis questions.

---

## 📈 Analysis Performed
The final dataset was used to answer analytical questions such as:
- Revenue analysis by city and membership type
- Cuisine-wise performance
- Order trends and seasonality
- Impact of Gold vs Regular membership
- High-value restaurants and customer behavior

All analysis is documented inside the Jupyter Notebook.

---

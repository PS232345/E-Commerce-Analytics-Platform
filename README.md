# E-Commerce Sales Analytics Dashboard

A Flask-based web dashboard visualizing e-commerce sales performance — revenue trends, top products, top customer states, and category breakdowns — mirroring KPIs from a companion Power BI report.

![Python](https://img.shields.io/badge/Python-3.11-blue)
![Flask](https://img.shields.io/badge/Built%20with-Flask-black)
![License](https://img.shields.io/badge/License-MIT-lightgrey)
<img width="1920" height="968" alt="Screenshot (98)" src="https://github.com/user-attachments/assets/4e3fcaa3-4b7d-4656-bfdc-d876a185db19" />



---

## 📌 Overview

This project presents key e-commerce business metrics through a Flask web application, backed by pre-aggregated CSV datasets (revenue by month, top products, customer analysis, and category analysis). The dashboard's KPIs are kept in sync with a corresponding Power BI report, so both tools tell the same story.

---

## ✨ Features

- **KPI Cards** — Total Revenue, Total Orders, Total Customers, Average Order Value
- **Revenue Trend** — Monthly revenue chart data
- **Top 5 Products** — Ranked by revenue
- **Top 5 States** — Customer distribution and revenue by state
- **Top 5 Categories** — Category-wise revenue breakdown
- Server-rendered dashboard using Flask + Jinja templates

---

## 🗂️ Data

The app reads from four pre-processed CSV files (generated from the source e-commerce dataset via a separate analysis/ETL step):

| File | Description |
|---|---|
| `monthly_revenue.csv` | Revenue aggregated by month |
| `top_products.csv` | Product-level revenue data |
| `customer_analysis.csv` | Customer/state-level revenue data |
| `category_analysis.csv` | Category-level revenue data |

> Source dataset: Brazilian E-Commerce (Olist) public dataset — 99,441 orders, ~96,100 customers, ~$20.47M total revenue.

---

## 🛠️ Tech Stack

| Category | Tools |
|---|---|
| Language | Python 3.11 |
| Backend | Flask |
| Templating | Jinja2 |
| Data Handling | pandas |
| Frontend | HTML/CSS + Chart.js (via `index.html`) |
| BI Companion | Power BI |

---

## 📊 Key Metrics

| Metric | Value |
|---|---|
| Total Revenue | $20.47M |
| Total Orders | 99.44K |
| Total Customers | 96.10K |
| Avg Order Value | $205.86 |

---

## 📁 Project Structure

```
E-Commerce Sales Analytics Dashboard/
│
├── app.py                       # Flask application
├── templates/
│   └── index.html               # dashboard template
├── static/                      # CSS/JS/assets (if any)
├── monthly_revenue.csv
├── top_products.csv
├── customer_analysis.csv
├── category_analysis.csv
├── E-Commerce Sales Dashboard.pbix   # companion Power BI report
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

```bash
# Clone the repository
git clone https://github.com/<your-username>/ecommerce-sales-dashboard.git
cd ecommerce-sales-dashboard

# Create a virtual environment
python -m venv .venv
.venv\Scripts\activate      # Windows
source .venv/bin/activate   # macOS/Linux

# Install dependencies
pip install -r requirements.txt
```

### requirements.txt
```
flask
pandas
```

---

## ▶️ Usage

1. Ensure `monthly_revenue.csv`, `top_products.csv`, `customer_analysis.csv`, and `category_analysis.csv` are in the project root.
2. Run the app:
   ```bash
   python app.py
   ```
3. Open `http://127.0.0.1:5000/` in your browser to view the dashboard.

---

## 🚀 Future Improvements

- Move hardcoded KPI values into dynamic calculations from the CSVs
- Add date-range and category filters to the dashboard
- Add a REST API layer for external data access
- Deploy to a cloud host (Render/Heroku/Azure)
- Add authentication for internal business use

---

## 👤 Author

**Prachi Sable**
B.E. Artificial Intelligence & Data Science, GSMCOE, Pune

---

## 📄 License

This project is licensed under the MIT License.

# 📊 SalesIQ — Sales & Revenue Analytics Dashboard

> A production-grade, fully interactive sales analytics dashboard built with vanilla HTML, CSS & JavaScript. No build tools or frameworks required — just open `index.html`.

![Dashboard Preview](https://img.shields.io/badge/Status-Live-brightgreen) ![Data Rows](https://img.shields.io/badge/Dataset-1200%2B%20Rows-blue) ![Charts](https://img.shields.io/badge/Charts-8%20Interactive-purple) ![License](https://img.shields.io/badge/License-MIT-orange)

## ✨ Features

### 📈 KPI Tracking (5 Key Metrics)
| Metric | Description |
|--------|-------------|
| 💰 Total Revenue | Sum of all sales revenue |
| 📈 Total Profit | Net profit after costs |
| 📦 Total Orders | Order count |
| 🎯 Profit Margin | Profit as % of revenue |
| ⭐ Avg Customer Rating | Average order satisfaction score |

### 📊 8 Interactive Charts
| Chart | Type | Insight |
|-------|------|---------|
| Revenue & Profit Trend | Line (Monthly/Quarterly toggle) | Revenue over time |
| Revenue by Category | Doughnut | Category performance split |
| Top 10 Products | Horizontal Bar (Revenue/Profit toggle) | Best sellers |
| Revenue by Region | Polar Area | Geographic breakdown |
| Sales by Channel | Bar | Online vs Retail vs Wholesale etc |
| Salesperson Performance | Mixed Bar + Line | Team leaderboard |
| Discount vs Revenue Impact | Mixed Bar + Line | Pricing strategy insight |

### 🔍 Filters & Slicers
- **Year** — 2023 / 2024 / All
- **Category** — 10 product categories
- **Region** — 5 global regions
- **Channel** — 5 sales channels
- **Status** — Completed / Refunded / Pending
- **Reset** — One-click filter reset

### 📁 Data Import / Export
- 📂 **Import** any CSV file via drag & drop or file picker
- ⬇ **Export** filtered data as CSV (timestamped filename)
- 🗃 Bundled dataset: `data/sales_data.csv` (1,200 rows)

### 📋 Data Table
- Full transaction table with 13 columns
- Live search across all fields
- Click-to-sort on any column
- Paginated (20 rows/page) with navigation

---

## 📁 Project Structure

```
sales-dashboard/
├── index.html              ← Main dashboard (single file app)
├── data/
│   └── sales_data.csv      ← 1,200-row dataset (importable to Excel/DB)
├── generate_data.js        ← Node.js script to regenerate dataset
└── README.md               ← This file
```

---

## 🗃️ Dataset Schema

**File:** `data/sales_data.csv` — **1,200 rows** | **15 columns**

| Column | Type | Description |
|--------|------|-------------|
| Order ID | String | Unique order identifier (ORD-00001…) |
| Date | Date | Transaction date (2023–2024) |
| Category | String | Product category (10 categories) |
| Product | String | Product name |
| Region | String | Geographic region (5 regions) |
| Salesperson | String | Sales rep name (10 reps) |
| Channel | String | Sales channel (5 channels) |
| Quantity | Integer | Units sold |
| Unit Price | Float | Price per unit ($) |
| Discount (%) | Integer | Discount applied (0–20%) |
| Revenue | Float | Qty × Unit Price × (1 - Disc%) |
| Cost | Float | Cost of goods sold |
| Profit | Float | Revenue − Cost |
| Status | String | Completed / Refunded / Pending |
| Customer Rating | Float | 2.5–5.0 stars |

### Data Dimensions
- **Categories:** Electronics, Clothing, Home & Garden, Sports, Books, Beauty, Toys, Food & Beverage, Automotive, Office Supplies
- **Regions:** North America, Europe, Asia Pacific, Latin America, Middle East
- **Channels:** Online, Retail Store, Wholesale, Direct Sales, Partner
- **Salespersons:** 10 named reps
- **Date Range:** Jan 2023 – Dec 2024

---

## 🔧 How to Use

### Option 1: Direct Open
```bash
# Just double-click index.html — no setup needed!
```

### Option 2: Local Server (recommended for CSV auto-load)
```bash
# Python
python -m http.server 8000

# Node.js
npx serve .

# Then visit: http://localhost:8000
```

### Option 3: GitHub Pages (free hosting)
1. Push to GitHub
2. Go to `Settings → Pages`
3. Source: `main` branch, `/ (root)`
4. Your dashboard is live at `https://username.github.io/repo-name`

### Option 4: Regenerate Dataset
```bash
node generate_data.js
# Outputs: data/sales_data.csv (1200 rows)
```

---

## 📥 Importing Your Own Data

The dashboard accepts any CSV with these columns (column names must match exactly):

```
Order ID, Date, Category, Product, Region, Salesperson, Channel,
Quantity, Unit Price, Discount (%), Revenue, Cost, Profit, Status, Customer Rating
```

Click **📂 Import CSV/Data** to load your own file.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|------------|---------|
| HTML5 / CSS3 | Structure & styling |
| Vanilla JavaScript (ES6+) | All logic & interactivity |
| [Chart.js 4.4](https://www.chartjs.org/) | All 8 charts |
| [PapaParse 5.4](https://www.papaparse.com/) | CSV parsing |
| Google Fonts (Space Grotesk + Syne) | Typography |

**Zero dependencies to install. Zero build step.**

---

## 🎨 Design

- **Theme:** Dark mode with electric blue/teal/coral accent palette
- **Grid:** CSS Grid & Flexbox responsive layout
- **Animations:** CSS transitions, Chart.js animations, loading screen
- **Responsive:** Works on mobile, tablet, desktop

---

## 📊 Use Cases

- 🎓 **Academic projects** — Data visualization, business analytics coursework
- 💼 **Portfolio** — Showcase frontend + data skills on GitHub/LinkedIn
- 📈 **Business** — Adapt with real data for actual sales tracking
- 🔬 **Learning** — Study Chart.js, CSV parsing, dashboard architecture

---

## 🚀 Extending the Dashboard

Ideas to make it your own:
- Connect to a real database (MySQL/PostgreSQL) via a backend API
- Add date range picker (start/end date slicers)
- Add Excel (.xlsx) export using SheetJS
- Deploy with a Node.js/Express backend + SQLite database
- Add user authentication and role-based views

---

## 📄 License

MIT License — free to use, modify, and distribute.

---

## 👨‍💻 Author

Built as part of a Design Thinking & Innovation (DTI) project — B.Tech CSE, 2024–2025.

---

⭐ **If you found this useful, please star the repo!**

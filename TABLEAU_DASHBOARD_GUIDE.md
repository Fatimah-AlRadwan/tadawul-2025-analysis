# Tableau Dashboard Guide — Tadawul 2025
## Files to connect in Tableau
Load all 4 CSV files from `/data` folder:
- `tableau_sector_daily.csv` → rename to **Sector Daily**
- `tableau_index_daily.csv` → rename to **Index Daily**
- `tableau_size_daily.csv` → rename to **Size Daily**
- `tableau_sector_summary.csv` → rename to **Sector Summary**

---

## Dashboard Structure: 4 Sheets + 1 Dashboard

### Sheet 1 — TASI Trend Line
- **Data source:** Index Daily (filter: Index contains "TASI")
- **Chart type:** Line chart
- Columns: `Date` (continuous)
- Rows: `Close`
- Add reference line at average
- Color: #1A6E9C
- Title: "TASI Performance 2025"

### Sheet 2 — Sector Performance Bar Chart
- **Data source:** Sector Summary
- **Chart type:** Horizontal bar chart
- Rows: `Sector`
- Columns: `Price Change Pct`
- Color: Use diverging Red-Green on `Price Change Pct` (center = 0)
- Sort: Descending by Price Change Pct
- Title: "Sector Price Performance 2025 (%)"

### Sheet 3 — Sector Liquidity Treemap
- **Data source:** Sector Summary
- **Chart type:** Treemap
- Size: `Total Value Traded SAR`
- Color: `Price Change Pct` (diverging Red-Green)
- Label: `Sector` + `Total Value Traded SAR` (formatted in Billions)
- Title: "Market Liquidity by Sector (Value Traded SAR)"

### Sheet 4 — Monthly Activity Bar Chart
- **Data source:** Sector Daily
- **Chart type:** Bar chart
- Columns: `Month`
- Rows: SUM(`Value Traded (SAR)`)
- Format Y-axis in Billions
- Color: #1A6E9C
- Add average reference line
- Title: "Monthly Trading Activity 2025"

### Sheet 5 — Cap Size Volatility
- **Data source:** Size Daily
- **Chart type:** Dual-axis (Line + Bar)
- Line: `Close` by `Date`, colored by `Size`
- Use colors: Large=#1A6E9C, Mid=#F4A623, Small=#d9534f
- Title: "Market Cap Performance Comparison 2025"

---

## Dashboard Layout (1200 × 800px)

```
┌─────────────────────────────────────────────────────────┐
│  TADAWUL 2025 — Saudi Stock Market Dashboard            │
│  Subtitle: Full-year analysis | Source: Tadawul.com     │
├───────────────────────────┬─────────────────────────────┤
│                           │                             │
│   Sheet 1: TASI Trend     │   Sheet 3: Treemap          │
│   (top left, wide)        │   (top right)               │
│                           │                             │
├─────────────┬─────────────┴──────────┬──────────────────┤
│             │                        │                  │
│ Sheet 2:    │  Sheet 4: Monthly      │  Sheet 5:        │
│ Sector Bars │  Activity              │  Cap Size        │
│             │                        │                  │
└─────────────┴────────────────────────┴──────────────────┘
```

## KPI Tiles to add (text boxes or calculated fields)
- **TASI Annual Return:** -13.1%
- **Most Liquid Sector:** Banks — SAR 240.8B
- **Top Performer:** Pharma +98.5%
- **Total Market Value Traded:** SAR ~1.3T

## Filters to add (as dashboard filter cards)
- Sector (multi-select)
- Quarter (buttons: Q1 / Q2 / Q3 / Q4)

## Publishing
1. File → Save to Tableau Public
2. Copy the public link
3. Add the link to your GitHub README

# 📈 Tadawul 2025 — Saudi Stock Market Analysis

**Author:** Fatimah Alradwan  
**Date:** April 2026  
**Status:** In Progress

---

## Overview
End-to-end data analysis of the Saudi Stock Exchange (Tadawul) for the full year 2025, covering 22 market sectors, the TASI benchmark index, and market cap segments. Data was extracted directly from the official Tadawul website.

## Business Questions Answered
1. How did the TASI perform across 2025 — trends and turning points?
2. Which sectors generated the most trading value (liquidity leaders)?
3. Which sectors had the best and worst price performance?
4. How does volatility differ across Large, Mid, and Small Cap stocks?
5. Which months had the highest market activity?
6. Which sectors had the highest number of trades (retail activity)?
7. Is there a correlation between trading volume and price performance?

## Key Findings
| Finding | Detail |
|---------|--------|
| TASI Annual Return | **-13.1%** (12,077 → 10,491) |
| Sectors with positive returns | **2 out of 22** |
| Top performing sector | **Pharma +98.5%** |
| Worst performing sector | **Media & Entertainment -49.4%** |
| Most liquid sector | **Banks — SAR 240.8B** |
| Most active month | **January 2025** |
| Highest retail activity | **Basic Materials** |

## Tools Used
- **Python** (pandas, matplotlib, seaborn) — cleaning & analysis
- **Jupyter Notebook** — development environment (VSCode)
- **Tableau Public** — interactive dashboard

## Project Structure
```
tadawul-2025-analysis/
├── data/
│   ├── Tadawul_2025.xlsx          # Raw: sector daily data
│   ├── Indices_2025.xlsx          # Raw: index daily data
│   ├── Size_2025.xlsx             # Raw: market cap daily data
│   ├── clean_sector.csv           # Cleaned sector data
│   ├── clean_index.csv            # Cleaned index data
│   ├── clean_size.csv             # Cleaned size data
│   ├── tableau_sector_daily.csv   # Tableau ready
│   ├── tableau_index_daily.csv    # Tableau ready
│   ├── tableau_size_daily.csv     # Tableau ready
│   └── tableau_sector_summary.csv # Tableau ready (summary)
├── images/
│   └── q1_tasi_trend.png
│   └── q2_sector_liquidity.png
│   └── q3_sector_performance.png
│   └── q4_size_volatility.png
│   └── q5_monthly_activity.png
│   └── q6_sector_trades.png
│   └── q7_volume_vs_performance.png
├── notebooks/
│   └── Tadawul_2025_Analysis.ipynb
├── README.md
```

## Dashboard
🔗 [View Tableau Dashboard](https://public.tableau.com/views/Tadawul2025SaudiStockMarketAnalysis/TadawulDashboard?:language=en-US&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)  

## Data Source
All data extracted from the official [Tadawul website](https://www.saudiexchange.sa) — Saudi Exchange.

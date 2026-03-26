# EDA Roadmap — English Premier League 2023/24
**By:** Youssef Moussa
**Dataset:** EPL 2023/24 Match Stats

---

## Progress Overview

| Stage | Name | Status |
|-------|------|--------|
| 1 | Setup & First Look | ✅ Done |
| 2 | Data Cleaning | ✅ Done |
| 3 | Univariate Analysis | ✅ Done |
| 4 | Bivariate Analysis | 🔄 Next |
| 5 | Multivariate Analysis | ⏳ Pending |
| 6 | Team-Level Analysis | ⏳ Pending |
| 7 | Time-Based Analysis | ⏳ Pending |
| 8 | Key Insights & Summary | ⏳ Pending |

---

## Stage Descriptions

### ✅ Stage 1 — Setup & First Look
- Import libraries
- Load dataset
- Inspect shape, dtypes, and sample rows
- Statistical summary
- Missing values check

### ✅ Stage 2 — Data Cleaning
- Drop useless columns (zero-variance, fully null)
- Fix Date dtype
- Add engineered columns (GD, Rest_Days)
- Validate data ranges (Poss)
- Handle missing values (Attendance)
- Check for duplicates

### ✅ Stage 3 — Univariate Analysis
- Distribution of Goals Scored (`GF`)
- Match Results breakdown (`Result`)
- Possession distribution (`Poss`)
- Shots on Target distribution (`SoT`)
- Rest Days distribution (`Rest_Days`)
- Summary statistics table (Mean, Median, Std, Skewness)

### 🔄 Stage 4 — Bivariate Analysis
- How do two variables relate to each other?
- Examples:
  - Does more possession lead to more wins?
  - Does more rest lead to better performance?
  - Does SoT correlate with GF?

### ⏳ Stage 5 — Multivariate Analysis
- Correlation heatmaps
- Pair plots
- Multiple variables analyzed together

### ⏳ Stage 6 — Team-Level Analysis
- Team by team breakdown
- Which teams dominate which metrics?
- Home vs Away performance per team

### ⏳ Stage 7 — Time-Based Analysis
- Performance trends across the season
- Do teams improve or decline over time?
- Impact of fixture congestion on performance

### ⏳ Stage 8 — Key Insights & Summary
- Consolidate all findings
- Write clean, presentation-ready insights
- Prepare conclusions for the final report

---

*Last updated: March 2026*

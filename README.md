# 🏴󠁧󠁢󠁥󠁮󠁧󠁿 English Premier League 2023/24 — Exploratory Data Analysis

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-150458?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-3.7+-11557c)
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)

---

## 📋 Table of Contents
- [Project Overview](#-project-overview)
- [Dataset Description](#-dataset-description)
- [Project Structure](#-project-structure)
- [EDA Stages](#-eda-stages)
- [Key Findings](#-key-findings)
- [How to Run](#-how-to-run)
- [Author](#-author)

---

## 📌 Project Overview

This project performs an end-to-end **Exploratory Data Analysis (EDA)** on the English Premier League 2023/24 season match statistics. The goal is to understand team performance patterns, match result distributions, and key metrics across the full season — laying the groundwork for future predictive modeling.

---

## 📂 Dataset Description

| Property | Details |
|----------|---------|
| **Source** | [Kaggle — English Premier League Matches 2023/2024 Season](https://www.kaggle.com/datasets/mertbayraktar/english-premier-league-matches-20232024-season) |
| **Rows** | 760 (one row = one team's performance per match) |
| **Columns** | 28 (raw) → 25 (after cleaning) |
| **Coverage** | All 380 EPL matches across the 2023/24 season |

**Key Columns:**

| Column | Description |
|--------|-------------|
| `Team` | Team name |
| `Date` | Match date |
| `Venue` | Home or Away |
| `Result` | W / D / L |
| `GF` | Goals scored |
| `GA` | Goals conceded |
| `GD` | Goal difference (engineered) |
| `Poss` | Possession percentage |
| `SoT` | Shots on target |
| `Attendance` | Stadium attendance |
| `Rest_Days` | Days since last match (engineered) |

> **Note:** The dataset uses one row per team per match. A single fixture (e.g. Man City vs Arsenal) appears as **two separate rows** — one for each team.

---

## 📁 Project Structure

```
📁 epl-eda-2024/
├── 📓 eda_2024.ipynb        ← Main analysis notebook
├── 📄 project_stages.md     ← Full EDA roadmap (all 8 stages)
├── 📄 README.md             ← You are here
└── 📄 .gitignore
```

> `matches.csv` is excluded from the repository via `.gitignore`.  
> Download the dataset from Kaggle and place it in the root directory before running the notebook.

---

## 📊 EDA Stages

### ✅ Stage 1 — Setup & First Look
- Loaded dataset and inspected shape, dtypes, and sample rows
- Identified missing values (`Notes` fully null, `Attendance` partially null)
- Generated statistical summary — confirmed `Poss` mean = 50.0

### ✅ Stage 2 — Data Cleaning
- Dropped 5 useless columns (zero-variance or fully null)
- Converted `Date` to datetime
- Engineered `GD` (Goal Difference) and `Rest_Days` columns
- Validated `Poss` range (0–100%), no impossible values found
- Filled `Attendance` nulls using each team's median (not global mean)
- Confirmed no duplicate rows

### ✅ Stage 3 — Univariate Analysis
- **Goals Scored (`GF`):** Right-skewed — most matches end with 1–2 goals; rare high-scoring outliers (up to 8)
- **Match Results (`Result`):** Wins and losses are equal by definition (298 each); draws are least common (164)
- **Possession (`Poss`):** Perfectly symmetrical around 50% — mean and median both = 50.0
- **Shots on Target (`SoT`):** Right-skewed — typical range is 3–5; some matches recorded 0
- **Rest Days (`Rest_Days`):** Most common window is 7–9 days; 20+ day gaps due to international breaks

### ⏳ Stage 4 — Bivariate Analysis *(coming soon)*
### ⏳ Stage 5 — Multivariate Analysis *(coming soon)*
### ⏳ Stage 6 — Team-Level Analysis *(coming soon)*
### ⏳ Stage 7 — Time-Based Analysis *(coming soon)*
### ⏳ Stage 8 — Key Insights & Summary *(coming soon)*

---

## 🔍 Key Findings

> *(Updated as analysis progresses)*

- Most EPL matches end with **1–2 goals per team** — high-scoring matches are rare outliers
- **Possession is balanced** across the league — no team consistently dominates the ball
- Teams typically rest **7–9 days** between matches, with congested periods dropping to 3–5 days
- **Draws are the least common** result — the EPL tends to produce decisive outcomes

---

## ▶️ How to Run

1. Clone the repository
```bash
git clone https://github.com/theyoussefmoussa/epl_2024.git
cd epl_2024
```

2. Install dependencies
```bash
pip install pandas numpy matplotlib seaborn jupyter
```

3. Download the dataset from [Kaggle](https://www.kaggle.com/datasets/mertbayraktar/english-premier-league-matches-20232024-season) and place `matches.csv` in the root directory

4. Launch the notebook
```bash
jupyter notebook eda_2024.ipynb
```

---

## 👤 Author

**Youssef Moussa**
Data Science Student — EDA Project | March 2026

# acc102-firm-size-profitability-analysis
Do small firms really earn higher returns? An empirical analysis of U.S. firms (2024) comparing ROA across size groups using WRDS Compustat data.
## Overview
This project investigates the relationship between firm size (market capitalization) and profitability (return on assets, ROA) using 2024 U.S. public company data from WRDS Compustat. The analysis challenges the common heuristic that "small firms are more profitable."

**Research Question**: Are small firms more profitable than large firms? We compare mean and median ROA across three size groups (Small, Medium, Large).

**Target Audience**: Beginner investors and financial analysis learners who want to understand the role of firm size in stock selection.


## Key Findings
| Size Group | Mean ROA | Median ROA | Std Dev | Count |
|------------|----------|------------|---------|-------|
| Large      | 3.28%    | 3.77%      | 0.112   | 2,108 |
| Medium     | -5.88%   | 0.60%      | 0.200   | 2,107 |
| Small      | -18.37%  | -9.11%     | 0.288   | 2,108 |

**Main conclusions:**
- Large firms have significantly higher average ROA (3.28%) than small firms (-18.37%).
- More than half of small firms reported a loss in 2024 (median ROA = -9.11%).
- Profitability is much more dispersed among small firms (std dev 0.288 vs. 0.112 for large firms), indicating higher investment risk.


## Repository Structure
firm-size-profitability-analysis

- firm-size-profitability2471401.ipynb   # Complete Python analysis (data fetch, cleaning, grouping, visualization)
- requirements.txt        # Python dependencies
- roa_mean_std_with_bar.png       # Mean and std ROA by size group
- roa_median.png         #  Median ROA by size group
- README.md               # Project documentation (this file)

## Data Source

- **Database:** WRDS Compustat – Fundamentals Annual (`comp.funda`)
- **Access Date:** April 12, 2026
- **Sample:** 6,323 U.S. firms with fiscal year 2024
- **Filters applied:**
  - Industrial firms (`indfmt='INDL'`)
  - Standard format (`datafmt='STD'`)
  - Annual reports (`popsrc='D'`)
  - Consolidated statements (`consol='C'`)
  - Positive total assets (`at > 0`)
  - Non-missing net income (`ni IS NOT NULL`)
  - Valid market capitalization (`mkvalt > 0` OR `csho * prcc_f > 0`)

> **Citation:** Data were obtained from the Wharton Research Data Services (WRDS), specifically the Compustat North America - Fundamentals Annual database.

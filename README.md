# CAMEL Model Analysis — Vikas Souharda Co-operative Bank (FY2021–FY2025)

A five-year supervisory-framework assessment of a co-operative bank's financial health using the CAMEL model (Capital Adequacy, Asset Quality, Management, Earnings, Liquidity), built during my finance internship at the bank.

## Overview
- **Scope:** FY2020-21 to FY2024-25 annual reports (5 years of primary-source data)
- **Framework:** CAMEL with formula-driven composite scoring in Excel + Power BI
- **Output:** Excel scoring workbook + Power BI dashboard + interactive HTML visualization

## Key Finding — RBI Inspection Divergence

**The headline:** In FY2022-23, the RBI inspection assessed Gross NPA at **9.3%** versus the bank's reported **1.83%** — a divergence of **7.47 percentage points**. This was the most material finding of the analysis.

Under stress scenario (applying RBI-assessed NPA), the composite score deteriorates from 2.10 (Satisfactory) to 3.10 (Fair).

## Dashboard Preview

### Power BI Dashboard
![CAMEL Dashboard Overview](camel_dashboard_screenshot.png)

*Interactive features:* KPI cards, CAMEL pillar heatmap (5-year trend), composite score trend line with grade bands, stress-test spotlight, detailed pillar metrics.

### Interactive HTML Version
👉 [View live dashboard here](CAMEL_Dashboard_Interactive.html)

Full dashboard in a single HTML file (no build required). Open in any browser or embed in your portfolio site.

## Repository Contents

| File | Purpose |
|---|---|
| `CAMEL_Model_VikasSouharda_5yr.xlsx` | Original Excel workbook with all scoring, inputs, formulas, and stress-test tab |
| `CAMEL_PowerBI_Import.xlsx` | Clean star-schema import file (Fact_CAMEL, Dim_Pillar, Dim_Year, Stress_Test tables) |
| `CAMEL_Dashboard.pbix` | Power BI Desktop model with 6 measures (Composite Score, Grade, YoY Change, Latest, Weakest Pillar, NPA Divergence) |
| `CAMEL_Dashboard_Interactive.html` | Standalone interactive dashboard (fully styled, no dependencies beyond CDN) |
| `README.md` | This file |

## Methodology

**CAMEL Framework:**
- **C (Capital Adequacy):** CRAR %; target ≥15% for rating 1
- **A (Asset Quality):** Gross NPA %; lower is better (target <2% for rating 1)
- **M (Management):** Cost-to-Income ratio; lower is better (target <45% for rating 1)
- **E (Earnings):** ROA %; higher is better (target ≥1.5% for rating 1)
- **L (Liquidity):** Credit-Deposit ratio; target <60% for rating 1

**Composite Scoring:**
- Each pillar rated 1–5 (1=Strong, 5=Unsatisfactory)
- Weights: C=0.20, A=0.25, M=0.15, E=0.20, L=0.20
- Composite Score = weighted average
- Grade mapping: 1–1.5=Strong, 1.5–2.5=Satisfactory, 2.5–3.5=Fair, 3.5–4.5=Marginal, 4.5–5=Unsatisfactory

## 5-Year Summary

| FY | Composite Score | Grade | Trend |
|---|---|---|---|
| FY2020-21 | 2.95 | Fair | — |
| FY2021-22 | 2.35 | Satisfactory | ✓ Improved |
| FY2022-23 | 2.10 | Satisfactory | ✓ Improved (best year) |
| FY2023-24 | 2.55 | Fair | ⚠️ Deteriorated |
| FY2024-25 | 2.75 | Fair | ⚠️ Continued deterioration |

**Trend Analysis:**
- Best: FY2022-23 (2.10) — lowest composite score despite RBI NPA divergence finding
- Worst: FY2024-25 (2.75) — deterioration driven by elevated Asset Quality and Management scores
- Weakest pillar across period: **Management** (Cost-to-Income consistently high at 72–74%)
- Strength: **Liquidity** (consistently adequate; CD ratio in comfortable 60–67% band)

## Key Insights

1. **Capital Adequacy is strong** — CRAR improved from 12.3% (FY21) to 14.68% (FY25), consistently above regulatory minimum.

2. **Asset Quality deteriorated significantly post-FY23** — Reported Gross NPA was 1.83% in FY23 (all-time low), but RBI inspection findings (~9.3%) suggested underreporting. Gross NPA then rose to 4.29% (FY24) and 4.86% (FY25), indicating either better recognition or genuine deterioration.

3. **Management efficiency is a persistent drag** — Cost-to-Income ratio remains elevated at 72.2% (FY25), reflecting operational inefficiencies. This is the primary driver of the Marginal (4) management rating.

4. **Earnings are stable but low** — ROA hovering around 0.8–0.9%, typical for a co-operative bank but a constraint on organic capital generation.

5. **Liquidity position is comfortable** — CD ratio in 60–67% band throughout, no liquidity stress.

## Skills Demonstrated

- **Ratio analysis & banking norms** — RBI CAMEL framework, regulatory capital requirements (CRAR), NPA definitions
- **Financial data extraction** — reading and extracting metrics from audited annual reports (balance sheet, P&L, notes to accounts)
- **Excel financial modeling** — formula-driven scoring, stress-test sensitivity, multi-year comparative analysis
- **Power BI data modeling** — star schema design, DAX measures (SWITCH, CALCULATE, FILTER, VAR), calculated columns
- **Data visualization** — professional dashboard design, heatmaps, trend analysis, visual storytelling
- **Supervisory analysis** — understanding RBI inspection findings, identifying divergences, stress-testing balance sheets

## Author

**Kedarnath H**  
MBA Finance | Financial Analyst | [LinkedIn](https://www.linkedin.com/in/mrkedar) | [GitHub](https://github.com/Kedarnath-H)

## Source & Verification

- Vikas Souharda Co-operative Bank Ltd. Annual Reports: FY2020-21 to FY2024-25 (audited, filed with Registrar of Co-operative Societies & RBI)
- RBI Inspection Report: FY2022-23 findings on NPA divergence (reference: Bank's Board Minutes, public disclosures)
- All calculations verified against primary source documents

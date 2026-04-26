# Saudi Aramco — DCF Intrinsic Valuation Model
### Ticker: 2222.SR &nbsp;|&nbsp; Currency: USD Millions &nbsp;|&nbsp; Version: v1.0 &nbsp;|&nbsp; April 2026

> **⚠️ Disclaimer:** This model is built for educational and portfolio purposes only. It does not constitute investment advice. All projections are estimates based on publicly available information and analyst assumptions.

---

## 📌 Investment Recommendation

| Metric | Value |
|---|---|
| **Recommendation** | 🔴 SELL / UNDERPERFORM |
| **GGM Price Target** | $3.93 / share |
| **Exit Multiple Price Target** | $3.82 / share |
| **Market Price (Apr 2026)** | $6.24 / share |
| **Implied Downside** | **−37.8%** |

---

## 📁 Repository Contents

```
Aramco_DCF_Intrinsic_Valuation_v1.0.xlsx
```

A single-file, fully formula-driven Excel workbook with 8 structured sheets. Every projection cell references the centralised `3_Assumptions` tab — zero hardcoded values outside of it.

---

## 🗂️ Model Structure

| Sheet | Description |
|---|---|
| `Cover` | Summary dashboard — recommendation, price targets, model map |
| `1_HistoricalIS` | Five-year income statement · FY2021–FY2025 · Revenue → EBITDA → Net Income |
| `2_HistoricalCF` | Five-year cash flow · CFO, CapEx (negative), FCF build, Brent crude reference |
| `3_Assumptions` | **Single source of truth** · Oil price path, margins, WACC inputs, terminal value drivers |
| `4_WACC` | CAPM cost of equity · after-tax cost of debt · blended WACC = **7.57%** |
| `5_Projections` | Five-year unlevered FCF build · FY2026E–FY2030E · all cells formula-driven |
| `6_DCF` | PV of FCFs · terminal value (GGM + EV/EBITDA multiple) · equity bridge · price targets |
| `7_Sensitivity` | Three color-scaled tables: WACC × Brent · Multiple × Brent · g × Brent |
| `8_Output` | Football field chart · KPI strip · investment recommendation summary |

---

## 📊 Key Model Outputs

### Valuation Summary

| Method | Enterprise Value ($M) | Price Target (USD/share) |
|---|---|---|
| Gordon Growth Model (GGM) | $992,645 | **$3.93** |
| Exit EV/EBITDA Multiple | $965,939 | **$3.82** |

### WACC Build

| Component | Value |
|---|---|
| Risk-Free Rate (Rf) | 4.29% · FRED DGS10, April 2026 |
| Beta (β) | 0.69 · Yahoo Finance 2222.SR |
| Equity Risk Premium (ERP) | 5.30% · Damodaran 2025 (US 4.6% + Saudi CRP 0.7%) |
| **Cost of Equity (Ke)** | **7.95%** |
| Pre-Tax Cost of Debt (Kd) | 3.25% · Finance Costs / Avg Debt |
| After-Tax Cost of Debt | 1.66% |
| Debt Weight (D/V) | 5.97% |
| Equity Weight (E/V) | 94.03% |
| **Blended WACC** | **7.57%** |

### Five-Year Projections Snapshot (USD Millions)

| Metric | FY2026E | FY2027E | FY2028E | FY2029E | FY2030E |
|---|---|---|---|---|---|
| Brent ($/bbl) | $92 | $80 | $75 | $73 | $72 |
| Revenue | 491,648 | 427,520 | 400,800 | 390,112 | 384,768 |
| EBITDA | 211,409 | 183,834 | 172,344 | 167,748 | 165,450 |
| Unlevered FCF | 63,177 | 54,937 | 51,503 | 50,130 | 49,443 |

---

## ⚙️ Key Assumptions

### Oil Price Path
FY2026 assumes **$92/bbl** reflecting a Hormuz disruption scenario. FY2027–FY2030 normalises gradually to the EIA long-run estimate of **$72/bbl**.

### Margin & Cost Assumptions
| Assumption | Value | Basis |
|---|---|---|
| EBITDA Margin | 43.0% | Above FY2025 actual (39.4%) reflecting higher FY2026 oil; historical median 46.6% |
| D&A % of Revenue | 5.8% | Five-year average FY2021–FY2025 |
| CapEx % of Revenue | 11.5% | Reflects $50–55B guidance through 2028; FY2024–25 actuals 11.5%–12.2% |
| ΔNW C % of Revenue | 0.5% | Conservative positive drag (best-practice conservatism) |
| Effective Tax Rate | 48.79% | Five-year median ETR |

### Terminal Value
| Assumption | Value | Basis |
|---|---|---|
| Terminal Growth Rate (g) | 3.0% | Long-run nominal GDP growth; constrained: g < WACC and g < Rf |
| Exit EV/EBITDA Multiple | 6.5× | Integrated oil major peer median (ExxonMobil, Shell, TotalEnergies, BP) |
| TV / EV (GGM) | 77.9% | Within target range of 60%–80% ✅ |
| TV / EV (Multiple) | 77.3% | Within target range of 60%–80% ✅ |

---

## 📈 Historical Performance Snapshot (USD Millions)

| Metric | FY2021 | FY2022 | FY2023 | FY2024 | FY2025 | 5-Yr Median |
|---|---|---|---|---|---|---|
| Revenue | 359,181 | 535,188 | 440,875 | 436,613 | 415,824 | 436,613 |
| EBITDA | 228,649 | 329,518 | 257,421 | 234,090 | 213,310 | 234,090 |
| Net Income | 109,972 | 161,068 | 121,271 | 106,246 | 93,389 | 109,972 |
| Free Cash Flow | 107,455 | 148,531 | 101,202 | 85,333 | 85,428 | 101,202 |
| EBITDA Margin | 63.7% | 61.6% | 58.4% | 53.6% | 51.3% | 58.4% |
| FCF Margin | 29.9% | 27.8% | 23.0% | 19.5% | 20.5% | 23.0% |

---

## 📉 Sensitivity Analysis

Three two-way sensitivity tables in `7_Sensitivity`, color-scaled from bull to bear:

- **WACC × Brent** — price target impact of discount rate vs. oil price
- **Exit Multiple × Brent** — peer multiple vs. oil price
- **Terminal Growth Rate (g) × Brent** — perpetuity growth vs. oil price

---

## 🗃️ Data Sources

| Source | Usage |
|---|---|
| Saudi Aramco Annual Reports FY2021–FY2025 | Income statement, cash flow, balance sheet inputs |
| FRED Series DGS10 (April 2026) | Risk-free rate (10-Year US Treasury yield) |
| Damodaran Country Risk Premiums 2025 | US base ERP (4.6%) + Saudi CRP (0.7%) |
| EIA Short-Term Energy Outlook (April 2026) | Long-run Brent crude oil price forecast ($72/bbl) |
| Yahoo Finance — 2222.SR (April 2026) | Beta (0.69), current market price ($6.24/share) |

---

## 👤 Author

**Uzair Kareem Bakhsh**  
April 2026 · Portfolio Release v1.0

---

*This model is for educational and portfolio showcase purposes only. It does not constitute financial or investment advice. All projections involve uncertainty and are subject to change.*

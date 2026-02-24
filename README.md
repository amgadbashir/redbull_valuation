# Red Bull GmbH — Valuation & M&A Analysis

> A fully integrated investment banking model covering intrinsic valuation, relative valuation, synergy analysis, M&A accretion / dilution, and leveraged buyout analysis for Red Bull GmbH.

---

## Overview

This Excel-based financial model was built from scratch following institutional IB conventions. It values Red Bull GmbH, a privately held company with no publicly filed financials, using multiple methodologies and consolidates the outputs into a football field valuation summary. The model then extends into buy-side analysis: synergy valuation, a full M&A accretion / dilution framework (with Coca-Cola as the illustrative acquirer), and an LBO with sponsor return sensitivity.

**Analyst:** Amgad Bashir  
**Currency:** EUR / USD (as noted per tab)  
**Units:** Millions  

---

## Model Structure

| # | Tab | Description |
|---|-----|-------------|
| 1 | **Red Bull Model** | Fully integrated 3-statement forecast (IS / BS / CF) with assumptions, PP&E schedule, equity rollforward, interest circularity, and operating statistics |
| 2 | **WACC** | Bottom-up WACC build: unlevered beta from public comps, re-levered to Red Bull's target capital structure, with cost of debt from credit spread analysis |
| 3 | **DCF** | Discounted cash flow valuation using unlevered FCF, Gordon Growth terminal value, and 3 sensitivity tables (EV, EBITDA multiple, terminal multiple vs. WACC and LTG) |
| 4 | **Trading Comps** | Public company comparable analysis across 8 beverage peers with EV / Revenue, EV / EBITDA, EV / EBIT, P/E, and growth / margin benchmarking |
| 5 | **1 / 2 / 3** | Individual company tearsheets for Coca-Cola, Keurig Dr Pepper, and Monster Beverage — key data, EV bridge, and financial summary |
| 6 | **Transaction Comps** | 20 precedent beverage transactions with EV / Revenue and EV / EBITDA multiples; shortlist of 4 most comparable deals |
| 7 | **Valuation Summary** | Football field consolidating all valuation approaches into min–max ranges with a visual chart |
| 8 | **Synergies** | Synergy valuation using a DCF approach with phased realisation (20% → 50% → 100%) and a perpetuity terminal value |
| 9 | **M&A** | Full accretion / dilution analysis with Coca-Cola as acquirer — includes sources & uses, pro-forma EPS, sensitivity tables (EV multiple × equity mix), leverage analysis, P/E analysis, ROIC vs. WACC, and ownership dilution |
| 10 | **LBO** | Leveraged buyout model with senior debt / unsecured notes waterfall, cash sweep, sponsor equity returns (IRR), and sensitivity table (entry multiple × exit year) |

---

## Key Modelling Features

### Three-Statement Model
- Regional revenue build (Europe, USA, Americas ex-USA, Rest of World) with individual growth assumptions
- Margin-driven expense forecasting (COGS, SG&A, marketing as % of revenue)
- Working capital modelled on days outstanding (AR, inventory, AP) and % of revenue
- PP&E schedule (beginning → capex → depreciation → ending)
- Equity rollforward (beginning → net income → dividends → ending)
- Circular interest calculation with a binary switch (`Circswitch`) to toggle on/off
- Balance sheet check row to verify Assets = Liabilities + Equity

### Valuation
- **DCF:** Mid-year convention, Gordon Growth terminal value, implied terminal EBITDA multiple cross-check
- **Trading comps:** Full longlist (8 companies) filtered to a 3-company shortlist; multiples include EV/Revenue, EV/EBITDA, EV/EBIT, EV/EBITDAR, EV/EBITR, and P/E
- **Transaction comps:** 20 deals sourced from public filings and financial databases; implied multiples for deals without reported EBITDA derived using Red Bull's own margin
- **Sensitivity tables:** Two-variable data tables throughout (WACC vs. LTG, entry multiple vs. equity mix, entry multiple vs. exit year)

### M&A Analysis
- Sources and uses of funds with configurable equity / debt mix
- Pro-forma income statement combination with phased synergy realisation
- EPS accretion / dilution across CY1, CY2, CY3 with breakeven synergy calculation
- Dual sensitivity grid: EV / EBITDA multiple × equity financing % for both fixed EV and variable EV scenarios
- Leverage ratio analysis (net debt / EBITDA) pre- and post-deal
- P/E analysis: acquirer P/E vs. debt P/E vs. acquisition P/E
- Return on invested capital vs. WACC comparison
- Implied standalone value (purchase price less synergy value)

### LBO
- Capital structure: senior secured debt (4× EBITDA) + unsecured notes (2× EBITDA) + equity
- Mandatory debt repayment waterfall with cash sweep
- Debt paydown tracking (% of total debt repaid)
- Sponsor equity IRR calculation
- Sensitivity: IRR across entry multiples (11× – 30×) and exit years (3 – 6)

---

## Formatting Conventions

The model follows standard investment banking colour-coding:

| Colour | Meaning |
|--------|---------|
| 🔵 Blue font, light blue background | Input cell — hardcoded assumption (editable) |
| 🔵 Blue font, white background | Hardcoded value — historical or sourced data |
| ⚫ Black font | Formula / calculation |
| 🟢 Green font, grey background | Cross-sheet link |
| 🟡 Yellow background | Key assumption — review required |

Negative numbers are shown in parentheses. Currency values are formatted as `$#,##0` and percentages as `0.0%`. Years are formatted as text to avoid comma separation.

---

## How to Use

1. **Download** the `.xlsx` file and open in Excel (desktop recommended for data tables and circular references)
2. **Start on the Info tab** — review the table of contents, model details, and colour legend
3. **Assumptions are in blue** — adjust projected growth rates, margins, and working capital assumptions in the Red Bull Model tab (columns I–P) to run your own scenarios
4. **Toggle the circular switch** (`Info!N10`) between 0 and 1 to enable/disable circular interest calculations
5. **Sensitivity tables** use Excel's built-in Data Table feature — they update automatically when assumptions change
6. **Follow the flow:** Red Bull Model → WACC → DCF → Comps → Valuation Summary → Synergies → M&A → LBO

---

## Data Sources & Limitations

- Red Bull is privately held and does not publicly file detailed financials. Revenue figures for FY2024 and FY2025 are sourced from Red Bull's public disclosures; regional breakdowns and cost structure are estimated based on prior-year proportions
- Comparable company market data (share prices, market caps) are sourced from public exchanges and financial databases
- Precedent transactions are sourced from public deal announcements and financial databases
- Beta, credit ratings, and EPS estimates are sourced from publicly available data
- This model is for **educational and demonstration purposes only** and does not constitute investment advice

---

## Built With

- Microsoft Excel (`.xlsx`)
- No VBA or macros — the model is fully formula-driven
- Data tables for two-variable sensitivity analysis
- Named ranges for readability (`WACC`, `ltg`, `Circswitch`, `FX`)

---

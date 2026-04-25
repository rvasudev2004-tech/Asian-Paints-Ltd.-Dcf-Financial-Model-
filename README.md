# ASIAN_PAINTS_VALUATION_ENGINE_V2

## PROJECT_DOCUMENTATION
This repository contains a high-fidelity fundamental analysis and intrinsic valuation framework for Asian Paints Ltd. The engine utilizes a three-stage Discounted Cash Flow (DCF) methodology to derive equity value independent of market volatility, integrating multi-year historical normalization with forward-looking risk assessments.

### ANALYTICAL_ARCHITECTURE
- **Valuation Methodology:** Free Cash Flow to Firm (FCFF) utilizing a 5-year explicit forecast horizon and a terminal value stage based on the perpetuity growth model.
- **WACC Framework:** Weighted Average Cost of Capital calculated at **13.91%**, derived from a bottom-up levered beta approach, a risk-free rate ($Rf$) of 6.93%, and localized equity risk premiums.
- **Intrinsic Growth Engine:** Forecasting is driven by the fundamental relationship between **ROIC (Return on Invested Capital)** and the **Reinvestment Rate**, ensuring growth projections are mathematically constrained by capital allocation efficiency.
- **Equity Bridge Logic:** Enterprise Value (EV) is adjusted for a complex debt stack (including lease liabilities under Ind AS 116) and cash equivalents to arrive at a precise net equity value per share.

---

## QUANTIFIABLE_ANALYSIS_READING

* **INTRINSIC_VALUATION_GAP:** The model identifies a significant variance between fundamental support and market pricing. The calculated intrinsic value of **INR 622.19** per share, when mapped against the current market price of **INR 2,514**, reveals a **75.25% valuation gap**. This quantifies a market premium of **4.04x** over the base-case fundamental value, indicating that current market pricing necessitates an implied growth trajectory significantly higher than the company's historical reinvestment capacity.

* **CAPITAL_STRUCTURE_DYNAMICS:** The model reconciles a total debt-equivalent load of **INR 3,557 Cr**—reconciling **INR 1,427 Cr in lease liabilities** against **INR 864 Cr in core financial borrowings**. By integrating these liabilities into the WACC and the Enterprise-to-Equity bridge, the engine maintains a strict 1:1 deduction ratio, ensuring that the valuation of equity holders is not overstated by the omission of off-balance-sheet financing.

---

## SENSITIVITY_MODEL_OUTPUT

The following matrix illustrates the stability of the per-share intrinsic value (INR) relative to shifts in the discount rate and terminal growth assumptions.

| WACC / g | 6.00% | 6.50% | 6.93% (Rf) |
| :--- | :--- | :--- | :--- |
| **13.00%** | 654.21 | 701.33 | 745.89 |
| **13.91% (Baseline)** | 552.45 | 589.12 | **622.19** |
| **15.00%** | 461.90 | 489.24 | 514.56 |

---

## REPOSITORY_TREE
- `/core_engine`: Integrated DCF forecasting and FCFF calculation modules.
- `/risk_assessment`: Bottom-up beta de-levering and WACC calculation framework.
- `/fundamental_growth`: ROIC and Reinvestment Rate historical analysis.
- `/historical_data`: 10-year normalized financial statements and peer comparisons.

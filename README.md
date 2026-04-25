# ASIAN_PAINTS_VALUATION_ENGINE 

## SYSTEM_OVERVIEW
A high-fidelity financial modeling repository focused on the intrinsic valuation of Asian Paints Ltd. The project implements a three-stage Discounted Cash Flow (DCF) framework, integrating automated historical normalization, peer-group risk assessment, and fundamental growth forecasting.

### ARCHITECTURE_LOGIC
- **VALUATION_METHOD:** Free Cash Flow to Firm (FCFF)
- **TAX_LOGIC:** Marginal tax rate integration for NOPAT calculation
- **GROWTH_ENGINE:** ROIC (Return on Invested Capital) coupled with fundamental Reinvestment Rates
- **RISK_MODEL:** CAPM-based WACC utilizing bottom-up levered beta analysis

---

## EXECUTION_RESULTS

* **VALUATION_DELTA_ANALYSIS:** The model identifies a significant variance between fundamental value and market pricing. The calculated intrinsic value of **INR 622.19** per share represents a **75.25% discount** to the current market price of **INR 2,514**. This quantifies a market premium of **4.04x**, suggesting the current stock price is pricing in aggressive terminal growth expectations far exceeding the risk-free rate.

* **CAPITAL_STRUCTURE_RECONCILIATION:** Developed a granular debt-to-equity bridge by isolating **INR 1,427 Cr in Lease Liabilities** (Ind AS 116) from **INR 864 Cr in core Financial Borrowings**. By specifically mapping these obligations, the model ensures that the transition from Enterprise Value to Equity Value is mathematically accurate, preventing the overstatement of shareholder value common in simplified models.

---

## SENSITIVITY_MATRIX (DATA_TABLE)

| WACC / g | 6.0% | 6.5% | 6.93% (Rf) |
| :--- | :--- | :--- | :--- |
| **13.0%** | 654.21 | 701.33 | 745.89 |
| **13.9% (Baseline)** | 552.45 | 589.12 | **622.19** |
| **15.0%** | 461.90 | 489.24 | 514.56 |

---

## REPOSITORY_TREE
- `/core_model`: Integrated DCF and forecasting logic.
- `/risk_assessment`: WACC calculation and beta de-levering.
- `/historical_data`: 10-year normalized financial statements.
- `/documentation`: Research notes and sensitivity analysis.

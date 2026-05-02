---
title: "Three-Statement Model"
type: concept
created: 2026-05-02
updated: 2026-05-02
tags: [financial-modeling, foundation, model-type]
sources: [financial-modeling-guide]
status: draft
---

# Three-Statement Model

## Definition

A financial model comprised of three linked financial statements: the Income Statement, Balance Sheet, and Cash Flow Statement. It is the foundation of most financial modeling and valuation work.

## Explanation

The three-statement model is the foundation of all other models. It links together the company's core financial statements using formulas, so that changes in assumptions flow through all three statements consistently.

The typical building process:
1. Input historical data for Income Statement and Balance Sheet
2. Calculate ratios (growth rates, margins, CapEx ratios, working capital)
3. Build forecast assumptions based on historical trends
4. Forecast Income Statement (revenue down to pre-interest income)
5. Forecast Balance Sheet (assets, then liabilities, then equity)
6. Forecast Cash Flow Statement (operating, investing, financing)
7. "Plug" cash and short-term debt balances
8. Calculate interest expense
9. Ensure balance sheet balances

## Key Steps

- Turn off iteration to prevent circular references
- Work top-down (revenue → net income)
- Leave interest and cash out initially
- Use MAX/MIN functions to balance cash and debt
- Link all statements together
- Ensure the balance sheet equals: Assets = Liabilities + Equity

## Related Concepts

- [[financial-modeling]]
- [[excel-financial-modeling]]
- [[model-assumptions]]

## Sources

- [[financial-modeling-guide]]

---

---
title: "DCF Model"
type: concept
created: 2026-05-02
updated: 2026-05-02
tags: [financial-modeling, valuation, model-type]
sources: [financial-modeling-guide]
status: stub
---

# DCF Model

## Definition

Discounted Cash Flow (DCF) model is a valuation model that estimates a company's future cash flows and discounts them to their present value to determine enterprise value.

## Explanation

DCF analysis focuses on cash generation within a company to determine its valuation. The model projects free cash flows (operating cash flow minus capital expenditures) for a forecast period, calculates a terminal value, and discounts both back to today using a discount rate (typically WACC).

The fundamental question: "If this business generates X dollars of cash flow over the next 10 years, what's that worth to me today?"

## Uses

- [[investment-banking|Investment banking]] — valuation for M&A
- [[private-equity|Private equity]] — assessing acquisition targets
- Equity research — stock valuation
- Corporate finance — project and acquisition evaluation

## Related Concepts

- [[financial-modeling]]
- [[three-statement-model]] — DCF builds on the three-statement model
- [[ma-model]] — M&A valuation

## Sources

- [[financial-modeling-guide]]

## Open Questions

- How sensitive is DCF to discount rate and terminal value assumptions?
- When is DCF better than comparable company analysis?

---

---
title: "LBO Model"
type: concept
created: 2026-05-02
updated: 2026-05-02
tags: [financial-modeling, private-equity, model-type]
sources: [financial-modeling-guide]
status: stub
---

# LBO Model

## Definition

Leveraged Buyout (LBO) model is a financial model that helps identify a company's debt capacity and structure a leveraged acquisition, given a target investment horizon and expected returns.

## Explanation

Used primarily by [[private-equity|private equity]] funds and their financial advisors, LBO models evaluate how much debt can be used to finance an acquisition while still meeting debt covenants and return targets. The model forecasts cash flows and debt paydown over the holding period.

Key metrics:
- Debt/EBITDA ratios
- Interest coverage ratios
- Debt service coverage ratios
- Target IRR (internal rate of return)

## Related Concepts

- [[financial-modeling]]
- [[three-statement-model]]
- [[private-equity-analyst]]

## Sources

- [[financial-modeling-guide]]

---

---
title: "M&A Model"
type: concept
created: 2026-05-02
updated: 2026-05-02
tags: [financial-modeling, investment-banking, model-type]
sources: [financial-modeling-guide]
status: draft
---

# M&A Model

## Definition

Merger & Acquisition (M&A) model is a financial model that brings together the financial models of two companies and assesses the impact of the transaction on the acquirer's financials.

## Explanation

The M&A model is used by [[investment-banking|investment bankers]] and [[ma-analyst|M&A analysts]] to:
- Evaluate the financial impact of a merger or acquisition
- Determine accretion/dilution to EPS (earnings per share)
- Assess deal economics and synergies
- Structure the transaction

The model builds a combined company forecast that accounts for purchase accounting, integration costs, and projected synergies.

## Uses

- Evaluating whether a merger benefits both companies
- Deal structuring and pricing
- Determining deal accretion/dilution

## Related Concepts

- [[financial-modeling]]
- [[three-statement-model]]
- [[investment-banking]]
- [[ma-analyst]]

## Sources

- [[financial-modeling-guide]]

## Open Questions

- How are synergies modeled and validated?
- What are typical deal assumptions?

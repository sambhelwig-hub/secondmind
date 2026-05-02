---
title: "Excel & Financial Modeling"
type: concept
created: 2026-05-02
updated: 2026-05-02
tags: [technical-skill, excel, tool]
sources: [financial-modeling-guide]
status: draft
---

# Excel & Financial Modeling

## Definition

The technical skills and Excel techniques required to build robust financial models, including formulas, circular reference management, and spreadsheet best practices.

## Explanation

Financial modeling is most commonly done in Excel. Key technical skills include:

**Formulas & Functions:**
- Linking across sheets
- SUM, IF, MAX, MIN functions
- Absolute vs. relative references
- Array formulas

**Circular Reference Management:**
- Turning off iteration initially to prevent errors
- Using MAX/MIN functions to "plug" values
- Recognizing when circular references are necessary vs. problematic

**Model Structure:**
- Separating inputs, calculations, and outputs
- Using consistent naming conventions
- Organizing sheets by function (assumptions, calcs, outputs)
- Breaking complex calculations into steps

**Maintenance & Editing:**
- Saving backups before major edits
- Tracing dependencies to avoid #REF errors
- Documenting formulas and assumptions
- Keeping the model clean

## Common Pitfalls

- Mixing hard-coded values with formulas
- Not documenting assumptions
- Creating overly complex calculations in one cell
- Ignoring circular references during build
- Not testing the model thoroughly

## Related Concepts

- [[financial-modeling]]
- [[three-statement-model]]
- [[model-assumptions]]
- [[financial-model-best-practices]]

## Sources

- [[financial-modeling-guide]]

---

---
title: "Model Assumptions"
type: concept
created: 2026-05-02
updated: 2026-05-02
tags: [financial-modeling, forecasting, skill]
sources: [financial-modeling-guide]
status: draft
---

# Model Assumptions

## Definition

The forecasting assumptions that drive a financial model — revenue growth rates, margin expectations, capital expenditure levels, working capital changes, and other forward-looking estimates based on historical analysis and market expectations.

## Explanation

The key skill in financial modeling is creating sensible, justifiable assumptions. A model is only as good as the assumptions that drive it.

**Process:**
1. Calculate historical ratios (revenue growth, margins, CapEx as % of revenue, working capital days)
2. Analyze what drove historical performance
3. Identify assumptions that should change in the forecast (e.g., if 4% of growth came from FX and 6% from organic, forecast organic growth going forward)
4. Build assumptions based on:
   - Historical trends
   - Management guidance
   - Industry forecasts
   - Analyst consensus
   - Company-specific catalysts

**Common Assumptions:**
- Revenue growth rates
- Operating margins
- CapEx as % of revenue
- Working capital as days of revenue
- Tax rates
- Discount rates (WACC)

## Sensitivity Analysis

Models should test how outputs change when key assumptions change. This reveals which assumptions matter most to the valuation or decision.

## Related Concepts

- [[financial-modeling]]
- [[three-statement-model]]
- [[excel-financial-modeling]]

## Sources

- [[financial-modeling-guide]]

## Open Questions

- How conservative should assumptions be?
- How do you validate assumptions against market data?

---

---
title: "Financial Model Best Practices"
type: concept
created: 2026-05-02
updated: 2026-05-02
tags: [financial-modeling, documentation, maintenance]
sources: [financial-modeling-guide]
status: draft
---

# Financial Model Best Practices

## Definition

Industry-standard conventions and practices for designing, building, maintaining, and documenting financial models to ensure they are intuitive, error-proof, and structurally sound.

## Best Practices

### Design

- Start with outputs (what decision does the model support?)
- Design the layout before building
- Separate inputs from calculations from outputs
- Use consistent formatting and naming conventions
- Document all assumptions clearly

### Building

- Turn off iteration to prevent accidental circular references
- Build systematically: income statement, balance sheet, cash flow
- Link statements together, not separately
- Test the model with sample data before populating
- Break complex calculations into steps
- Use cell comments to document logic

### Maintenance & Editing

- Always save a backup before making major changes
- Make one edit at a time, updating all affected sections
- Label new items clearly
- Trace dependencies before removing old items to avoid #REF errors
- Ensure all changes flow through all three statements
- Remove redundant cells after changes
- Keep the model clean and efficient

### Output & Communication

- Ensure outputs look reasonable (sanity check)
- Create multiple scenarios (base, bull, bear)
- Use charts and graphs for presentation
- Document assumptions on a separate sheet
- Make the model easy for others to understand and update

## Why This Matters

Most models encountered in practice are poorly designed, difficult to follow, and hard to maintain. Models should be built to the highest possible standards because they drive financial decisions worth millions of dollars.

## Related Concepts

- [[financial-modeling]]
- [[excel-financial-modeling]]

## Sources

- [[financial-modeling-guide]]

# NotebookLM Reference — ESG Translation Background Knowledge

This document summarizes the conceptual framework, translation philosophy, and international standards referenced in the user's NotebookLM notes. Claude must use this knowledge to ensure audit-grade translation quality.

---

## 1. Terminology Database (E/S/G + International Standards)

The user requires a disclosure-grade terminology system aligned with global sustainability reporting practices.

### Environmental (E)
- Scope 1 / 2 / 3 Emissions
- GHG Inventory / Accounting
- Carbon Intensity
- Climate Resilience
- Pollution Prevention and Management
- Effluent Treatment and Mitigation
- Natural Capital (preferred over Natural Resources)

### Social (S)
- Occupational Health and Safety (OHS)
- Diversity & Inclusion (D&I)
- Human Rights Due Diligence
- Community Engagement

### Governance (G)
- Double Materiality
- Business Integrity / Ethics
- Risk Management / Mitigation
- Responsible Sourcing (value chain context)

### International Framework Abbreviations
- CSRD — Corporate Sustainability Reporting Directive
- ESRS — European Sustainability Reporting Standards
- GRI — Global Reporting Initiative
- ISSB — IFRS S1/S2
- TCFD — Task Force on Climate-related Financial Disclosures
- GHG — Greenhouse Gas

Claude must ensure all terminology aligns with glossary.md.

---

## 2. Translation Principles from NotebookLM

### 2.1 Functional Equivalency (not literal translation)
Use internationally recognized disclosure language.

Examples:
- “減少污染” → not “reducing pollution”
  - Use “Pollution Prevention and Management”
- “廢水處理” → “Effluent Treatment and Mitigation”

### 2.2 Ecolinguistic Perspective
Prefer sustainability-oriented language:
- “Natural Capital” instead of “Natural Resources”
- “Climate-related Financial Risks” instead of generic “climate risks”

### 2.3 Financial & Quantitative Precision
Units must be preserved exactly:
- MWh of Electricity Saved
- Metric Tons of CO₂e Reduced

---

## 3. Corporate Tone Learning (Few-Shot Examples)

Claude may reference the tone and structure of:
- Nuvoton Sustainability Report
- CyberTAN Sustainability Report
- Macronix Sustainability Report

Key patterns:
- “About this Report”
- “Message from Management”
- “Materiality Assessment and Stakeholder Engagement”
- Standardized GRI / SASB / TCFD index tables

Claude must maintain:
- Consistent section headers
- Proper disclosure tone
- Correct table formatting

---

## 4. International Standards Context

### ISSB (IFRS S1/S2)
- Focus on climate-related financial risks and opportunities
- Distinguish:
  - Transition risks
  - Physical risks

### GRI (Global Reporting Initiative)
- Emphasizes Double Materiality:
  - Outside-in: impact on enterprise value
  - Inside-out: enterprise impact on economy, environment, people

### Value Chain Considerations
- Upstream and Downstream impacts
- Responsible Sourcing
- Supplier environmental/social assessments

---

## 5. How Claude Must Use This Document

When reviewing translations:
- Apply terminology from glossary.md
- Apply tone/structure rules from translation_guidelines.md
- Apply workflow from workflow.md
- Use this NotebookLM reference as background knowledge to:
  - Improve accuracy
  - Ensure alignment with international standards
  - Maintain corporate disclosure tone
  - Avoid literal translation errors
  - Preserve sustainability framing

This document does not override glossary.md or translation_guidelines.md.

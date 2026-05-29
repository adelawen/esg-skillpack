# Quantitative Standards — Numbers, Units, Dates, Currency

This file defines mandatory formatting for all numerical content in ESG report translation. Audit-grade translation requires absolute precision in quantitative data.

## 1. Numbers

- Use thousands separators with commas: `1,234,567` (not `1234567` or `1.234.567`)
- Decimal point is `.` (period), not `,` (comma)
- Preserve exact precision from source: if source shows `12.50`, do not write `12.5`
- Negative numbers: use minus sign `-1,234`, not parentheses `(1,234)` unless source uses parentheses for accounting

## 2. Units of Measurement

| Source (Chinese) | Standard English |
|------------------|------------------|
| 公噸 / 噸 | metric tons (or t) |
| 二氧化碳當量 | CO₂e |
| 公噸二氧化碳當量 | tCO₂e (subscript when possible) |
| 千瓦時 / 度 | kWh |
| 百萬瓦時 | MWh |
| 十億焦耳 | GJ |
| 立方公尺 | m³ |
| 公升 | L (liters) |
| 公斤 | kg |
| 公頃 | hectares (ha) |

**Critical:** Always use `tCO₂e` (lowercase t, subscript 2). Never `TCO2e`, `tCO2e`, `Tons CO2`.

## 3. Dates and Years

| Source | Translation |
|--------|-------------|
| 2024 年 | 2024 |
| 民國 113 年 | 2024 (convert ROC year to Western year) |
| 2024 年度 | fiscal year 2024 / FY2024 |
| 報告期間 2024 年 1 月 1 日至 12 月 31 日 | the reporting period from January 1 to December 31, 2024 |
| 截至 2024 年底 | as of December 31, 2024 |

**Always convert ROC (民國) years to Western years.** Add a footnote on first occurrence if the report originally uses ROC convention.

## 4. Currency

| Source | Translation |
|--------|-------------|
| 新台幣 | NT$ (in tables) / New Taiwan Dollar (NTD) (in prose, first occurrence) |
| 仟元 / 千元 | NT$ thousand |
| 佰萬元 / 百萬元 | NT$ million |
| 億元 | NT$100 million (do not translate to "billion" — preserve Chinese counting unit if relevant) |

**Use ISO 4217 codes** in financial tables: `TWD`, `USD`, `EUR`, `JPY`, `CNY`.

## 5. Percentages

- Use `%` symbol with no space: `15.5%`, not `15.5 %` or `15.5 percent`
- Preserve decimal places exactly as source
- For ranges: `10%–15%` with en dash, not hyphen

## 6. Scope 1 / 2 / 3 Emissions

- Always capitalize: `Scope 1`, `Scope 2`, `Scope 3` (not `scope 1`)
- Hyphenate when used as adjective: `Scope 1 emissions` (no hyphen) but `Scope-1-related risks` (hyphenated)
- Total emissions: `total Scope 1 and Scope 2 emissions` (repeat "Scope")

## 7. GHG Calculation Method References

When source mentions calculation methodology, preserve exact framework:
- 環保署公告排放係數 → emission factors published by the Taiwan EPA
- IPCC 第六次評估報告 GWP 值 → Global Warming Potential (GWP) values from IPCC AR6
- ISO 14064-1:2018 → ISO 14064-1:2018 (no translation)

## 8. Verification of Numerical Accuracy

Before finalizing translation, perform numerical sanity check:
- [ ] Every number in source appears in translation
- [ ] No digits transposed (e.g., 1,234 vs. 1,243)
- [ ] Units match source
- [ ] Year references converted correctly (ROC → Western)
- [ ] Percentages and totals add up if source shows breakdowns
# ESG Sustainability Report Translation Skill Pack

**Version:** 1.2
**Last Updated:** 2026-05-27
**Maintained for:** 新竹科學城 2024 永續報告書 (extensible to other ESG reports)

## Purpose

Audit-grade translation and review of Chinese ESG sustainability reports into English, aligned with GRI Universal Standards 2021, SASB, TCFD, and ISSB (IFRS S1/S2).

## File Structure

| File | Layer | Priority | Purpose |
|------|-------|----------|---------|
| `manifest.md` | Documentation | — | Project overview and maintenance guide (this file) |
| `WORKFLOW.md` | Documentation | — | End-to-end Canva + Claude translation pipeline |
| `SKILL.md` | Execution | — | Main skill entry point with mode selection |
| `glossary.md` | Rules | 1 (highest) | Terminology dictionary, prohibited translations |
| `quantitative_standards.md` | Rules | 2 | Numbers, units, dates, currency |
| `translation_guidelines.md` | Rules | 3 | Tone, tense, structure |
| `examples.md` | Reference | 4 | Few-shot translation patterns |
| `notebooklm_reference.md` | Knowledge | 5 (lowest) | Conceptual background only |

## Installation

Copy this folder to your Claude Code project as:
```
.claude/skills/esg-report-translator/
```
Then invoke with `/esg-report-translator` or any trigger phrase listed in SKILL.md.

## Operating Modes

- **TRANSLATE_AND_REVIEW** (default): full pipeline
- **REVIEW_ONLY**: QA without rewriting
- **TRANSLATE_ONLY**: source → translation with self-review

## Output Standards

Every output must include:
1. Final English Translation (or skip if REVIEW_ONLY)
2. Error List with Severity Classification
3. Consistency Check
4. Notes for Canva Fixes

## Priority Resolution

When rules conflict, apply this order:
1. glossary.md
2. quantitative_standards.md
3. translation_guidelines.md
4. examples.md
5. notebooklm_reference.md

## Extension Path

To add new industry vocabulary:
1. Add terms to relevant glossary.md section (A–K)
2. Add prohibited translations to Section K
3. Add examples to examples.md if needed
4. Update version number above

## Change Log

- **v1.2 (2026-05-27)**: Added WORKFLOW.md (Canva + Claude pipeline documentation); upgraded SKILL.md frontmatter with `context: fork` and `allowed-tools`; added installation instructions; renamed project to 新竹科學城 2024
- **v1.1 (2026-04-26)**: Merged manifest and final_skill_pack; added quantitative_standards.md, examples.md; completed glossary G section; added prohibited translations Section K
- **v1.0**: Initial skill pack
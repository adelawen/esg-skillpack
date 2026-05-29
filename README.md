# esg-skillpack
ESG sustainability report translation system built with Claude Code — includes 7 rule files (SkillPack) and installation guide.
# ESG SkillPack for Claude Code

A reusable, iterable translation system for ESG sustainability reports.
Built to produce audit-ready English output aligned with GRI, SASB, and TCFD frameworks.

## What this is

Most ESG translation workflows are one-time prompts. This is a system —
seven rule files that together function as a transferable translation engine
that can be updated, versioned, and handed off.

Built for the Hsinchu Science City 2024 Sustainability Report.

## Files

| File | Purpose |
|------|---------|
| `SKILL.md` | Master router — triggers the entire system |
| `glossary.md` | Chinese–English term dictionary (highest priority) |
| `translation_guidelines.md` | Tone, tense, sentence structure standards |
| `quantitative_standards.md` | Units, dates, currency formatting |
| `examples.md` | Reference translations for common ESG sentence patterns |
| `notebooklm_reference.md` | GRI / SASB / TCFD framework context |
| `WORKFLOW.md` | Five-stage process: analysis → terminology → draft → QA → output |

## How to use

1. Install Node.js and Claude Code
2. Place all seven files in `.claude/skills/esg-report-translator/`
3. Launch Claude Code from your working directory
4. Trigger with `/esg-report-translator` or type `永續報告書翻譯審查`

## Output

- Corrected English full text
- Error list with severity classification
- Canva Find/Replace commands for layout correction

## Author

Hsin-Yu Wen (溫心語) · [LinkedIn](https://www.linkedin.com/in/adelawen)

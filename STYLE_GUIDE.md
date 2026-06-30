# Style Guide

## Purpose

Establish consistent formatting, terminology, and presentation standards for all documents in this repository.

## General Principles

- Clarity over brevity
- Precision over generality
- Active voice preferred
- Present tense for current requirements
- Future tense only for planned changes

## Formatting Standards

### Headings
- H1: Document title only (one per document)
- H2: Major sections (## Section Name)
- H3: Subsections (### Subsection Name)
- H4: Sub-subsections (#### Detail Name) — use sparingly
- No H5 or H6

### Text Formatting
- **Bold**: Key terms on first use, critical requirements
- *Italic*: Emphasis, foreign terms, document titles in references
- `Monospace`: File paths, code, commands, abbreviations
- ~~Strikethrough~~: Not used (use version control for history)

### Lists
- Unordered: `- ` (dash + space)
- Ordered: `1. ` (number + period + space)
- Nested: 2-space indent
- Maximum 3 nesting levels

### Tables
- Header row required
- Use pipes `|` for separation
- Align content: left for text, right for numbers, center for codes
- No empty cells — use "N/A" or "—"
- Caption above table: `**Table N:** Description`

### Code Blocks
- Always specify language: ```yaml, ```markdown, ```bash
- Use for: configuration, structured data, commands, formulas
- Not for: regular text, bullet points

### Links
- Internal: `[Link Text](../path/document.md#anchor)`
- External: `[Link Text](https://example.com) <!-- Accessed: YYYY-MM-DD -->`
- Reference style: `[REF: DOC_ID]` for inline cross-references

### Images
- Store in `assets/images/`
- Format: `![Alt Text](../assets/images/filename.png)`
- Preferred formats: PNG (diagrams), SVG (vector), JPG (photos)
- Maximum width: 800px

## Writing Standards

### Terminology
- Use terms defined in GLOSSARY.md
- On first use: **full term (ABBREVIATION)** then ABBREVIATION thereafter
- Avoid synonyms for defined terms

### Numbers and Units
- SI units mandatory
- Space between number and unit: `100 kg`, not `100kg`
- Thousands separator: comma `1,000` or space `1 000` (consistent per doc)
- Decimals: period `3.14`
- Ranges: `10–20 kg` (en dash)

### Currency
- Indian Rupees: `₹` symbol, Indian numbering (lakh, crore)
- Format: `₹10 lakh`, `₹1.5 crore`
- USD for reference: `$` with conversion date `($1 = ₹83.50, 2026-06-30)`

### Dates
- ISO 8601: `YYYY-MM-DD`
- Fiscal year: `FY 2025-26`
- Quarters: `Q1 FY 2025-26`

### Citations
Format: `[CITATION: Source, Year, Section/Page]`
Examples:
- `[CITATION: MoFPI, 2024, Para 3.2]`
- `[CITATION: FSSAI, 2023, Regulation 4.1]`
- `[CITATION: BIS, 2020, IS 12345:2020 Clause 5]`

### Abbreviations
- Define in ABBREVIATIONS.md
- First use in each document: **Full Term (ABBR)**
- Common abbreviations (PMKSY, MoFPI, FSSAI, BIS) may be used without definition after first use in document

## Document-Specific Styles

### Technical Specifications
- Requirements: `SHALL` (mandatory), `SHOULD` (recommended), `MAY` (optional)
- Use RFC 2119 keywords
- Quantifiable criteria with tolerances

### Financial Models
- All assumptions in dedicated table
- Formula notation: standard mathematical notation
- Sensitivity analysis required for key variables

### Procedures
- Numbered steps
- Decision points in diamond notation: `IF condition THEN action`
- Responsible role for each step

### Compliance Checklists
- Table format: Requirement | Reference | Status | Evidence
- Status values: Compliant / Non-Compliant / Not Applicable / Partial

## Markdown Linting Rules

### Enabled Rules (markdownlint)
- MD001: Heading levels increment by one
- MD003: Heading style (ATX)
- MD004: Unordered list style (dash)
- MD007: Unordered list indentation (2 spaces)
- MD009: No trailing spaces
- MD010: No hard tabs
- MD012: No multiple consecutive blank lines
- MD013: Line length (max 120 chars, exceptions for tables/links)
- MD022: Headings surrounded by blank lines
- MD025: Single top-level heading
- MD026: No trailing punctuation in headings
- MD031: Fenced code blocks surrounded by blank lines
- MD032: Lists surrounded by blank lines
- MD033: No inline HTML (except comments for access dates)
- MD034: No bare URLs
- MD040: Fenced code blocks have language
- MD041: First line is top-level heading
- MD046: Code block style (fenced)
- MD047: Single trailing newline

### Disabled Rules
- MD013 (line length) for tables and long URLs
- MD033 for access date comments

## Front Matter Template

```yaml
---
doc_id: "CATEGORY-NNN"
title: "Document Title"
version: "1.0.0"
status: "DRAFT"
owner: "Role Name"
reviewers: ["Role1", "Role2"]
approver: "Role Name"
created: "YYYY-MM-DD"
modified: "YYYY-MM-DD"
tags: ["tag1", "tag2"]
references: ["DOC_ID_1", "DOC_ID_2"]
---
```

## Quality Checklist (Pre-Submission)

- [ ] Single H1 heading
- [ ] Heading hierarchy sequential
- [ ] All lists use dash/number format
- [ ] Tables have headers and aligned columns
- [ ] Code blocks have language specified
- [ ] Internal links use relative paths
- [ ] External links have access dates
- [ ] [REF: DOC_ID] format used for cross-refs
- [ ] All abbreviations defined or in ABBREVIATIONS.md
- [ ] Citations in standard format
- [ ] Units with spaces
- [ ] Currency in ₹ with lakh/crore
- [ ] Dates in YYYY-MM-DD
- [ ] Front matter complete and valid
- [ ] markdownlint passes (zero errors)
- [ ] All links resolve
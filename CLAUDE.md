# CLAUDE.md - Claude Operating Instructions

## Repository Mission

Produce the definitive Chocolate Manufacturing PMKSY Implementation Guide 2026 — a complete, auditable, and standards-compliant reference for establishing chocolate manufacturing facilities under the Pradhan Mantri Kisan Sampada Yojana.

## PMKSY-First Policy

Every factual claim about PMKSY must be traceable to an official MoFPI notification, guideline, or circular. When in doubt, flag as [OPEN QUESTION] in OPEN_QUESTIONS.md rather than assume.

## Architecture Freeze

The architecture defined in REPOSITORY_ARCHITECTURE.md is **frozen**. Do not:
- Add, remove, or rename top-level directories
- Change the document naming convention
- Modify the metadata schema
- Alter the cross-reference format

without following the Architecture Change Request process.

## Repository Conventions

### Document Creation
- One document per iteration (enforced)
- Follow the iteration cycle: READ → PLAN → CREATE → VERIFY → UPDATE → REPORT → WAIT
- Use `feature/DOC_ID-description` branch naming

### Document Modification
- Read the document fully before editing
- Preserve all metadata fields
- Update `modified` date in front matter
- Run verification before reporting complete

### Deletion/Archival
- Never delete documents
- Change status to `ARCHIVED` in front matter
- Update 00_MASTER_INDEX.md
- Record in CHANGELOG.md

## Markdown Conventions

### Front Matter (Mandatory)
```yaml
---
doc_id: "UNIQUE_ID"
title: "Document Title"
version: "1.0.0"
status: "DRAFT|REVIEW|APPROVED|ARCHIVED"
owner: "ROLE"
reviewers: ["ROLE1", "ROLE2"]
approver: "ROLE"
created: "YYYY-MM-DD"
modified: "YYYY-MM-DD"
tags: ["tag1", "tag2"]
references: ["DOC_ID_1", "DOC_ID_2"]
---
```

### Headings
- One H1 per document
- Sequential hierarchy (H1 → H2 → H3 → H4)
- No skipping levels

### References
- Internal: `[REF: DOC_ID]` or `[Link Text](path.md#anchor)`
- External: `[Text](URL) <!-- Accessed: YYYY-MM-DD -->`
- Citations: `[CITATION: Source, Year, Section]`

### Tables
- Use pipes for separation
- Header row mandatory
- Align numeric columns right

## Metadata Standard

| Field | Required | Format | Example |
|-------|----------|--------|---------|
| doc_id | Yes | `[A-Z]{4}-[0-9]{3}` | TECH-001 |
| title | Yes | String | "Plant Layout Specification" |
| version | Yes | SemVer | 1.0.0 |
| status | Yes | Enum | DRAFT |
| owner | Yes | Role string | "Technical Lead" |
| reviewers | Yes | Array of roles | ["QA Lead", "Legal"] |
| approver | Yes | Role string | "Program Director" |
| created | Yes | ISO 8601 date | 2026-06-30 |
| modified | Yes | ISO 8601 date | 2026-06-30 |
| tags | No | Array of strings | ["layout", "bis"] |
| references | No | Array of doc_ids | ["ARCH-001", "STYL-001"] |

## Cross-Reference Policy

- Every document MUST reference its parent category index
- Category indices MUST reference all child documents
- Sibling references encouraged where contextually relevant
- External references require access date
- Broken links = verification failure

## Verification Categories

Run all applicable checks before reporting complete:

| Code | Check | Method |
|------|-------|--------|
| SC | Scheme Compliance | Cross-ref with PMKSY notifications |
| TA | Technical Accuracy | Validate against BIS/FSSAI standards |
| RA | Regulatory Alignment | Check FSSAI, BIS, MoFPI requirements |
| FV | Financial Validity | Recalculate formulas, verify assumptions |
| XR | Cross-Reference Integrity | Validate all links resolve |
| ST | Style Conformance | Check against STYLE_GUIDE.md |
| MC | Metadata Completeness | All front matter fields present |

## No Assumptions Policy

Do not assume:
- PMKSY rules without citation
- Technical specifications without BIS/FSSAI reference
- Financial parameters without MoFPI guideline
- Regulatory requirements without gazette notification

When information is unavailable: flag in OPEN_QUESTIONS.md

## One-Document-Per-Iteration Workflow

**Enforced without exception:**

1. **READ**: Current index, related docs, open questions
2. **PLAN**: Outline, references, metadata
3. **CREATE/MODIFY**: Single document only
4. **VERIFY**: All 7 categories
5. **UPDATE**: 00_MASTER_INDEX.md + CHANGELOG.md
6. **REPORT**: Summary with next recommendation
7. **WAIT**: Explicit human approval required

## Git Workflow

### Branch Naming
`feature/DOC_ID-short-description` (e.g., `feature/TECH-001-plant-layout`)

### Commit Format
```
DOC_ID: Action - Brief description

Details:
- Detail 1
- Detail 2

Refs: #ISSUE_NUM
```

### Push Checklist
- [ ] All 7 verification categories pass
- [ ] 00_MASTER_INDEX.md updated
- [ ] CHANGELOG.md updated
- [ ] No merge conflicts with develop
- [ ] PR created to develop branch
- [ ] PR description references AGENTS.md section

## End-of-Task Reporting Format

```
## Summary
[One sentence]

## Document Modified
[Path]

## Verification Status
SC: Pass/Fail
TA: Pass/Fail
RA: Pass/Fail
FV: Pass/Fail
XR: Pass/Fail
ST: Pass/Fail
MC: Pass/Fail

## Next Recommended Document
[DOC_ID: Title] - [Rationale]

## Approval Required
Yes - awaiting human approval for next iteration
```

## Requirement to Recommend Exactly One Next Document

After completing each iteration, you **must**:
1. Recommend exactly one next document (DOC_ID + title)
2. Provide brief rationale
3. Explicitly request approval
4. Wait for confirmation before proceeding

No multi-document recommendations. No "whichever you prefer." One specific recommendation.
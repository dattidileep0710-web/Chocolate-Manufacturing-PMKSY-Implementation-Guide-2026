# Repository Architecture

## Overview

This document defines the architectural principles, structure, and organization of the Chocolate Manufacturing PMKSY Implementation Guide 2026 repository.

## Architectural Principles

### PMKSY-First Principle
All content must align with PMKSY scheme requirements, guidelines, and objectives. No content may contradict official PMKSY notifications.

### Architecture Freeze Policy
Once the repository architecture is established in this document, structural changes require:
1. Formal architecture review
2. Approval from designated architecture authority
3. Update to this document with version increment
4. Notification to all stakeholders

### Single Source of Truth
Each piece of information exists in exactly one authoritative location. Cross-references use standardized linking.

## Repository Structure

```
/
├── README.md                 # Repository overview
├── REPOSITORY_ARCHITECTURE.md # This document
├── 00_MASTER_INDEX.md        # Master document index
├── AGENTS.md                 # AI agent operating manual
├── CLAUDE.md                 # Claude-specific instructions
├── CHANGELOG.md              # Version history
├── ROADMAP.md                # Implementation roadmap
├── DOCUMENT_CONTROL.md       # Document control procedures
├── VERIFICATION_MATRIX.md    # Verification requirements
├── STYLE_GUIDE.md            # Content style standards
├── OPEN_QUESTIONS.md         # Unresolved questions
├── KNOWN_GAPS.md             # Identified content gaps
├── CONTRIBUTING.md           # Contribution guidelines
├── CONTACTS.md               # Stakeholder contacts
├── GLOSSARY.md               # Terminology definitions
├── ABBREVIATIONS.md          # Abbreviation list
├── LICENSE                   # License file
└── PMKSY_MASTER/
    ├── 01_SCHEME_OVERVIEW.md
    ├── 02_PROJECT_ELIGIBILITY.md
    ├── 03_APPLICANT_ELIGIBILITY.md
    ├── 04_ENTITY_ELIGIBILITY.md
    ├── 05_LAND_ELIGIBILITY.md
    ├── 06_ELIGIBLE_PROJECT_COST.md
    ├── 07_REQUIRED_DOCUMENTS.md
    ├── 08_APPLICATION_WORKFLOW.md
    ├── 09_IMPLEMENTING_AGENCIES.md
    ├── 10_PROJECT_APPRAISAL.md
    ├── 11_GRANT_RELEASE.md
    ├── 12_POST_PROJECT_MONITORING.md
    ├── 13_COMPLIANCE.md
    ├── 14_COMMON_REJECTION_REASONS.md
    └── 15_FAQ.md
    └── 10_appendices/
```

## Document Organization

### Naming Convention
- Format: `NN_CATEGORY_NAME.md` (zero-padded two-digit prefix)
- Categories use lowercase with underscores
- Example: `03_technical_specs_chocolate_processing.md`

### Metadata Header
Every document must begin with a YAML front matter block:
```yaml
---
doc_id: "UNIQUE_ID"
title: "Document Title"
version: "1.0.0"
status: "DRAFT|REVIEW|APPROVED|ARCHIVED"
owner: "ROLE_OR_NAME"
reviewers: ["ROLE1", "ROLE2"]
approver: "ROLE"
created: "YYYY-MM-DD"
modified: "YYYY-MM-DD"
tags: ["tag1", "tag2"]
references: ["DOC_ID_1", "DOC_ID_2"]
---
```

## Cross-Reference Standards

### Internal Links
Format: `[Link Text](relative/path/to/document.md#section-id)`

### External Links
Format: `[Link Text](https://example.com)` with access date comment

### Reference Format
`[REF: DOC_ID]` for inline references

## Version Control

### Branching Strategy
- `main` - Approved, production-ready content
- `develop` - Active development
- `feature/*` - Individual document development
- `hotfix/*` - Urgent corrections

### Tagging
Format: `vMAJOR.MINOR.PATCH` (e.g., `v1.0.0`)

## Governance Integration

This architecture is governed by:
- [AGENTS.md](AGENTS.md) - Agent workflow rules
- [CLAUDE.md](CLAUDE.md) - Claude-specific rules
- [DOCUMENT_CONTROL.md](DOCUMENT_CONTROL.md) - Document lifecycle
- [VERIFICATION_MATRIX.md](VERIFICATION_MATRIX.md) - Quality gates
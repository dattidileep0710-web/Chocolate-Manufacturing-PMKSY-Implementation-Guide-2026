# AI Agent Operating Manual

## Repository Purpose

This repository contains the Chocolate Manufacturing PMKSY Implementation Guide 2026 — a comprehensive, standards-compliant framework for establishing and operating chocolate manufacturing facilities under the Pradhan Mantri Kisan Sampada Yojana (PMKSY).

## Repository Scope

### In Scope
- PMKSY scheme interpretation for chocolate manufacturing
- Technical specifications and standards
- Quality and compliance frameworks
- Financial models and subsidy calculations
- Implementation procedures and timelines
- Monitoring and verification systems

### Out of Scope
- General chocolate manufacturing not under PMKSY
- Policy advocacy or scheme modification proposals
- Proprietary manufacturer-specific processes
- Real-time operational data or production records

## PMKSY-First Principle

**All content must align with official PMKSY notifications, guidelines, and objectives.**

### Rules
1. No content may contradict Ministry of Food Processing Industries (MoFPI) notifications
2. All scheme interpretations must cite official source documents
3. Where ambiguity exists, flag as [OPEN QUESTION] in OPEN_QUESTIONS.md
4. Updates to PMKSY guidelines trigger mandatory content review

## Architecture Freeze Policy

The repository architecture (defined in REPOSITORY_ARCHITECTURE.md) is frozen after initial approval.

### Change Process
1. Submit Architecture Change Request (ACR) via GitHub Issue
2. Architecture Review Board evaluates impact
3. Approved changes increment architecture version
4. All dependent documents updated within 5 business days
5. CHANGELOG.md records the change with rationale

## Repository Implementation Workflow

### One-Document-Per-Iteration Policy
Agents create or modify exactly **one** Markdown document per iteration.

### Iteration Cycle
```
1. READ current state (index, related docs, open questions)
2. PLAN document content (outline, references, metadata)
3. CREATE/MODIFY single document
4. VERIFY against standards (style, cross-refs, metadata)
5. UPDATE 00_MASTER_INDEX.md and CHANGELOG.md
6. REPORT completion with next document recommendation
7. WAIT for human approval before next iteration
```

### Document Lifecycle
```
DRAFT → REVIEW → APPROVED → (ARCHIVED)
```

## Markdown Standards

### File Encoding
- UTF-8 without BOM
- LF line endings

### Heading Structure
- Single H1 (#) per document (title)
- H2 (##) for major sections
- H3 (###) for subsections
- Maximum depth: H4 (####)

### Lists
- Use `-` for unordered lists
- Use `1.` for ordered lists
- Nested lists indented by 2 spaces

### Tables
- Use GitHub-flavored markdown tables
- Header row required
- Align columns for readability

### Code Blocks
- Specify language for syntax highlighting
- Use for code, configs, structured data only

### Links
- Relative paths for internal links
- Absolute URLs for external with access date: `[Text](URL) <!-- Accessed: YYYY-MM-DD -->`

### Images
- Store in `assets/images/`
- Reference with relative paths
- Include alt text

## Verification Categories

| Category | Code | Description |
|----------|------|-------------|
| Scheme Compliance | SC | Aligns with PMKSY notifications |
| Technical Accuracy | TA | Factually correct specifications |
| Regulatory Alignment | RA | Meets FSSAI, BIS, MoFPI requirements |
| Financial Validity | FV | Calculations verified, assumptions stated |
| Cross-Reference Integrity | XR | All links valid, references current |
| Style Conformance | ST | Follows STYLE_GUIDE.md |
| Metadata Completeness | MC | All required front matter fields present |

## Cross-Reference Rules

1. Every document references its parent category document
2. Child documents reference sibling documents where relevant
3. Use `[REF: DOC_ID]` format for inline references
4. Maintain bidirectional links (parent↔child)
5. Broken references fail verification

## Git Workflow

### Branching
- `main`: Production-ready, approved content only
- `develop`: Integration branch for approved documents
- `feature/DOC_ID-short-description`: Per-document development

### Commits
- One commit per document per iteration
- Message format: `DOC_ID: Brief description`
- Include `Closes #ISSUE_NUM` if applicable

### Push Requirements
- Push only after verification passes
- Push to `feature/*` branch
- Create PR to `develop`
- No direct pushes to `main` or `develop`

### Merge
- PR requires 1 approval from domain reviewer
- PR requires verification checklist passed
- Squash merge to `develop`
- Release tags created from `main`

## Commit Standards

### Message Format
```
DOC_ID: Action - Brief description

Details:
- Change 1
- Change 2

Refs: #ISSUE_NUM
```

### Examples
```
TECH-001: Create - Chocolate processing plant layout specification

Details:
- Define minimum area requirements
- Specify zone segregation
- Reference BIS standards

Refs: #42
```

## Push Requirements

1. All verification categories pass
2. 00_MASTER_INDEX.md updated
3. CHANGELOG.md updated
4. No merge conflicts with `develop`
5. PR description references this manual section

## Response Format

Agents must respond with:
```
## Summary
[One sentence describing what was done]

## Document Modified
[Path to document]

## Verification Status
[Pass/Fail for each category]

## Next Recommended Document
[DOC_ID: Title] - [Brief rationale]

## Approval Required
Yes - awaiting human approval for next iteration
```

## One-Document-Per-Iteration Policy

**Strictly enforced.** Agents may not:
- Create multiple documents in one response
- Modify unrelated documents in same iteration
- Skip the approval wait step

Exceptions: None.

## Dependency Rules

### Document Dependencies
- Content documents depend on bootstrap documents
- Category index documents depend on all category members
- Cross-category references require both documents approved

### Update Propagation
When a document changes:
1. Update 00_MASTER_INDEX.md
2. Update CHANGELOG.md
3. Check dependent documents for impact
4. Flag impacted documents in OPEN_QUESTIONS.md if review needed

## Rules for Updating 00_MASTER_INDEX.md

1. Update on every document create/modify/archive
2. Modify only the relevant row(s)
3. Keep version, status, modified date current
4. Do not reorder without architecture approval
5. Commit with message: `INDEX: Update - [DOC_ID] [action]`

## Rules for Updating CHANGELOG.md

1. Add entry for every document change
2. Use format:
   ```markdown
   ## [VERSION] - YYYY-MM-DD
   ### DOC_ID - Action
   - Detail 1
   - Detail 2
   ```
3. Group by version
4. Maintain reverse chronological order

## Requirement to Ask for Approval

**Before starting any new document iteration, the agent must:**
1. Complete current iteration fully
2. Report with next document recommendation
3. Explicitly request approval
4. Wait for human confirmation

No exceptions. This is a governance requirement.
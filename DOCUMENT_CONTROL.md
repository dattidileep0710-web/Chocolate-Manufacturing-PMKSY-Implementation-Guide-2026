# Document Control Procedures

## Purpose

Define the lifecycle management, version control, and approval processes for all documents in this repository.

## Document Lifecycle

### States
| State | Description | Entry Criteria | Exit Criteria |
|-------|-------------|----------------|---------------|
| DRAFT | Initial creation, work in progress | Document created with required metadata | Author declares content complete |
| REVIEW | Under formal review | Author requests review; reviewers assigned | All reviewers approve or request changes |
| APPROVED | Finalized and approved | All reviewers approve; approver signs off | Superseded or archived |
| ARCHIVED | Superseded or obsolete | New version approved or document deprecated | Permanent (no exit) |

### State Transitions
```
DRAFT → REVIEW → APPROVED
  ↓         ↓
  → ARCHIVED (from any state)
```

## Version Control

### Version Numbering
Semantic Versioning (MAJOR.MINOR.PATCH):
- MAJOR: Breaking changes (structure, scope, fundamental approach)
- MINOR: New content, significant additions, non-breaking changes
- PATCH: Corrections, clarifications, formatting fixes

### Version Increment Rules
| Change Type | Version Increment |
|-------------|-------------------|
| New document | 1.0.0 |
| Content addition | MINOR |
| Content modification | MINOR |
| Error correction | PATCH |
| Formatting/style fix | PATCH |
| Structural change | MAJOR |
| Scheme interpretation change | MAJOR |

## Approval Workflow

### Roles
| Role | Responsibility |
|------|----------------|
| Author | Creates content, responds to review comments |
| Reviewers (min 2) | Technical/regulatory review, approve or request changes |
| Approver | Final sign-off authority |
| Documentation Lead | Process compliance, metadata, indexing |

### Review Process
1. Author creates document on `feature/DOC_ID-*` branch
2. Author opens PR to `develop` with "Ready for Review" label
3. Documentation Lead assigns reviewers (minimum 2)
4. Reviewers have 5 business days to review
5. Reviewers comment via PR; author responds and updates
6. When all reviewers approve, Approver reviews and merges
7. Squash merge to `develop`; version incremented
8. Documentation Lead updates 00_MASTER_INDEX.md

### Approval Criteria
- All 7 verification categories pass
- No unresolved reviewer comments
- Metadata complete and accurate
- Cross-references valid
- CHANGELOG.md entry added

## Change Management

### Minor Changes (PATCH/MINOR)
- Author makes changes on feature branch
- Follows standard PR process
- No architecture review needed

### Major Changes (MAJOR)
- Requires Architecture Change Request (ACR)
- ACR submitted as GitHub Issue with impact analysis
- Architecture Review Board evaluates within 10 business days
- If approved, architecture version incremented
- All dependent documents updated within 5 business days

## Document Identification

### Document ID Format
`[CATEGORY]-[NNN]` where:
- CATEGORY: 4-letter code (e.g., TECH, QLTY, FINM)
- NNN: Zero-padded sequence number

### Category Codes
| Code | Category |
|------|----------|
| ARCH | Architecture |
| AGNT | Agent Governance |
| CLDE | Claude Instructions |
| CHLG | Changelog |
| ROAD | Roadmap |
| DCTL | Document Control |
| VRFY | Verification |
| STYL | Style Guide |
| OQST | Open Questions |
| KGAP | Known Gaps |
| CNTR | Contributing |
| CONT | Contacts |
| GLOS | Glossary |
| ABBR | Abbreviations |
| LICN | License |
| SCHM | Scheme Overview |
| ELGB | Eligibility |
| TECH | Technical Specs |
| QLTY | Quality Standards |
| FINM | Financial Modeling |
| IMPL | Implementation |
| MONI | Monitoring |
| CMPL | Compliance |
| CASE | Case Studies |
| APPX | Appendices |

## Archival Process

1. Change status to `ARCHIVED` in front matter
2. Update `modified` date
3. Add note in CHANGELOG.md
4. Update 00_MASTER_INDEX.md (status column)
5. Move to `docs/archive/` if file system organization requires
6. PR with "Archive" label, standard review

## Record Keeping

All document control actions recorded in:
- CHANGELOG.md (content changes)
- Git history (structural changes)
- PR discussions (review decisions)
- 00_MASTER_INDEX.md (current state)

## Compliance

Non-compliance with document control procedures results in:
- Document returned to DRAFT
- Process gap logged in OPEN_QUESTIONS.md
- Root cause analysis required for repeat violations
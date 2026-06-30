# Known Gaps

## Overview

This document identifies acknowledged gaps in the current implementation guide — areas where content is incomplete, outdated, or pending external inputs. Gaps are tracked transparently to manage stakeholder expectations.

## Gap Format

| Field | Description |
|-------|-------------|
| ID | KGAP-YYYYMMDD-NNN |
| Category | Content area |
| Gap Description | What is missing |
| Root Cause | Why the gap exists |
| Impact | Affected documents/decisions |
| Severity | Critical / High / Medium / Low |
| Mitigation | Current workaround |
| Target Resolution | Planned closure date |
| Owner | Responsible party |

## Active Gaps

### KGAP-20260630-001
**Category**: Scheme Interpretation
**Gap Description**: No official PMKSY 2026-27 notification available; working from 2024 guidelines with anticipated updates
**Root Cause**: MoFPI typically releases updated guidelines in Q2 FY
**Impact**: All scheme-dependent documents (SCHM, ELGB, FINM, IMPL)
**Severity**: Critical
**Mitigation**: Base on 2024 guidelines; flag all interpretations as [PENDING 2026 NOTIFICATION]; monitor MoFPI portal weekly
**Target Resolution**: 2026-08-31 (expected notification release)
**Owner**: Scheme Expert

### KGAP-20260630-002
**Category**: Technical Standards
**Gap Description**: BIS standard IS 11555 for chocolate last updated 2020; potential revision pending
**Root Cause**: BIS revision cycle 3-5 years; no public draft available
**Impact**: QLTY-002, TECH-002, TECH-003
**Severity**: High
**Mitigation**: Use IS 11555:2020; add note "subject to revision"; monitor BIS work program
**Target Resolution**: 2026-12-31 (monitor for draft)
**Owner**: Quality/Regulatory Lead

### KGAP-20260630-003
**Category**: Financial Parameters
**Gap Description**: MoFPI cost norms for chocolate-specific equipment not published; using generic food processing norms
**Root Cause**: Cost norms updated periodically; chocolate niche category
**Impact**: FINM-001, FINM-003, FINM-004
**Severity**: High
**Mitigation**: Use generic norms with 15% contingency; document assumption; engage MoFPI for clarification
**Target Resolution**: 2026-09-30
**Owner**: Financial Analyst

### KGAP-20260630-004
**Category**: State-Level Data
**Gap Description**: State-specific incentives for chocolate manufacturing not consolidated
**Root Cause**: 28 states + 8 UTs; each with own food processing policy
**Impact**: FINM-003, FINM-004, ELGB-003
**Severity**: Medium
**Mitigation**: Cover top 10 cocoa-producing/consuming states initially; add others iteratively
**Target Resolution**: 2026-10-31
**Owner**: Financial Analyst

### KGAP-20260630-005
**Category**: Case Studies
**Gap Description**: No documented PMKSY chocolate manufacturing success stories in public domain
**Root Cause**: Scheme relatively new for this sector; commercial confidentiality
**Impact**: CASE-001, CASE-002, CASE-003
**Severity**: Medium
**Mitigation**: Use analogous food processing case studies; anonymize where needed; flag as illustrative
**Target Resolution**: 2026-11-30
**Owner**: Program Manager

### KGAP-20260630-006
**Category**: Environmental Regulations
**Gap Description**: State-level environmental clearance processes for food processing vary significantly
**Root Cause**: State Pollution Control Boards have delegated authority with variations
**Impact**: CMPL-002, IMPL-001
**Severity**: Medium
**Mitigation**: Provide generic framework; add state-specific annexes for priority states
**Target Resolution**: 2026-10-15
**Owner**: Compliance Lead

### KGAP-20260630-007
**Category**: Testing Infrastructure
**Gap Description**: NABL-accredited lab coverage for chocolate-specific tests (particle size, temper index, bloom stability) incomplete
**Root Cause**: Specialized testing capability concentrated in few locations
**Impact**: QLTY-003, QLTY-004, MONI-003
**Severity**: Low
**Mitigation**: List known accredited labs; note gaps; recommend in-house capability for critical tests
**Target Resolution**: 2026-11-30
**Owner**: Quality/Regulatory Lead

### KGAP-20260630-008
**Category**: Digital Monitoring
**Gap Description**: PMKSY's digital monitoring framework (PM Gati Shakti, MIS) integration specs not finalized
**Root Cause**: Central MIS platform under development
**Impact**: MONI-001, MONI-003, IMPL-002
**Severity**: Low
**Mitigation**: Design to common data standards (JSON/CSV); build adapter pattern for integration
**Target Resolution**: 2027-03-31
**Owner**: Technical Lead

### KGAP-20260630-009
**Category**: Export Compliance
**Gap Description**: Export-oriented chocolate units have additional APEDA/FSSAI requirements not fully mapped
**Root Cause**: Dual domestic/export compliance complex; APEDA guidelines evolving
**Impact**: CMPL-001, QLTY-001, QLTY-004
**Severity**: Low
**Mitigation**: Add export compliance annex; reference APEDA portal for current requirements
**Target Resolution**: 2026-12-31
**Owner**: Compliance Lead

### KGAP-20260630-010
**Category**: Climate Resilience
**Gap Description**: No PMKSY-specific guidance on climate-resilient chocolate manufacturing (cocoa supply, energy, water)
**Root Cause**: Emerging focus area; not in current scheme design
**Impact**: TECH-004, IMPL-004, MONI-002
**Severity**: Low
**Mitigation**: Include as optional enhancement section; align with National Mission on Sustainable Agriculture
**Target Resolution**: 2027-06-30
**Owner**: Technical Lead

## Closed Gaps

*None yet — first tracking cycle*

## Gap Review Process

1. **Weekly**: Review new gaps from document creation
2. **Bi-weekly**: Update status, adjust severity, check target dates
3. **Monthly**: Program Manager reviews Critical/High gaps with stakeholders
4. **Quarterly**: Full gap portfolio review; retire resolved, add new

## Gap-to-Question Conversion

If a gap requires external clarification → create entry in OPEN_QUESTIONS.md
If a question remains unresolved past target → convert to KNOWN_GAP
Both cross-referenced: `[KGAP-ID]` ↔ `[OQST-ID]`
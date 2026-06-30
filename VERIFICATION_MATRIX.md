# Verification Matrix

## Overview

Defines the verification requirements, methods, and acceptance criteria for all documents in the repository.

## Verification Categories

| Code | Category | Weight | Mandatory |
|------|----------|--------|-----------|
| SC | Scheme Compliance | Critical | Yes |
| TA | Technical Accuracy | Critical | Yes |
| RA | Regulatory Alignment | Critical | Yes |
| FV | Financial Validity | High | Yes* |
| XR | Cross-Reference Integrity | High | Yes |
| ST | Style Conformance | Medium | Yes |
| MC | Metadata Completeness | Medium | Yes |

*Financial Validity mandatory for financial documents only

## Verification Methods

### SC - Scheme Compliance
**Method**: Cross-reference every PMKSY claim with official MoFPI notification
**Tools**: Manual verification against gazette notifications, MoFPI website
**Evidence**: Citation in document with `[REF: NOTIFICATION_NO, DATE]`
**Pass Criteria**: 100% of PMKSY claims traced to official source

### TA - Technical Accuracy
**Method**: Validate specifications against BIS standards, equipment manufacturer data
**Tools**: BIS database, OEM specifications, industry handbooks
**Evidence**: Reference to standard number (e.g., IS 12345:2020)
**Pass Criteria**: All technical values match cited sources

### RA - Regulatory Alignment
**Method**: Check against FSSAI regulations, BIS standards, MoFPI guidelines, state laws
**Tools**: FSSAI portal, BIS portal, state government notifications
**Evidence**: Specific regulation/section citation
**Pass Criteria**: No conflicts with applicable regulations

### FV - Financial Validity
**Method**: Recalculate all formulas; verify assumptions against MoFPI guidelines
**Tools**: Spreadsheet recalculation, parameter sensitivity analysis
**Evidence**: Assumption table with source for each parameter
**Pass Criteria**: Calculations reproduce within 0.1%; assumptions documented

### XR - Cross-Reference Integrity
**Method**: Automated link validation + manual spot-check
**Tools**: Markdown link checker (CI), manual verification of [REF: DOC_ID]
**Evidence**: CI pass report
**Pass Criteria**: Zero broken internal/external links; all [REF:] resolve

### ST - Style Conformance
**Method**: Automated linting + manual review
**Tools**: markdownlint, custom style rules
**Evidence**: Lint report
**Pass Criteria**: Zero lint errors; warnings reviewed and accepted

### MC - Metadata Completeness
**Method**: Schema validation against front matter requirements
**Tools**: Custom validator script
**Evidence**: Validation report
**Pass Criteria**: All required fields present and correctly formatted

## Verification Checklist Template

```markdown
## Verification Report for DOC_ID

| Category | Status | Evidence | Notes |
|----------|--------|----------|-------|
| SC | Pass/Fail | [Link to citations] | |
| TA | Pass/Fail | [Link to standards] | |
| RA | Pass/Fail | [Link to regulations] | |
| FV | Pass/Fail/N/A | [Link to calculations] | |
| XR | Pass/Fail | [CI report link] | |
| ST | Pass/Fail | [Lint report link] | |
| MC | Pass/Fail | [Validation report] | |

**Overall**: Pass/Fail
**Verified By**: [Role/Name]
**Date**: YYYY-MM-DD
```

## Automated Verification (CI Pipeline)

### Required Checks
1. **markdownlint** - Style conformance
2. **link-checker** - Cross-reference integrity
3. **metadata-validator** - Metadata completeness
4. **citation-checker** - Scheme compliance (PMKSY citations)
5. **reference-resolver** - [REF: DOC_ID] resolution

### CI Configuration
```yaml
# .github/workflows/verify.yml
on: [pull_request]
jobs:
  verify:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - name: Run markdownlint
      - name: Check links
      - name: Validate metadata
      - name: Verify citations
      - name: Resolve references
```

## Verification Gates

### Pre-PR (Author Self-Check)
- [ ] All 7 categories self-verified
- [ ] Checklist completed and attached to PR
- [ ] No known open questions in document

### PR Review (Reviewer Verification)
- [ ] Independent verification of SC, TA, RA
- [ ] FV recalculation for financial docs
- [ ] XR, ST, MC via CI reports
- [ ] Approve only if all Pass

### Merge Gate (Automated)
- [ ] All CI checks green
- [ ] Minimum 2 reviewer approvals
- [ ] Approver approval
- [ ] No merge conflicts

## Exception Handling

### Conditional Pass
If a category cannot be fully verified (e.g., pending official clarification):
1. Document as [OPEN QUESTION] in OPEN_QUESTIONS.md
2. Mark category as "Conditional Pass - Pending [OQST-ID]"
3. Schedule re-verification within 30 days
4. Escalate if not resolved in 60 days

### Failed Verification
- Document returned to DRAFT
- Author must address all failures
- Re-verification required before re-submission
- Root cause logged in KNOWN_GAPS.md if systemic

## Metrics Tracking

Track per document:
- First-pass pass rate (target: >80%)
- Mean time to verification (target: <3 days)
- Verification cycle count (target: ≤2)
- Open question resolution time (target: <30 days)

## Continuous Improvement

Quarterly review of:
- Verification effectiveness (defect escape rate)
- Category weight adjustments
- Tool improvements
- Process bottlenecks
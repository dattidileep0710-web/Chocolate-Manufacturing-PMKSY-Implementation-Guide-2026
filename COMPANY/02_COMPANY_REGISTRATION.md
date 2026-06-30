---
doc_id: "CMPY-002"
title: "Company Registration and Incorporation Procedures"
version: "1.0.0"
status: "DRAFT"
owner: "Legal"
reviewers: ["Compliance Lead", "Financial Analyst"]
approver: "Program Director"
created: "2026-06-30"
modified: "2026-07-01"
tags: ["company", "registration", "incorporation", "mca", "legal"]
references: ["CMPY-001", "PMKS-004", "PMKS-001"]
---

# Company Registration and Incorporation Procedures

## Overview

This document provides a step-by-step procedural guide to registering and incorporating a Private Limited Company in India through the Ministry of Corporate Affairs (MCA) portal, specifically for a chocolate manufacturing unit in Andhra Pradesh seeking PMKSY support.

**OFFICIAL** — Company registration is governed by the Companies Act 2013 and administered by the Ministry of Corporate Affairs through the Registrar of Companies (ROC). The MCA21 portal and SPICe+ form are the official channels for incorporation.

> **SCOPE BOUNDARY**: This document covers **registration procedures only**. It does **not** address entity selection (see [CMPY-001: Company Formation and Legal Entity Selection](COMPANY/01_COMPANY_FORMATION.md)) or PMKSY eligibility (see [PMKS-004: Entity Eligibility](PMKSY_MASTER/04_ENTITY_ELIGIBILITY.md)).

---

## Pre-Registration Preparations

### Digital Signature Certificate (DSC)

**OFFICIAL** — DSC is mandatory for filing incorporation documents electronically through MCA.

| Aspect | Detail | Status |
|--------|--------|--------|
| Purpose | Digital authentication of filed documents | OFFICIAL |
| Issuing Authority | Certifying Authorities licensed by Controller of Certifying Authorities (CCA) | OFFICIAL |
| Class | Class 3 (for MCA filings) | OFFICIAL |
| Validity | 1-2 years (renewable) | OFFICIAL |
| Required For | All directors and authorized signatories | OFFICIAL |
| Cost | ₹1,000-₹3,000 per signature (varies by provider) | PROJECT ASSUMPTION |

**ENGINEERING RECOMMENDATION** — Obtain DSC for all proposed directors before starting name reservation to avoid delays.

### Director Identification Number (DIN)

**OFFICIAL** — DIN is mandatory for all directors of a proposed company.

| Aspect | Detail | Status |
|--------|--------|--------|
| Purpose | Unique identification for company directors | OFFICIAL |
| Application | Through MCA21 portal using SPICe+ form | OFFICIAL |
| Fee | Free (Nil) | OFFICIAL |
| Processing | Instant (if KYC documents are in order) | OFFICIAL |
| Validity | Lifetime (no renewal required) | OFFICIAL |

**PROJECT ASSUMPTION** — Directors can apply for DIN concurrently with SPICe+ filing or in advance.

### Registered Office Address

**OFFICIAL** — Every company must have a registered office in India.

| Requirement | Detail | Status |
|-------------|--------|--------|
| Address proof | Rent agreement / sale deed + electricity bill / tax receipt | OFFICIAL |
| NOC from owner | If premises are rented | OFFICIAL |
| Corporate Mailing | Official correspondence sent here | OFFICIAL |

**PROJECT ASSUMPTION** — For a chocolate manufacturing project, the registered office can be the factory address or a separate corporate office. Ensure the address is accessible for MCA correspondence.

---

## Name Reservation

### RUN (Reserve Unique Name) Process

**OFFICIAL** — Company name must be reserved through MCA before incorporation.

| Aspect | Detail | Status |
|--------|--------|--------|
| Form | SPICe+ Part A (or RUN form) | OFFICIAL |
| Name Options | Up to 6 preferred names in order of preference | OFFICIAL |
| Naming Guidelines | Must not be identical / too similar to existing companies; not violate trademark; not contain undesirable words | OFFICIAL |
| Fee | Free | OFFICIAL |
| Validity | 20 days from reservation | OFFICIAL |
| Re-reservation | Available upon expiry | PROJECT ASSUMPTION |

**ENGINEERING RECOMMENDATION** — For a chocolate manufacturing unit, propose names that:
- Include "Chocolate", "Cocoa", "Confectionery", or "Food Processing"
- End with appropriate suffix: "Private Limited" or "Pvt. Ltd."
- Are distinctive and not too similar to existing brands

**Example**: "Andhra Cocoa Chocolates Private Limited" or "Godavari Chocolate Works Private Limited"

### Name Approval Considerations

| Factor | Guidance | Status |
|--------|----------|--------|
| Uniqueness | Check MCA database before applying | PROJECT ASSUMPTION |
| Trademark | Verify trademark availability if brand name is important | PROJECT ASSUMPTION |
| Domain | Check domain availability for company website | PROJECT ASSUMPTION |
| MOA Object | Ensure name aligns with proposed MOA objects | ENGINEERING RECOMMENDATION |

---

## Memorandum and Articles of Association

### Memorandum of Association (MOA)

**OFFICIAL** — MOA defines the company's relationship with the outside world.

| Clause | Required Content | Status |
|--------|------------------|--------|
| Name clause | Company name | OFFICIAL |
| Registered office clause | State where registered office is located | OFFICIAL |
| Objects clause | Main objects and ancillary objects | OFFICIAL |
| Liability clause | Members' liability is limited | OFFICIAL |
| Capital clause | Authorized share capital | OFFICIAL |

**ENGINEERING RECOMMENDATION** — Objects clause for chocolate manufacturing should include:
1. Manufacturing, processing, packaging, and sale of chocolate, cocoa products, confectionery, and related food items
2. Procurement, trading, and export/import of cocoa beans, cocoa butter, cocoa mass, and chocolate ingredients
3. Any ancillary or incidental activities connected to the main business

**PROJECT ASSUMPTION** — Draft MOA with broad objects to avoid future amendments when expanding product lines or adding activities.

### Articles of Association (AOA)

**OFFICIAL** — AOA governs internal management of the company.

| Aspect | Detail | Status |
|--------|--------|--------|
| Purpose | Rules for board meetings, share transfers, dividends, etc. | OFFICIAL |
| Customization | Can be customized or use MCA model AOA | OFFICIAL |
| Filing | Filed with SPICe+ at incorporation | OFFICIAL |

**ENGINEERING RECOMMENDATION** — Use MCA model AOA with modifications for PMKSY-specific requirements:
- Share transfer restrictions (if needed for promoter control)
- Director appointment/removal procedures
- Quorum requirements for board meetings
- Bank account operation mandates

---

## SPICe+ Incorporation Process

### SPICe+ Form Overview

**OFFICIAL** — SPICe+ (Simplified Proforma forIncorporation Company) is the unified form for company incorporation, DIN, PAN, TAN, GST, EPF, ESI, and other registrations.

| Feature | Detail | Status |
|---------|--------|--------|
| Form | SPICe+ (5-in-1 or 2-in-1) | OFFICIAL |
| Portal | MCA21 (https://www.mca.gov.in) | OFFICIAL |
| Fee | Nil for incorporation; nominal for other services | OFFICIAL |
| Processing | Typically 3-7 days | PROJECT ASSUMPTION |
| Approval | ROC (Registrar of Companies) | OFFICIAL |

### SPICe+ Parts

| Part | Purpose | Status |
|------|---------|--------|
| Part A | Name reservation (if not already done) | OFFICIAL |
| Part B | Incorporation details, DIN, PAN, TAN, GST, EPF, ESI, bank account | OFFICIAL |

### Required Information for SPICe+

| Category | Details Required | Status |
|----------|-----------------|--------|
| Company details | Name, address, object, authorized capital | OFFICIAL |
| Director details | Name, DIN, PAN, address, nationality | OFFICIAL |
| Subscriber details | Name, address, shares subscribed | OFFICIAL |
| Registered office | Address proof | OFFICIAL |
| MOA/AOA | Attached as attachments | OFFICIAL |

### Step-by-Step SPICe+ Filing

**ENGINEERING RECOMMENDATION** — Follow this sequence:

1. **Pre-filing**:
   - Obtain DSC for all directors
   - Apply for DIN (if not already done)
   - Reserve company name via RUN or SPICe+ Part A
   - Prepare MOA and AOA
   - Gather address proof for registered office

2. **SPICe+ Part A** (if name not reserved):
   - Submit 6 preferred names
   - Pay fee (if applicable)
   - Wait for approval (1-2 days)

3. **SPICe+ Part B**:
   - Fill company details (CIN, state, category, sub-category)
   - Fill director details (DIN, PAN, address)
   - Fill subscriber details (shareholding pattern)
   - Attach MOA, AOA, address proof, DSC
   - Apply for DIN, PAN, TAN, GST, EPF, ESI simultaneously

4. **Post-filing**:
   - ROC reviews application (3-7 days)
   - May raise queries (SRN-based)
   - Respond to queries within 15 days (otherwise application rejected)
   - Upon approval, receive Certificate of Incorporation (COI) with CIN, PAN, TAN

### Common SPICe+ Queries and Rejections

| Query / Rejection Reason | Prevention | Status |
|--------------------------|------------|--------|
| Name not approved | Check MCA database before applying | PROJECT ASSUMPTION |
| Incomplete director details | Ensure DIN, PAN, address complete | PROJECT ASSUMPTION |
| MOA/AOA not aligned with name | Objects must match proposed business | PROJECT ASSUMPTION |
| Address proof inadequate | Provide latest utility bill + rent agreement | PROJECT ASSUMPTION |
| DSC not linked to DIN | Ensure DSC registered with MCA before filing | PROJECT ASSUMPTION |

---

## Post-Incorporation Requirements

### Certificate of Incorporation (COI)

**OFFICIAL** — Upon successful SPICe+ filing, ROC issues COI.

| Detail | Information | Status |
|--------|-------------|--------|
| Contains | CIN, Company name, Date of Incorporation, PAN, TAN | OFFICIAL |
| Validity | Permanent (until company struck off) | OFFICIAL |
| Copies | Digital copy available on MCA21 portal | OFFICIAL |
| Physical copy | Available on demand (additional fee) | PROJECT ASSUMPTION |

### PAN and TAN

**OFFICIAL** — PAN and TAN are auto-issued through SPICe+ if applied simultaneously.

| Card | Issuing Authority | Purpose | Status |
|------|-------------------|---------|--------|
| PAN | Income Tax Department | Tax identification | OFFICIAL |
| TAN | Income Tax Department | TDS deduction | OFFICIAL |

### GST Registration

**OFFICIAL** — GST registration is mandatory before commencing business.

| Aspect | Detail | Status |
|--------|--------|--------|
| Application | GST Portal (https://www.gst.gov.in) | OFFICIAL |
| Timeline | Typically 2-5 working days | PROJECT ASSUMPTION |
| Fee | Free | OFFICIAL |
| Documents | PAN, COI, address proof, bank details, promoter KYC | OFFICIAL |

**PROJECT ASSUMPTION** — For a ₹2 crore chocolate unit, GST registration should be obtained before procurement or production.

### Bank Account Opening

**OFFICIAL** — Company must open a current account in its name.

| Requirement | Detail | Status |
|-------------|--------|--------|
| Documents | COI, PAN, TAN, MOA/AOA, board resolution for account opening, KYC of directors | OFFICIAL |
| Bank selection | Choose bank with MSME / food processing experience | BANK PRACTICE |
| NABARD linkage | Opt for NABARD-linked bank if possible | BANK PRACTICE |

### AP-Specific Registrations

**REQUIRES RE-VERIFICATION** — After central incorporation, complete Andhra Pradesh-specific registrations:

| Registration | Authority | Priority | Status |
|-------------|-----------|----------|--------|
| Shops & Establishments | AP Labor Department | High | OFFICIAL |
| Professional Tax | AP Commercial Taxes | High | OFFICIAL |
| EPF Registration | EPFO (AP regional) | Medium | OFFICIAL (if applicable) |
| ESI Registration | ESIC (AP regional) | Medium | OFFICIAL (if applicable) |
| AP Factory License | AP Labor Department | High | OFFICIAL |

---

## Timeline and Costs

### Typical Timeline

| Phase | Duration | Status |
|-------|----------|--------|
| DSC procurement | 1-2 days | PROJECT ASSUMPTION |
| DIN application | 1 day | OFFICIAL |
| Name reservation | 1-2 days | OFFICIAL |
| SPICe+ filing and approval | 3-7 days | PROJECT ASSUMPTION |
| GST registration | 2-5 days | PROJECT ASSUMPTION |
| Bank account opening | 7-14 days | BANK PRACTICE |
| AP registrations | 2-4 weeks | PROJECT ASSUMPTION |

**PROJECT ASSUMPTION** — Total incorporation time: approximately 4-6 weeks from start to operational readiness.

### Typical Costs

| Item | Cost Range (₹) | Status |
|------|----------------|--------|
| DSC (2 directors) | 2,000 - 6,000 | PROJECT ASSUMPTION |
| DIN (if separate) | 0 (free via SPICe+) | OFFICIAL |
| Name reservation | 0 | OFFICIAL |
| SPICe+ | 0 (incorporation free) | OFFICIAL |
| MOA/AOA drafting | 5,000 - 20,000 | PROJECT ASSUMPTION |
| GST registration | 0 | OFFICIAL |
| Bank account opening | 0 | BANK PRACTICE |
| Professional fees (CA/CS) | 15,000 - 50,000 | PROJECT ASSUMPTION |

**PROJECT ASSUMPTION** — Total incorporation cost: approximately ₹25,000 - ₹80,000 depending on professional fees and complexity.

---

## Common Registration Pitfalls

### Pitfall 1: Name Rejection
- **Problem**: Proposed name rejected by ROC for being too similar or undesirable
- **Prevention**: Check MCA database thoroughly; avoid generic names; ensure name matches proposed business activity
- **Status**: PROJECT ASSUMPTION

### Pitfall 2: Director DIN Issues
- **Problem**: DIN not obtained or not linked to DSC before filing
- **Prevention**: Apply for DIN in advance; verify DIN-DSC linkage on MCA portal
- **Status**: PROJECT ASSUMPTION

### Pitfall 3: MOA Objects Too Narrow
- **Problem**: MOA object clause restricts business activities
- **Prevention**: Draft broad objects covering all planned and potential activities
- **Status**: ENGINEERING RECOMMENDATION

### Pitfall 4: Address Proof Inadequate
- **Problem**: ROC rejects registered office address proof
- **Prevention**: Provide recent utility bill + registered rent agreement + NOC
- **Status**: PROJECT ASSUMPTION

### Pitfall 5: Delayed GST Registration
- **Problem**: Commencing business without GST registration
- **Prevention**: Apply for GST concurrently with incorporation or immediately after
- **Status**: OFFICIAL — GST registration mandatory before business commencement

### Pitfall 6: Ignoring State-Specific Registrations
- **Problem**: Focusing only on central MCA incorporation, neglecting AP-specific requirements
- **Prevention**: Create checklist of AP registrations; execute in parallel
- **Status**: PROJECT ASSUMPTION

---

## Relationship with PMKSY

### PMKSY Application and Company Registration Sequence

**PROJECT ASSUMPTION** — Optimal sequence:

```
1. Reserve company name (MCA)
         ↓
2. Incorporate company (MCA - SPICe+)
         ↓
3. Open bank account
         ↓
4. Obtain GST registration
         ↓
5. Complete AP registrations
         ↓
6. Prepare PMKSY application with company documents
```

**ENGINEERING RECOMMENDATION** — Complete company registration before engaging PMKSY consultant. A registered entity with valid documents strengthens the application.

### Documents Required for PMKSY (from Registration)

| Document | PMKSY Use | Status |
|----------|-----------|--------|
| Certificate of Incorporation | Entity eligibility proof | OFFICIAL |
| PAN | Entity identification | OFFICIAL |
| TAN | TDS compliance | OFFICIAL |
| MOA / AOA | Entity charter | OFFICIAL |
| Bank account proof | Financial account verification | OFFICIAL |
| GST registration | Tax compliance | OFFICIAL |

See [PMKS-007: Required Documents](PMKSY_MASTER/07_REQUIRED_DOCUMENTS.md) for complete PMKSY document checklist.

---

## Cross-References

| This Document References | Document ID | Title | Relationship |
|-------------------------|-------------|-------|--------------|
| Company Formation | [CMPY-001](COMPANY/01_COMPANY_FORMATION.md) | Company Formation and Legal Entity Selection | Predecessor — entity selection |
| Entity Eligibility | [PMKS-004](PMKSY_MASTER/04_ENTITY_ELIGIBILITY.md) | Entity Eligibility | PMKSY-specific entity requirements |
| Scheme Overview | [PMKS-001](PMKSY_MASTER/01_SCHEME_OVERVIEW.md) | Scheme Overview | Scheme context |
| Required Documents | [PMKS-007](PMKSY_MASTER/07_REQUIRED_DOCUMENTS.md) | Required Documents | Registration documents feed into PMKSY |
| Abbreviations | [ABBR-001](../ABBREVIATIONS.md) | Abbreviations | Terminology reference |
| Glossary | [GLOS-001](../GLOSSARY.md) | Glossary | Definition reference |
| Open Questions | [OQST-001](../OPEN_QUESTIONS.md) | Open Questions | Clarification tracking |
| Known Gaps | [KGAP-001](../KNOWN_GAPS.md) | Known Gaps | Gap tracking |

---

## Official References

### Primary Sources (OFFICIAL)

| Source | Document | Access Date | Status |
|--------|----------|-------------|--------|
| MCA | Companies Act 2013 | 2026-07-01 | Active |
| MCA | SPICe+ Form and User Manual | 2026-07-01 | Active |
| MCA | MCA21 Portal | 2026-07-01 | Active |
| CCA | Digital Signature Certificate Rules | 2026-07-01 | Active |
| Income Tax Department | PAN / TAN Rules | 2026-07-01 | Active |
| GST Portal | GST Registration Rules | 2026-07-01 | Active |
| AP Labor Department | AP Shops & Establishments Act | 2026-07-01 | Active |
| AP Commercial Taxes | AP Professional Tax Rules | 2026-07-01 | Active |

### Secondary Sources

| Source | Usage | Basis |
|--------|-------|-------|
| Company Secretaries | Registration practices | PROJECT ASSUMPTION |
| Chartered Accountants | Tax and GST implications | PROJECT ASSUMPTION |

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0.0 | 2026-06-30 | Legal | Initial creation — step-by-step company registration guide for PMKSY chocolate manufacturing projects |

---

## Document Control

**Document Owner**: Legal  
**Review Cycle**: Annually, or upon MCA rule changes  
**Next Review Due**: 2027-06-30  
**Archive When**: Superseded by updated company law or MCA procedural changes

---
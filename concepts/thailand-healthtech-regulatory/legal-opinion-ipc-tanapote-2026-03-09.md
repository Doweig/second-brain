---
type: legal-research
date: 2026-03-09
source: pdf-extraction
tags: [legal, corporate-structure, clinic-licensing, pdpa, medical-device, telehealth]
people: [art-tanapote, guillaume-verbal, art-chawapon-kidhirunkul]
companies: [bodycypher, ipc-international, acclime-thailand, n-health]
status: reviewed
---

# Legal Opinion — IPC International (via Tanapote)

**Date:** 9 March 2026
**Prepared for:** [[guillaume-verbal|Guillaume Verbal]] (William)
**Firm:** [[ipc-international|IPC International]] (instructed by [[art-tanapote|Tanapote]])
**Subject:** Corporate formation, foreign business restrictions, healthcare regulation, data protection, and licensing for a telehealth + wellness supplement business in Thailand.

## 1. Business Model (As Described to Counsel)

- Proprietary app — patients access remotely, no physical premises
- Nurse dispatched to patient's home for blood collection
- Samples sent to contracted licensed lab ([[n-health|N Health]])
- AI/algorithmic analysis generates report
- Licensed physician reviews and confirms before patient sees it
- Doctor recommends supplements if needed → fulfilled via contracted stores
- **Key:** Entire service chain is remote — no patient visits to company premises

## 2. Corporate Structure

### Recommended: Thai Private Limited Company
- 51% Thai / 49% foreign shareholding to avoid Foreign Business License requirement
- Proposed: Thai Shareholder 1 (26%) + Thai Shareholder 2 (25%) + Guillaume (49%)
- Minimum 3 promoters at registration, 3 shareholders maintained throughout
- Registered office address in Thailand required
- MOA + AOA filed with DBD

### ⚠️ Nominee Warning
Thai shareholders must be **genuine investors with real economic stakes**. Nominee arrangements strictly prohibited. Special class shares, weighted voting, or mechanisms transferring effective control to foreigner while maintaining Thai majority will attract scrutiny from Revenue Department and DBD.

### Work Permit & Visa
- Non-Immigrant Visa Type B required
- Work Permit from Department of Employment required before commencing work
- Annual renewal

## 3. Healthcare Regulation

### Clinic License: Probably NOT Required
IPC concurs with Tanapote's view — no clinic license needed because:
- No physical premises where patients attend
- Clinical functions (blood collection, lab analysis, medical review) performed by separately licensed contracted entities
- App performs data analysis, not clinical diagnosis — output reviewed by licensed doctor

### ⚠️ Regulatory Uncertainty Caveat
Evolving area. National Health Commission and Medical Council issuing new telemedicine guidelines. **Strongly recommended:** Seek formal or informal ruling from Department of Health Service Support (กรมสนับสนุนบริการสุขภาพ) before commencing operations.

### Nurse Requirements
- Valid nursing license from Nursing and Midwifery Council of Thailand
- Documented contractual arrangement assigning clinical responsibility
- Periodic licence validity confirmation required

### Lab Requirements
- Must be licensed under Laboratory Quality Standards (Dept of Medical Sciences / Medical Technology Council)
- Contract must delineate responsibility for sample integrity, result accuracy, data handling

### Physician Requirements
- Valid medical licence from Medical Council of Thailand
- Doctor must exercise **independent clinical judgement** — not just rubber-stamping AI output
- Supplement recommendations within physician's legal scope of practice
- Telemedicine guidelines compliance if applicable

## 4. The App — Medical Device Risk

### Software-as-Medical-Device (SaMD) Classification
Thailand has no standalone AI healthcare statute, but Medical Device Act B.E. 2562 (2019) applies.

**If app provides clinical diagnostic outputs → likely classified as medical device → requires Thai FDA registration.**

**If app provides analytical summaries reviewed by physician → stronger argument it's outside MDA scope.**

### ⚠️ Recommendation
Consult Thai FDA for pre-market classification ruling. Design app as clinical decision **support** tool for physician, not standalone diagnostic. Document physician's independent review in patient record.

### IP Protection
- Software protected as literary work under Copyright Act (automatic, but register with DIP)
- Register trademarks under Trademark Act
- Consider patent protection for novel app elements

## 5. Supplements Regulation

### Dual Classification Risk
Vitamins/supplements classified as either **food products** (Food Act) or **drug products** (Drug Act) depending on composition, concentration, and claims.

### Requirements
- All products must be registered with Thai FDA under appropriate category
- Thai language labelling required
- Compliant storage and transport
- If any products are prescription drugs → pharmacy licence required → only licensed pharmacists or physicians may dispense

### Recommended Structure
- Contracted stores hold appropriate retail/wholesale pharmaceutical licences
- Client's role as fulfilment intermediary (not direct seller) clearly documented

## 6. Data Protection (PDPA)

### Health Data = Sensitive Personal Data
Blood test results and health data require **explicit consent** under Section 26 PDPA.

### Obligations
- Published Privacy Policy
- Explicit informed consent for health data collection/use
- Technical + organisational security measures
- Data Protection Officer (DPO) if large-scale systematic processing of sensitive data
- Written Data Processing Agreements with all contractors (lab, doctors, nurses, stores)
- Data subject rights (access, rectification, erasure, portability)
- 72-hour breach notification to PDPC and affected subjects
- Cross-border transfer protections if servers/processors outside Thailand

### Electronic Transactions Act
Electronic records and e-signatures legally valid under ETA if requirements met.

---

## Key Comparison: IPC Opinion vs. Prior Tanapote Advice (Feb 2026)

| Topic | Tanapote (Feb) | IPC Opinion (Mar) |
|-------|---------------|-------------------|
| BOI | Not viable now (needs ฿1.5M/yr Thai IT salaries) | Not addressed |
| Entity structure | Thai company, wife as majority shareholder | Thai company, 26/25/49 split — no mention of wife specifically |
| Nominee risk | Not flagged explicitly | **Explicit warning** — genuine investors required, scrutiny flagged |
| Clinic license | Still researching | **Probably not required** — but seek formal ruling before launch |
| Medical device (AI app) | Not addressed | **Major risk flagged** — SaMD classification, consult Thai FDA |
| Supplements regulation | Not addressed | **Detailed** — dual classification, pharmacy licensing, FDA registration |
| PDPA | Not addressed | **Comprehensive** — DPO, DPAs, breach notification, consent requirements |
| Work permit | Not addressed | Required — Non-Immigrant B + work permit |

### What IPC Adds That Tanapote Didn't Cover
1. **Medical Device Act risk** for the AI app — this is the biggest new finding
2. **Supplements regulatory path** — food vs drug classification, pharmacy licensing
3. **PDPA compliance framework** — explicit consent, DPO, breach notification
4. **Nominee shareholder warning** — specific and emphatic
5. **Nurse licensing requirements** — contractual and periodic verification
6. **IP protection** recommendations for the software

### What's Still Missing (Neither Opinion Covers)
- BOI timing and pathway (Tanapote said later)
- Dual-entity (tech + clinic) structure details
- [[art-chawapon-kidhirunkul|Dr. C]] equity formalization mechanics
- Specific supplement licensing steps for an e-commerce/marketplace model
- [[acclime-thailand|Acclime]] opinion (questionnaire sent, awaiting response)

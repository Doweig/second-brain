---
type: legal-research
date: 2021-01-18
source: pdf-extraction
tags: [telemedicine, moph, regulation, clinic-licensing, medical-facility-act]
people: [art-chawapon-kidhirunkul]
companies: [bodycypher, prewell-clinic]
status: raw
---

# MOPH Notification — Standards for Telemedicine Services B.E. 2564 (2021)

**Full title:** ประกาศกระทรวงสาธารณสุข เรื่อง มาตรฐานการให้บริการของสถานพยาบาลโดยใช้ระบบบริการการแพทย์ทางไกล พ.ศ. 2564
**Published:** Royal Gazette, Volume 138, Special Section 23 Ngor, 1 February 2021 (B.E. 2564)
**Authority:** Sections 6 and 15 of the Medical Facility Act B.E. 2541 (1998)
**Signed by:** Sathit Pitutecha, Deputy Minister of Public Health (acting for the Minister)
**Source:** [[art-chawapon-kidhirunkul|Dr. Chawapon]] (provided March 2026)

---

## Key Definitions

**Telemedicine service** (การบริการการแพทย์ทางไกล): Medical and public health services provided by a medical facility to patients through licensed practitioners via a telemedicine system, for: consultation, examination, diagnosis, treatment, nursing, disease prevention, health promotion, and physical rehabilitation.

**Telemedicine system** (ระบบบริการการแพทย์ทางไกล): A system using digital technology for remote medical/public health services via transmission of audio-visual data or other methods.

---

## Requirements (Articles 4-10)

### Article 4 — Core Requirements
Facilities wishing to offer telemedicine must have:
1. **Sufficient licensed practitioners** — no impact on primary in-person services
2. **Adequate telemedicine technology** — communications equipment enabling clear two-way communication between provider and patient, with information security standards

### Article 5 — Registration Requirement
Must submit Form ส.พ.16 (application to change medical facility operations) to add telemedicine services. This is a formal application to the licensing authority.

### Article 6 — Liability
The licensee, operator, and treating practitioner are liable for service outcomes.

**Exception:** Consultation between practitioners (same or different professions) where no patient treatment occurs is NOT considered telemedicine under this notification.

### Article 7 — Documentation
Must maintain: registration records, data recording, service outcome reports, verification/confirmation of all telemedicine service processes.

### Article 8 — Professional Compliance
Must ensure all telemedicine practitioners comply with their professional practice laws and other relevant laws.

### Article 9 — Informed Consent
Must provide patients with: detailed pre-service information, step-by-step procedures, potential outcomes, and risks of telemedicine services.

### Article 10 — Technology Standards
Must have adequate and appropriate technology, medical equipment, and communications, including risk management and error control for communications technology per other relevant laws.

### Article 11 — Transitional Provision
Facilities already offering telemedicine before this notification must submit the registration application within 90 days.

---

## Application Process for Adding Telemedicine

### Where to Submit

| Facility Type | Location | Submit To |
|--------------|----------|-----------|
| Hospital (inpatient) | Bangkok | Dept. of Health Service Support (กรมสนับสนุนบริการสุขภาพ) |
| Hospital (inpatient) | Provinces | Provincial Public Health Office → forwarded to DHSS |
| Clinic (outpatient) | Bangkok | Dept. of Health Service Support |
| Clinic (outpatient) | Provinces | Provincial Public Health Office |

### Required Documents

1. **Form ส.พ.16** — Application to change medical facility operations
2. **Form ส.พ.10** — Application to change medical facility license details
3. **Practitioner certification letter** — Certifying telemedicine practitioners (names + license numbers)
4. **Standard Operating Procedures (SOP)** — Covering:
   - Pre-service explanation process
   - Registration procedures
   - Data recording
   - Service outcome reporting
   - Verification/confirmation of all telemedicine processes
5. **IT system documentation** — Per the IT assessment form (see below)

### IT Assessment Form (แบบประเมินระบบเทคโนโลยีสารสนเทศ)

If the facility has **ISO 27001 certification** or equivalent → attach certificate, done.

If using **outsourced IT systems** → attach service contract + provider's standards documentation.

Otherwise, must demonstrate compliance across 5 areas:

1. **IT Structure & Roles**
   - IT management team (executive + IT staff)
   - IT policy and operational plan
   - Standards (data standards, data coding, operational standards, patient privacy, network standards, physical/environmental standards)

2. **IT Risk Management**
   - Written risk management plan
   - Implementation evidence
   - Risk assessment results

3. **IT Security Management**
   - Security policies and procedures
   - Access controls (only current treating staff access patient data)
   - Patient confidentiality protections
   - Staff awareness of policies

4. **IT Resource Capacity**
   - Capacity management plan for Hardware, Software, Network

5. **Data Center Management**
   - If outsourced → attach service contract + provider standards
   - If in-house:
     - Secure data center
     - Physical security from unauthorized access
     - Fire protection (smoke detection, alarms, fire suppression)
     - Data/system protection (UPS, RAID, redundant power supply, redundant servers)

---

## Practitioner Certification Template (From DOCX)

A sample letter template was provided (Form: หนังสือรับรองผู้ประกอบวิชาชีพที่ให้บริการการแพทย์ทางไกลในคลินิก) certifying that named practitioners with their license numbers are authorized to provide telemedicine services at the clinic. Must be signed by both the facility licensee and the facility operator, with company seal if applicable.

---

## BodyCypher Implications

1. **Telemedicine requires a licensed medical facility.** Dr. C's [[prewell-clinic|Prewell clinic]] can apply for telemedicine service addition using Forms ส.พ.16 and ส.พ.10.

2. **The application is procedural, not discretionary.** Submit forms + SOP + IT assessment + practitioner certification → approval.

3. **Article 6 exception is useful:** Doctor-to-doctor consultation (e.g., Dr. C consulting with another specialist about a patient's results) is NOT considered telemedicine. Only direct patient-facing consultations count.

4. **IT assessment requirements** are manageable for a modern cloud-based platform. ISO 27001 certification or documented security policies would satisfy the IT component.

5. **SOP documentation** must be prepared for the entire telemedicine workflow — from patient registration through result delivery. This aligns with what [[bodycypher|BodyCypher]] needs to build anyway.

6. **The telemedicine communication software itself is NOT a medical device** (confirmed by the SaMD guide, exemption #13).

---

*Raw PDFs and DOCX preserved in vault/2026-03/raw/*

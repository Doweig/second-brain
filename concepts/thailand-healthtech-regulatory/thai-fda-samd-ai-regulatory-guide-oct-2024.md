---
type: legal-research
date: 2024-10-01
source: pdf-extraction
tags: [thai-fda, samd, ai-medical-device, classification, imdrf, regulatory, medical-device]
people: [art-chawapon-kidhirunkul]
companies: [bodycypher]
status: raw
---

# Thai FDA — Guide on Regulatory Oversight of Software and AI as Medical Devices

**Published:** October 2024 (B.E. 2567)
**Issuing body:** Medical Device Control Division (กองควบคุมเครื่องมือแพทย์), Thai FDA (สำนักงานคณะกรรมการอาหารและยา)
**Document ID:** Non-IVD_G_SMD_02
**Pages:** 85
**Source:** [[art-chawapon-kidhirunkul|Dr. Chawapon]] (provided March 2026)

---

## Overview

This is the official Thai FDA guide for regulating software and AI as medical devices. It shifts Thailand's regulatory approach from policy-based to **risk-based** control, aligning with the IMDRF (International Medical Device Regulators Forum) framework.

Key change: Software/AI previously classified as "general medical devices" (เครื่องมือแพทย์ทั่วไป) now falls into either:
- **Type 1** — notification required (เครื่องมือแพทย์ที่ต้องจดแจ้ง)
- **Type 2-3** — detailed listing required (เครื่องมือแพทย์ที่ต้องแจ้งรายการละเอียด)

---

## Table of Contents (Original)

1. Criteria for screening software/AI that qualifies as medical device (p.4)
2. Risk assessment and classification criteria (p.10)
3. Evidence and documentation for authorization application (p.14)
4. Guidelines for modifications/changes (p.70)
5. Quality system for manufacturing/import facilities (p.73)
6. Advertising rules specific to SaMD/AI (p.76)
7. Post-market surveillance and risk management (p.77)
8. Cybersecurity (p.80)
9. Appendix (p.84)

---

## 1. Screening Criteria — Is It a Medical Device?

### Decision Flowchart

The Thai FDA uses a flowchart based on **intended medical purpose** (วัตถุประสงค์ทางการแพทย์):

```
Software
  ├── Has medical purpose? → YES → Medical device
  │   ├── Embedded in hardware → Medical device (regulated with hardware)
  │   ├── Standalone / mobile app → Classified per IMDRF matrix below
  │   └── Accessory to medical device → Medical device
  └── No medical purpose → NOT a medical device
```

### Legal Definition of "Medical Purpose"

Per Section 4 of the Medical Devices Act B.E. 2551 (2008), as amended B.E. 2562 (2019), software qualifies if the manufacturer intends it for:

- (a) Diagnosis, prevention, monitoring, treatment, alleviation, or cure of disease
- (b) Diagnosis, monitoring, treatment, alleviation, or cure of injury
- (c) Investigation, replacement, modification, support of anatomy or physiological processes
- (d) Life support or sustaining
- (e) Contraception or fertility assistance
- (f) Disability assistance or compensation
- (g) Providing information from body specimens for medical/diagnostic purposes
- (h) Sterilization/disinfection of medical devices

If software meets ANY of these → it is a medical device.

### Examples — Software That IS a Medical Device

- Software to receive/check physiological signals to detect early non-severe sleep apnea
- Software to analyze photos of moles to identify abnormal moles indicating skin cancer risk
- Software to analyze ECG data to assist in diagnosing arrhythmias
- Software for cognitive behavioral therapy as part of emergency management for substance abuse patients
- Software to analyze skin lesion images for classification of serious vs. benign lesions
- Software to collect/analyze vital sign readings to triage patients for MACE risk in ER
- **Clinical Decision Support Software (CDSS)** — standalone (including mobile, cloud, web-based)

### Examples — Software That Is NOT a Medical Device (19 Examples)

| # | Description |
|---|-------------|
| 1 | Software solely for displaying/publishing medical information; does not analyze patient-specific data; provides no recommendations for prevention, diagnosis, treatment |
| 2 | Patient appointment and surgery scheduling software |
| 3 | Patient billing software |
| 4 | Simple clinical calculators (BMI, fluid volumes, unit conversions mmol/L ↔ mg/dL) |
| 5 | Laboratory Information Management Systems (LIMS) / Laboratory Information Systems (LIS) |
| 6 | Hospital Information Systems (HIS) |
| 7 | Software digitizing clinical decision steps WITHOUT analyzing patient data |
| 8 | Software displaying approved-label data for medicines/devices (dosing, quantity) |
| 9 | Diet/exercise tracking for diabetes management WITHOUT connecting to blood glucose device |
| 10 | Daily log software (pain scores, bowel function) |
| 11 | EHR software for display/receive/compile/store patient records WITHOUT processing or analysis |
| 12 | Software providing medical reference information (clinical guidelines) for training/QA |
| 13 | **Telemedicine communication software** — enables remote consultation/collaboration between physicians or with patients |
| 14 | Health promotion surveys/questionnaires showing appropriate next steps based on user-reported symptoms — general wellness only |
| 15 | Menstrual cycle tracking calendar |
| 16 | IVF treatment cycle progress tracking calendar |
| 17 | Drug dosage calculators using established clinical methods |
| 18 | Library/reference software matching patient data to established clinical criteria (e.g., diabetes diagnosis from blood glucose readings) |
| 19 | Display-only software developed by third parties to retrieve and show data from medical devices |

**Critical for [[bodycypher|BodyCypher]]:** Item #13 confirms telemedicine communication software is NOT a medical device. Item #18 (library/reference matching patient data to clinical criteria) is potentially relevant — a system that matches blood test values to reference ranges and just displays them could fall here. BUT if the software goes further and provides recommendations or analysis, it likely crosses into SaMD territory.

---

## 2. Risk Classification — IMDRF Matrix

Thailand uses the IMDRF SaMD risk categorization framework. Two dimensions:

### Significance of Information (ความสำคัญของข้อมูล)

| Level | Description |
|-------|-------------|
| **Treat or Diagnose** | Information used to directly treat or make a diagnosis |
| **Drive clinical management** | Information that directly drives/determines clinical management decisions |
| **Inform clinical management** | Information that supports clinical decisions but does not alone determine management |

### State of Healthcare Situation (สถานการณ์ด้านสุขภาพ)

| Level | Description |
|-------|-------------|
| **Critical** (วิกฤต) | Condition where errors could be life-threatening |
| **Serious** (รุนแรง) | Condition where errors could cause severe health deterioration or permanent disability |
| **Non-serious** (ไม่รุนแรง) | Condition where errors are unlikely to cause major harm |

### The Matrix

| Significance ↓ \ Situation → | Critical | Serious | Non-serious |
|------------------------------|----------|---------|-------------|
| **Treat or Diagnose** | Type 4 (IV) | Type 4 (IV) | Type 3 (III) |
| **Drive clinical management** | Type 4 (IV) | Type 3 (III) | Type 2 (II) |
| **Inform clinical management** | Type 3 (III) | Type 2 (II) | Type 1 (I) |

### Mapping to Thai Regulatory Categories

| IMDRF Category | Thai Type | Regulatory Requirement |
|----------------|-----------|----------------------|
| I | Type 1 (ประเภท 1) | Notification (จดแจ้ง) |
| II | Type 2 (ประเภท 2) | Detailed listing (แจ้งรายการละเอียด) |
| III | Type 3 (ประเภท 3) | Detailed listing (แจ้งรายการละเอียด) |
| IV | Type 4 (ประเภท 4) | Highest regulatory control |

### Classification Examples

| Software | Significance | Situation | → Category |
|----------|-------------|-----------|-----------|
| Acute stroke diagnosis AI | Treat/Diagnose | Critical | **Type 4** |
| Arrhythmia alert system (life-threatening) | Drive clinical mgmt | Critical | **Type 4** |
| Radiation therapy QA software | Treat/Diagnose | Serious | **Type 4** |
| Sleep apnea signal detection (non-severe) | Drive clinical mgmt | Non-serious | **Type 2** |
| Skin lesion analysis (mole screening) | Inform/Drive | Non-serious/Serious | **Type 2** |
| Diabetic retinopathy screening AI | Drive/Inform | Non-serious→Serious | **Type 2** |
| Intraocular lens power calculator | Inform clinical mgmt | Non-serious | **Type 1** |

---

## BodyCypher Classification Analysis

**BodyCypher's AI blood test interpretation:**
- **Significance:** The AI analyzes blood test results and provides health insights/recommendations → this is either "Drive clinical management" or "Inform clinical management"
- **Situation:** Blood biomarker optimization for generally healthy people → "Non-serious" in most cases
- **With doctor review:** If positioned as informing the doctor's clinical management (doctor makes the decision) → "Inform clinical management"

**Most likely classification:**
- If "Inform clinical management" + "Non-serious" → **Type 1** (notification only)
- If "Drive clinical management" + "Non-serious" → **Type 2** (detailed listing)
- If "Inform clinical management" + "Serious" (some biomarkers could flag serious conditions) → **Type 2**

**Key positioning strategy:** Frame as "informing" rather than "driving" clinical management. The doctor reviews and makes independent decisions. The AI provides supporting information. This pushes toward Type 1 or Type 2, avoiding the heavier Type 3-4 requirements.

---

## Key Requirements by Type

### Type 1 (Notification)
- Register establishment with Thai FDA
- Submit notification (จดแจ้ง)
- Maintain quality system
- Post-market surveillance

### Type 2-3 (Detailed Listing)
- All Type 1 requirements plus:
- ISO 13485:2016 compliance
- Clinical evaluation documentation
- AI training dataset disclosure
- Cybersecurity documentation
- Registration through SKYNET e-submission portal

### Documentation Required (all types)
- Intended use description
- Software architecture/design documentation
- Risk management per ISO 14971
- Software lifecycle documentation per IEC 62304
- Clinical evaluation
- Cybersecurity assessment
- Labeling/instructions for use

---

## Additional Topics Covered (Summary)

### Advertising (Section 6)
Special advertising rules for SaMD/AI. Claims must be supported by clinical evidence. No misleading claims about AI capabilities.

### Post-Market Surveillance (Section 7)
Mandatory adverse event reporting. Continuous monitoring of AI performance. Plan for handling AI model updates/retraining.

### Cybersecurity (Section 8)
Required cybersecurity documentation. Data protection measures. Vulnerability management plan. Network security requirements.

---

## Definitions (Thai → English)

| Thai Term | English |
|-----------|---------|
| ซอฟต์แวร์ที่ใช้งานโดยลำพัง (Standalone software) | Software/mobile apps used independently, not controlling medical device hardware |
| ซอฟต์แวร์ที่ฝังในเครื่องมือแพทย์ (Embedded software) | Software embedded in medical device hardware |
| ปัญญาประดิษฐ์ (AI) | Artificial intelligence |
| เครื่องมือแพทย์ปัญญาประดิษฐ์ (AI-MD) | AI medical device — AI with medical intended use |
| การประเมินทางคลินิก (Clinical evaluation) | Clinical evaluation of safety/efficacy |
| ซอฟต์แวร์สนับสนุนการตัดสินใจทางคลินิก (CDSS) | Clinical Decision Support Software |
| สถานการณ์วิกฤต (Critical situation) | May cause permanent disability or death |
| สถานการณ์รุนแรง (Serious situation) | May cause severe health deterioration |
| สถานการณ์ไม่รุนแรง (Non-serious situation) | Unlikely to cause major harm |

---

*Raw PDF preserved in vault/2026-03/raw/*

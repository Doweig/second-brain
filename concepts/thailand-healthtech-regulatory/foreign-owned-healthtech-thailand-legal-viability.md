---
type: legal-research
date: 2026-03-11
source: manual
tags: [fba, boi, dual-entity, samd, thai-fda, pdpa, corporate-structure, foreign-ownership]
people: [art-tanapote, art-chawapon-kidhirunkul]
companies: [bodycypher, ipc-international]
status: raw
---

# Foreign-owned healthtech in Thailand: legal viability analysis

*Updated March 2026*

---

A majority-foreign-owned healthtech company can legally operate in Thailand, but only through specific legal pathways — most practically via BOI promotion under Category 8.1.1, which permits 100% foreign ownership and exempts the company from Foreign Business Act restrictions for promoted activities. The path is viable but narrow: supplement e-commerce, AI-powered health interpretation, and blood test intermediation each trigger different regulatory regimes — FBA List 3 restrictions, Thai FDA SaMD classification, and Medical Facility Act requirements — that must be navigated individually.

The recommended structure is a **dual Thai entity model**: a BOI-promoted tech entity (100% foreign-owned) holding the IP, brand, app, and AI engine, and a Thai-majority operating entity handling lab coordination, doctor consultations, and supplements. These two entities are connected via an intercompany licensing agreement.

---

## Every healthtech service activity triggers FBA List 3

Thailand's Foreign Business Act B.E. 2542 (1999) classifies a Thai-registered company as a "foreigner" under Section 4 if foreign nationals hold 50% or more of shares. The Act restricts foreign participation across three lists (Section 8), and virtually every healthtech activity falls under **List 3, Item 21: "Other service businesses"** — the catch-all provision that the DBD interprets extraordinarily broadly.

By activity:

- **SaaS health platforms, AI-powered health interpretation, and health data analytics** fall under List 3(21)
- **A blood testing intermediary** connecting customers to labs could additionally trigger List 3(11) — "Brokerage or agency businesses"
- **Supplement e-commerce** falls under List 3(14)/(15) for retail/wholesale trade, with a carve-out: companies capitalized at THB 100M+ are exempt from FBA restrictions on retail and wholesale activities

For all List 3 activities, a majority-foreign-owned company must obtain either a Foreign Business License (FBL) — a discretionary, 3-6+ month process — or secure an exemption. The two primary exemption pathways for [[bodycypher|BodyCypher]] are:

- **BOI promotion** (Section 12 FBA + Investment Promotion Act B.E. 2520) — the correct pathway for the tech entity
- **Thai-majority ownership** — the correct structure for the operating entity handling labs, doctors, and supplements

VIE structures are not viable in Thailand and would be treated as illegal nominee arrangements. Thai courts apply a substance-over-form doctrine (Supreme Court Decision No. 2975/2547), and the 2024-2025 nominee crackdown has been severe — 820+ legal proceedings between September 2024 and January 2025.

---

## BOI Category 8.1.1 enables 100% foreign ownership for the tech entity

Under BOI Announcement No. Sor 2/2567 (March 15, 2024), Category 8.1 "Digital Technology Business" has two sub-activities:

**Activity 8.1.1 — "Development of Software, Digital Platform, or Digital Content"** receives Group A2 incentives: an 8-year corporate income tax exemption, import duty exemptions, and 100% foreign ownership with a Foreign Business Certificate.

The legal mechanism: Section 12 of the FBA explicitly exempts BOI-promoted entities from FBA List 2 and List 3 restrictions. When the BOI issues a Promotion Certificate, the company applies to the DBD for a Foreign Business Certificate (FBC). The Director-General must issue the FBC within 30 days if documents are complete. This is a non-discretionary entitlement, not a case-by-case approval.

A health-focused software platform developing blood test interpretation, AI action plans, and recommendation algorithms would likely qualify under 8.1.1, provided four conditions are met:

1. Software development occurs in Thailand
2. An in-house Thai IT development team exists
3. The company develops new software functionality (not just implementing third-party tools)
4. Revenue derives from software services (subscriptions, SaaS fees, licensing) rather than pure product retail

Investment requirements are startup-friendly: minimum THB 1.5M/year (~USD 42,000) in salary expenditures for Thai IT personnel — not a fixed capital investment. The company must hire at least 2-3 qualified Thai IT staff. Projects under THB 200M undergo a 40 working day evaluation period. Companies can apply before incorporation, with 6 months to incorporate after approval. Realistic timeline: 4-6 months from application to operational Promotion Certificate.

---

## How likely is BOI approval?

Quite likely for the tech entity, provided it is set up correctly. BOI 8.1.1 is not industry-specific — the BOI does not care that the vertical is health. What they care about is that software is genuinely being developed in Thailand.

The checklist is: Thai IT staff on payroll (2-3 minimum), software being built in Thailand (not just deployed), and revenue structured as software services. None of that is hard to demonstrate for BodyCypher given that the React Native app and backend are actively being developed.

The key practical adjustment: the developer should be on Thai payroll rather than pure contract, which strengthens the application considerably. The one scenario that kills BOI applications for software companies is an obvious shell — a holding company with no actual development activity. As long as BodyCypher has real product development happening in Thailand, the application is straightforward.

---

## Does the 20,000 THB package qualify as BOI software revenue?

Not cleanly as a single bundled price. The 20,000 THB bundle contains two components with fundamentally different natures: the lab test (a physical service being coordinated, not software) and the platform access plus AI analysis plus action plan (software services, BOI-eligible). The BOI entity cannot claim the full 20,000 THB as software revenue without creating audit risk.

The standard solution is an **intercompany licensing model**:

- The customer pays the Thai opco 20,000 THB
- The Thai opco pays the BOI tech entity a software licensing fee for use of the platform, AI engine, brand, and IP
- That licensing fee is the BOI entity's revenue
- The BOI entity does not sell blood tests — it licenses software to the Thai opco that does

The fee split must be defensible at arm's length under Thailand's transfer pricing rules (effective January 2019, aligned with OECD BEPS). Something in the range of 40-60% of the package price flowing as a licensing fee to the BOI entity is plausible at early stage, where the IP and platform are central to the product. This split must be documented in an intercompany licensing agreement from day one.

BOI exemption covers only promoted activities. Supplement retail falls outside BOI scope and must sit in the Thai-majority opco. Careful activity segregation and separate accounting between BOI and non-BOI revenue streams is essential to avoid BOI revocation risk.

---

## What happens after the 8-year tax exemption expires?

The 8-year period is a **tax exemption**, not an ownership permission. When it expires:

- The company starts paying normal Thai corporate income tax (20%)
- That is the only change

The **Foreign Business Certificate (FBC)** granted through BOI is permanent. It does not expire with the tax holiday. There is no requirement to sell shares to Thai holders, no forced dilution, no reversion. The foreign ownership structure remains intact indefinitely.

After expiry, the company can apply for additional BOI promotions on new projects or expanded activities, potentially stacking new tax exemptions on new development investments.

---

## Recommended dual-entity structure

| Entity | Ownership | BOI | What it holds | What it does |
|--------|-----------|-----|---------------|--------------|
| Tech entity (Thai Ltd.) | 100% foreign | Yes — 8.1.1 | IP, brand, app, AI engine | Licenses software to opco, collects licensing fees |
| Operating entity (Thai Ltd.) | Thai majority | No | Lab agreements, doctor relationships, supplements | Sells the 20,000 THB package, pays licensing fee to tech entity |

The intercompany licensing agreement between the two entities is the architectural piece everything else hangs on. It defines what percentage of package revenue flows to the BOI entity as software fees, must be drafted at arm's length, and should be in place from day one.

---

## Medical regulations: a layered compliance challenge

**The Medical Professional Act B.E. 2525 (1982)** restricts who can practice medicine — it regulates individual practitioners, not their corporate employers. A foreign-owned company can legally employ Thai-licensed medical professionals. However, if the platform offers telemedicine consultations, those must be delivered by Thai Medical Council-licensed physicians operating through a licensed medical facility.

**The Medical Facility Act B.E. 2541 (1998)** governs hospitals and clinics. The facility license holder must have Thai domicile, and the facility operator must be a Thai-licensed medical professional. A blood testing intermediary connecting customers to existing licensed labs — without itself collecting samples, running tests, or issuing diagnoses — likely does not require a medical facility license. This is a genuine gray area: if the platform is deemed to be "operating" a medical service rather than facilitating access, licensing requirements could be triggered. Formal legal opinion from [[art-tanapote|Tanapote]] is essential here.

**The Thai FDA's SaMD framework** (published June 2024, revised October 2024) classifies AI health software using the IMDRF risk-based model. AI software that interprets blood test results and provides health recommendations would very likely be classified as a medical device — specifically Clinical Decision Support Software (CDSS) under Class 2 or Class 3. Key requirements include ISO 13485:2016 compliance, disclosure of AI training datasets, cybersecurity documentation, and registration through the SKYNET e-submission portal. Critical constraint: the Thai FDA will not accept any AI medical device that foregoes human decision-making — all AI outputs must include human clinician review. This reinforces the doctor-in-the-loop model from both a product and regulatory standpoint.

**Health data (PDPA):** Under the PDPA B.E. 2562 (2019), health data is sensitive personal data (Section 26) requiring explicit consent. PDPA enforcement has entered an active phase — a hospital was fined THB 1.21M in 2025 for exposing patient records, and total fines exceeded THB 21.5M in August 2025 alone.

---

## Practical barriers beyond formal law

No unified regulatory pathway exists for a healthtech platform. A platform touching blood tests, AI interpretation, supplements, and health data must coordinate with: DBD (FBA compliance), BOI (promotion), Thai FDA (SaMD + supplement registration), Medical Council (if telemedicine), and PDPC (data protection).

Lab partnerships require local relationships and trust. Having [[art-chawapon-kidhirunkul|Dr. C]] and Sanwiz Lab infrastructure, or a formal N Health partnership, directly addresses this implicit barrier. Banking involves enhanced due diligence for foreign-owned companies, though BOI-promoted entities generally have smoother relationships with Thai banks.

---

## 2024-2025 regulatory shifts

**FBA reform approved by Cabinet on April 22, 2025** proposes lifting the 49% foreign equity cap in non-strategic sectors and removing digital platforms from List 3. Driven by Thailand's 2024 OECD membership application. No draft law published yet — implementation expected in stages through 2026.

**The Digital Health Act framework** was endorsed by the MOPH Special Committee in late 2025 to create foundational legislation for health data exchange, AI governance, and telemedicine. No draft legislation exists yet.

**Thai FDA's SaMD/AI guidance** (June-October 2024) creates for the first time a clear classification and registration pathway for AI health software.

---

## Three areas requiring formal legal counsel

1. Whether the blood testing intermediary model constitutes "operating a medical service" under the Medical Facility Act — genuinely ambiguous
2. The precise SaMD classification of the AI interpretation engine, which determines whether Class 2 notification or Class 3 license is required
3. The defensible transfer pricing split between the two entities, which must be formally documented from incorporation

---

*Prepared March 2026 | Verify regulatory details with [[art-tanapote|Tanapote]] ([[ipc-international|IPC International]]) before acting*

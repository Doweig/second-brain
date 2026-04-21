---
type: legal-research
date: 2026-02-01
source: manual
tags:
  - pdpa
  - foreign-business-act
  - launch-strategy
people: []
companies:
  - bodycypher
status: raw
---

# BodyCypher's Thai legal risks vary wildly across its three features

**The Lab Panel Builder is surprisingly safe to launch; the PDF extraction tool is not.** Thailand's enforcement apparatus focuses on tangible harms — selling drugs, distributing medical devices, operating unlicensed clinics — not on health information websites. Multiple platforms already publish Thai lab pricing openly, and no enforcement actions against health comparison sites exist. But the moment [[bodycypher|BodyCypher]] touches actual health data (Feature 3), Thailand's increasingly aggressive PDPA enforcement creates real personal liability, including criminal penalties, even for an unregistered individual. The founder's biggest strategic risk isn't the medical practice question — it's the data protection one.

Operating any commercial website in Thailand as a foreigner without a legal entity violates the Foreign Business Act, requires a work permit the founder can't get, and creates tax exposure. But enforcement against small pre-revenue digital businesses remains rare. The practical path forward involves launching Features 1 and 2 immediately with strong disclaimers while deferring Feature 3 until a legal entity exists.

---

## Feature 1 is the safest bet — and already has Thai precedent

The Lab Panel Builder carries **the lowest legal risk** of all three features. Here's why:

**Price comparison is established practice.** GoWabi, HDmall (formerly HonestDocs), HealthDeliver.asia, WhatClinic, and Bookimed all publish explicit pricing from N Health, PathLab, and other Thai labs without apparent regulatory issues. GoWabi lists N Health's Allergy Profile at ฿2,400 and PathLab's Risk Assessment packages at ฿2,050. No cease-and-desist actions or lawsuits against price republication have been found. The labs actively participate in marketplace platforms to acquire customers.

**Premade panels don't constitute medical practice.** Thailand's Medical Profession Act B.E. 2525 defines medical practice as "examination, diagnosis, treatment and prevention of disease" performed "on human beings." A website stating "people over 40 should consider a lipid panel" is educational content. The critical legal line is **personalization**: general panels organized by age, gender, or wellness goals (longevity, hormones, basic checkup) fall on the safe side. A tool that asks about individual symptoms and recommends specific tests based on those symptoms would cross toward medical practice.

**Practical risk: very low.** Thai FDA enforcement targets drug sellers, counterfeit products, and unlicensed medical facilities. The landmark enforcement case — the **2019 HonestDocs raid** — was specifically about selling dangerous drugs online via website and LINE, not about publishing health information. HonestDocs continues operating today as HDmall after pivoting to a compliant marketplace model.

**Recommended guardrails for Feature 1:**
- Frame panels as educational ("common tests for people interested in metabolic health") rather than prescriptive ("you should get these tests")
- Never ask about symptoms or conditions to personalize recommendations
- Include a clear disclaimer: "This is a health information tool, not medical advice. Consult a physician before ordering tests."
- Attribute pricing to public sources and update regularly
- Avoid language implying a doctor-patient relationship

---

## Feature 2 occupies a genuine legal grey zone, but leans safe

The ChatGPT Prompt Library is legally novel — no Thai precedent exists for this exact model. But its architecture creates meaningful legal distance from medical practice.

**The key protective factor is separation.** The website provides pre-written text templates. Users independently copy these into third-party AI tools. The website never sees, processes, or stores health data. This three-party structure (website → user → ChatGPT) makes it difficult to characterize the website as performing "examination" or "diagnosis" on a human being under Section 4 of the Medical Profession Act. The website is closer to publishing a book about how to understand blood tests than to practicing medicine.

**However, two risks deserve attention.** First, Thailand's 2021 Telemedicine Notification broadly defines telemedicine to include "health advice" delivered via telecommunications by practitioners through licensed facilities. While this targets actual medical consultations rather than template distribution, an aggressive regulator could argue the prompts constitute systematized health advice. Second, if Thailand's **draft AI legislation** (Draft Royal Decree on Business Operations Using AI Systems) passes — expected sometime in 2026 — medical AI tools will likely face "high-risk" classification with testing and human oversight requirements. The prompts themselves wouldn't be AI, but the regulatory environment is shifting.

**Civil liability is the more realistic concern.** If someone follows AI-generated advice derived from a BodyCypher prompt and suffers harm, Thailand's Civil and Commercial Code Section 420 (tort liability) and Consumer Case Procedure Act B.E. 2551 could theoretically apply. The "this is not medical advice" disclaimer helps but isn't bulletproof — Thai consumer protection law evaluates claims based on **consumer perception, not the provider's stated intention**.

**Recommended guardrails for Feature 2:**
- Every prompt page must carry prominent disclaimers in both English and Thai stating this is not medical advice, the website doesn't see user data, and AI outputs should be verified with a licensed physician
- Never frame prompts as producing "diagnoses" or "treatment plans" — use language like "educational exploration" or "conversation starters for discussing results with your doctor"
- Include a terms-of-service acknowledgment before accessing prompts
- Avoid prompts designed to recommend medications or treatments — focus on dietary, lifestyle, and "questions to ask your doctor" categories
- **Practical risk: low-to-moderate.** No enforcement precedent exists, but civil liability exposure is real if harm occurs

---

## Feature 3 is where the real danger lives — PDPA makes this a non-starter without an entity

The Lab Result PDF Extraction tool creates **significant and actively enforced legal exposure** that the other features do not.

**Blood test results are unambiguously sensitive personal data.** Section 26 of Thailand's PDPA B.E. 2562 explicitly lists health data as sensitive personal data. Processing is prohibited without explicit consent. The PDPA's definition of "collection" and "use" is broad — the moment a user uploads a PDF and the tool parses it, both "collection" and "use" have occurred, **even if the data is immediately discarded**. There is no transient-processing exemption in the PDPA.

**PDPA enforcement is real, escalating, and punitive.** Thailand imposed its first major PDPA fine in August 2024 — **THB 7 million** against a retail company for inadequate security and failure to appoint a Data Protection Officer. By August 2025, cumulative fines exceeded **THB 21.5 million** across multiple cases. Healthcare is explicitly identified as a high-scrutiny enforcement sector. Both data controllers and processors face penalties, and processors sometimes receive higher fines than controllers.

**The compliance requirements are substantial.** Processing sensitive health data triggers the full PDPA apparatus:

- **Explicit consent** via affirmative action (checkbox, button click) with clear disclosure of processing purposes
- **Privacy policy** disclosing all Section 23 requirements (purpose, retention, data subject rights, controller contact information)
- **Data Protection Officer appointment** — mandatory when core activities involve sensitive personal data
- **Record of Processing Activities** — no SME exemption applies when processing sensitive data
- **72-hour breach notification** to the PDPC
- **Security measures** — administrative, technical, and physical safeguards
- **Thai representative appointment** — required for foreign controllers processing sensitive data

**Criminal penalties apply to individuals.** Processing sensitive health data without consent can result in **up to 6 months imprisonment and THB 500,000 fine** — doubled to **1 year and THB 1 million** if done for commercial benefit. Administrative fines reach **THB 5 million per offense**. Punitive damages in civil suits can reach **2x actual damages**. These penalties attach to the individual data controller — which, under PDPA's definition, includes any "natural person" who makes decisions about data processing.

**Flagging high/low values adds medical practice risk.** While displaying standard reference ranges alongside values is arguably a factual comparison, Thai law's definition of "examination" and "diagnosis" is broad enough that interpreting individual lab results — even mechanically — could be characterized as a diagnostic act, especially under the Medical Device Act B.E. 2551, which classifies software performing diagnostic functions as a medical device.

**Bottom line on Feature 3:** Do not launch this feature without a registered legal entity, PDPA compliance infrastructure, and ideally legal counsel review. The personal criminal exposure to the founder is too high given active enforcement.

---

## The Foreign Business Act is the background risk for everything

Operating any commercial website in Thailand as a foreigner without a legal entity violates multiple laws simultaneously. The **Foreign Business Act B.E. 2542** classifies most service businesses under its List 3 catch-all (Item 21), requiring a Foreign Business License. Penalties for FBA violations include **up to 3 years imprisonment and THB 1 million fine**.

The **Alien Working Act** defines "work" as "using energy, knowledge, or effort to produce something" — broad enough to cover writing code on a laptop. Any work performed in Thailand by a foreigner requires a work permit, which requires a sponsoring Thai company. There are no statutory exemptions for pre-revenue startups, MVPs, or prototype testing.

**A US LLC does not solve this.** A foreign juristic person is still a "foreigner" under the FBA. The only US-specific advantage is the **US-Thailand Treaty of Amity (1966)**, which allows Americans to own 100% of a Thai-registered company — but this requires actually registering a Thai entity and obtaining Treaty certification through the US Embassy. Simply operating a US LLC that targets Thailand provides no protection.

**Realistic enforcement assessment: low for now, rising fast.** Thailand's Department of Business Development launched investigations into hundreds of companies in 2024-2025, with **820 nominee-related cases** and plans to inspect **46,918 business entities**. E-commerce is explicitly on the inspection list. The Revenue Department's AI-powered RD10X unit now matches platform data to identify undeclared online income. A pre-revenue English-language information website is still very low on the enforcement priority list, but the environment is tightening.

---

## The practical launch playbook: what to do right now

**Phase 1 — Launch immediately (no entity needed):**

Launch Features 1 and 2 as a static or semi-static information website. Keep it educational, not transactional. Accept no payments, process no personal data, collect no health information. Use robust disclaimers. This is the lowest-risk way to test market demand. The realistic enforcement probability for an English-language health information website with no revenue, no data collection, and no drug sales is **near zero** based on all available precedent.

Minimum disclaimers should include: (1) "This website provides general health information only and does not constitute medical advice"; (2) "No doctor-patient relationship is created"; (3) "Consult a licensed physician before making health decisions"; (4) "AI-generated content from third-party tools is not verified and may be inaccurate"; (5) "This service is not affiliated with any laboratory listed." Display these prominently, not buried in terms of service.

**Phase 2 — Register a legal entity (before collecting any data or revenue):**

Before launching Feature 3 or accepting any payment, establish a Thai limited company. The most practical options are a **Thai-majority company** (51% Thai / 49% foreign with preference shares giving the founder effective control — legal if Thai shareholders are genuine investors, not nominees) at approximately THB 20,000–50,000 for registration, or a **BOI-promoted company** under Category 8.1 (Software/Digital Platforms) allowing 100% foreign ownership with up to 8 years of tax exemption. The BOI path requires THB 1.5 million/year minimum in Thai IT personnel salaries but provides comprehensive legal protection including facilitated work permits.

**Phase 3 — PDPA compliance before Feature 3 goes live:**

With a legal entity in place, implement the full PDPA compliance stack: explicit consent mechanism, privacy policy, DPO appointment, ROPA, security measures, and breach notification protocol. Consider designing the PDF extraction tool to process entirely client-side (in the browser via JavaScript/WebAssembly) so that health data never reaches BodyCypher's servers. This architectural choice would dramatically reduce PDPA exposure, though legal counsel should confirm it eliminates "collection" under Thai law.

**What could actually get the founder in trouble** — ranked by realistic probability:

1. **PDPA violation from processing health data without compliance** (Feature 3) — highest real risk given active enforcement and criminal penalties against individuals
2. **Working without a work permit** — moderate risk if the founder is visible in Thailand's startup scene, attending events, or on social media
3. **Crossing into personalized medical advice** — low risk if guardrails are maintained, but serious consequences (up to 3 years imprisonment) if a complaint is filed
4. **FBA violation for operating without registration** — low risk for a pre-revenue information website, but rising given 2024-2025 enforcement trends
5. **Tax non-compliance** — low risk while pre-revenue, but Thai tax residency obligations apply from day one of earning income

The founder's instinct to test before incorporating is reasonable for Features 1 and 2. Feature 3 is the exception — the PDPA's combination of active enforcement, criminal penalties, and explicit health-data provisions makes it the one feature that genuinely requires legal infrastructure before launch.
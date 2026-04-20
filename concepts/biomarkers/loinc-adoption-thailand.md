---
type: product-research
date: 2026-02-01
source: manual
tags: [biomarkers, thailand, loinc, lab-integration]
people: []
companies: [bodycypher, bdms-wellness, bnh-hospital]
status: raw
---

# LOINC adoption is real but messy — and a Thai startup can skip most of it

**The short answer: major US reference labs do use LOINC codes, but the system is far more complex and inconsistently adopted than it appears on paper.** For a health tech startup in Thailand building a blood testing platform with ~200-500 biomarkers, full LOINC mapping is overkill. A curated spreadsheet of canonical biomarker names with aliases, fuzzy matching, and a single LOINC reference code per test is the pragmatic path — buildable in days, not months. Thailand has its own national lab terminology (TMLT) with LOINC mapping built in, but most Thai labs still deliver results as PDFs with no structured API access.

The LOINC database contains **~100,000 codes**, but usage follows a steep power law: **80 codes account for 80% of test volume**, and the official LOINC Top 2000+ subset covers **98-99% of all results**. For blood biomarker price comparison and test catalog matching, you need perhaps 300-500 codes — a tiny, manageable slice. The real question isn't whether to use LOINC at all, but how lightly you can touch it while future-proofing your data model.

---

## US labs use LOINC — unevenly and often imperfectly

LOINC adoption in the US is driven by regulation, but the mandates are subtler than they appear. The ONC requires certified EHR technology to *receive and process* LOINC codes — it does not require laboratories themselves to transmit them. Meaningful Use Stage 2 pushed LOINC for electronic laboratory reporting to public health authorities, and the USCDI framework requires LOINC for interoperability. But there's no single federal rule saying "every lab must use LOINC."

In practice, adoption splits sharply by lab size. **Quest Diagnostics and Labcorp** — which together process a massive share of US outpatient lab volume — both systematically map to LOINC and publish their mappings online. Quest provides LOINC codes through its Test Center, transmits them in HL7 messages and its newer FHIR-based Quantum Hub API, and supplies integration partners with test catalog files containing LOINC codes alongside internal codes. Labcorp publishes a downloadable LOINC Map spreadsheet and transmits LOINC codes in HL7 interfaces. Mayo Clinic Laboratories and ARUP Laboratories similarly assign LOINC codes to their assays and publish downloadable spreadsheets.

The story at smaller labs is far less tidy. Small community hospital labs and physician office labs are "very inconsistent" in LOINC adoption. Some legacy LIS platforms don't even have a database field for LOINC codes. The VA health system — the largest integrated US health system with 130 facilities — achieved **85% of tests and 99% of results** mapped to LOINC by 2018, but correctness "varied considerably by test and across time," with an estimated **16% noisy label rate** (incorrect LOINC assignments). A study of three major institutions found that of 884 manually reviewed mappings, 36 contained at least one error in LOINC axis assignment. Even sophisticated organizations get mapping wrong.

---

## How labs actually manage codes internally

Every lab operates with proprietary internal codes deeply embedded in instrument interfaces, billing, quality control, and decades of historical data. LOINC functions as a **translation layer for external communication**, not as the primary internal identifier. The LOINC organization itself recommends "simultaneous communication of the sender's local code and local name in addition to the LOINC code" — an acknowledgment that local codes aren't going away.

The mapping process remains predominantly manual and expert-dependent. **RELMA** (Regenstrief LOINC Mapping Assistant), a free Windows tool, assists with mapping but still requires someone who understands both clinical laboratory science and LOINC's six-axis structure (Component, Property, Time, System, Scale, Method). This granularity is why a single analyte like glucose generates **68 different LOINC codes** depending on specimen type, measurement method, scale, and units. Machine learning approaches show promise — a VA study achieved 85-96% accuracy — but remain research-grade rather than production-ready for most organizations.

The major LIS platforms all support LOINC to varying degrees. **Epic Beaker**, increasingly dominant as hospitals consolidate on enterprise platforms, supports LOINC code assignment to result components. **Sunquest** (now Clinisys) supports LOINC fields, though its VP once noted that "30,000 codes make mapping a daunting task." **Orchard Harvest**, serving 1,600+ smaller US labs, uses LOINC and SNOMED CT in HL7 messages. The trend is clear: modern LIS platforms support LOINC, but the quality and completeness of mapping depends entirely on the humans doing the work.

---

## DTC blood testing companies hide the complexity

Function Health, InsideTracker, and Mito Health all take the same basic approach: partner with a major reference lab, receive structured results, and map them to a proprietary consumer-facing taxonomy. None publicly document using LOINC in their consumer products. The standards complexity is entirely hidden behind clean dashboards.

**Function Health** partners exclusively with Quest Diagnostics across 2,000+ US locations, offering 160+ lab tests per member tested twice annually. Because it uses a single lab partner, Function's mapping challenge is simplified — it receives Quest's structured results (which include LOINC codes) and maps them to its own biomarker representation. **InsideTracker** faces a harder problem because it allows users to upload blood results from *any* lab, meaning it must recognize test names in formats like "Hemoglobin A1c" vs. "HbA1c" vs. "Glycated Hemoglobin" — essentially a fuzzy text matching challenge. **Mito Health**, founded in Singapore in 2023 and backed by Y Combinator, partners with Labcorp in the US and similarly allows past lab result uploads.

The data exchange between labs and platforms happens through two channels. **HL7v2 ORU messages** remain the workhorse — roughly **95% of US healthcare organizations** still use HL7v2 for lab results, typically delivered via SFTP file drops. Quest's newer **Quantum Hub API** uses FHIR, returning results as Observation and DiagnosticReport resources with LOINC codes in JSON format. Middleware platforms like **Health Gorilla** (FHIR-based Diagnostic Network API connecting Quest, Labcorp, BioReference) and **Junction** (formerly Vital, handling 500K+ tests annually for 140+ healthcare organizations) abstract the integration complexity into a single standardized API. For a startup, these middleware platforms represent a potential shortcut — though they're US-focused and unlikely to cover Thai labs.

Apple Health Records and CommonHealth (Android) both explicitly require **FHIR R4 with LOINC codes** for lab results. This creates a strong pull toward LOINC adoption among organizations wanting to surface results on consumer platforms.

---

## Thailand has its own lab coding system with LOINC baked in

Thailand's lab coding landscape is more developed than many assume. The **Thai Health Information Standards Development Center (THIS)** maintains **TMLT (Thai Medical Laboratory Terminology)**, a national lab coding standard with an official LOINC-TMLT mapping built in. Mapping studies show **>80% of Thai local laboratory codes** successfully map to LOINC, with coverage exceeding **95% for clinical chemistry tests** at major university hospitals (Ramathibodi, Siriraj, Chulalongkorn). Thailand also became a **SNOMED International member in February 2022**.

However, the practical reality on the ground is more fragmented. A 2024 survey of 81 public referral hospitals found that **77% still use dual electronic and paper systems** for lab ordering, with only 16% fully electronic. The dominant HIS in public hospitals is **HOSxP** (67% market share), a Thai-developed system used by 300+ hospitals. In the private sector, [[bdms-wellness|BDMS]] hospitals (including Bumrungrad, [[bnh-hospital|BNH]], Samitivej) use **InterSystems TrakCare**. All eight commercial HIS vendors serving Thai public hospitals are Thai companies.

**N Health**, the lab services arm of BDMS (Thailand's largest private healthcare group with 50+ hospitals), operates 80+ branches and holds both CAP and ISO 15189 accreditation. It provides online lab results through a web portal, but there is **no publicly documented API** for external integration. Results delivery across Thai labs is predominantly through hospital patient portals and **printed/downloadable PDFs** — structured electronic data exchange between institutions is still developing.

Thailand's **Health Link** HIE platform, launched in 2021, serves 50+ hospitals and implements HL7 FHIR with pseudonymization. But this is for inter-hospital exchange, not for third-party platform integration. The most common LIMS in Thai public hospital microbiology labs is **MLAB** (75% market share), followed by LAB PLUS and ALLABIS-M — all Thai-developed systems. TMLT codes are increasingly required for reimbursement from Thailand's three public insurance schemes, which effectively drives adoption through financial incentives rather than direct mandates.

---

## The minimum viable approach is a curated spreadsheet, not a terminology engine

For a startup matching ~200-500 blood biomarkers across a handful of Thai lab partners and competitors, the evidence strongly supports a **curated mapping table** over any automated terminology system. Here's why this works, and how to build it:

The approach mirrors what successful companies already do. TELUS Health's Collaborative Health Record uses a "lab synonym mapping" validated by clinicians — essentially a lookup table mapping name variations to canonical entries. The TRUU-Lab initiative at Texas Children's Hospital found that even within the US, lab test names vary wildly, and ~30% of 13 billion annual tests are unnecessary or incorrect partly due to naming confusion. Your problem is **product matching** (Lab A's CBC = Lab B's Complete Blood Count), not clinical interoperability.

**Recommended schema for a master mapping table:**

| Column | Purpose |
|--------|---------|
| `internal_id` | Your unique identifier (e.g., BM001) |
| `canonical_name_en` | Standardized English name |
| `canonical_name_th` | Thai name |
| `aliases` | All known variations, pipe-delimited |
| `category` | Simple grouping (Chemistry, Hematology, Lipids, Hormones) |
| `specimen_type` | Simplified: Blood, Serum, Urine |
| `loinc_code` | Single most relevant LOINC code (for future-proofing) |
| `units_si` | Expected units in Thailand (SI/molar preferred) |
| `lab_x_code` / `lab_x_name` | Per-partner-lab code and name columns |

**Build sequence:** Start with the **awesome-biomarkers** GitHub project (`markwk/awesome-biomarkers`), which provides a curated JSON database of common biomarkers with panels, reference ranges, and aliases. Cross-reference against the **LOINC Top 2000+ SI version** (free download from loinc.org/usage — use the SI version since Thailand uses molar units). Scrape test catalogs from your Thai lab partners. Manually curate 300 tests in **2-3 person-days**. For automated matching of new tests, use Python's `rapidfuzz` library (token_sort_ratio ≥ 85) with LLM-assisted matching for ambiguous cases — feed an LLM the unknown test name plus your canonical list and ask it to identify the best match with a confidence score.

**Include LOINC as a reference field, not a primary system.** The single most relevant LOINC code per biomarker takes minutes to look up from the Top 2000+ list and provides three benefits: future-proofing if you ever need clinical interoperability, a universal join key if you integrate with US platforms or Apple Health, and a source of standardized English names and units. But don't agonize over which of the 68 glucose LOINC codes is "correct" — pick the most common one (likely `2345-7` for serum/plasma glucose, mass concentration) and move on.

---

## Conclusion: pragmatism beats perfectionism

The gap between LOINC's theoretical promise and practical reality is wide. Major US reference labs use it; smaller labs often don't. Even large systems get **16% of mappings wrong**. DTC health companies universally build proprietary consumer taxonomies on top of whatever structured data they receive from labs. Thailand has a surprisingly mature standards framework (TMLT with LOINC mapping, SNOMED CT membership, HL7 FHIR pilots) but a practical reality of PDF lab reports and fragmented HIS systems.

For a Thai blood testing startup, the strategic insight is this: **your initial bottleneck is not terminology standards — it's getting structured data out of Thai labs at all.** N Health and other Thai labs deliver results primarily as PDFs through web portals. Your first integration challenge is likely OCR or manual data entry, not LOINC mapping. Build your curated biomarker table now (300-500 entries, 2-3 days of work), include a LOINC reference code per test for future-proofing, and invest your engineering time in solving the actual data extraction problem. When structured data exchange matures in Thailand — through Health Link, FHIR APIs, or direct lab partnerships — you'll have the canonical mapping layer ready to plug in.
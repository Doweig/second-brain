---
type: product-research
date: 2026-02-01
source: manual
tags: [biomarkers, reference-ranges, product, regulatory]
people: []
companies: [bodycypher, bdms-wellness]
status: raw
---

# Biomarker reference range datasets for BodyCypher's Thailand launch

**No single downloadable, machine-readable database of comprehensive biomarker reference intervals exists anywhere in the world — but the raw materials to build one are available across roughly a dozen key sources.** Thailand imposes no legally mandated reference intervals and classifies wellness-monitoring software outside medical device regulation, giving [[bodycypher|BodyCypher]] significant flexibility. However, using Thai- and Asian-specific data where available is both clinically important (documented differences for **>50% of common biomarkers** across ethnicities) and commercially defensible. This report maps every actionable dataset across four layers — Thailand-specific, global gold-standard, Asian population, and optimal/functional ranges — with access methods, formats, and licensing for each.

Your existing market intelligence document confirms the opportunity: Bangkok's expat and longevity communities are already "hacking" their own lab interpretation via LLMs, validating demand for an AI-driven wellness platform that goes beyond hospital "data cliffs." The reference range infrastructure you build will be the scientific backbone of that product.

---

## Layer 1: Thailand has no mandated ranges, but usable local studies exist

**Thailand does not require specific reference intervals from any regulatory body.** The Bureau of Laboratory Quality Standards (BLQS-DMSc) under the Department of Medical Sciences administers ISO 15189 accreditation for medical laboratories but delegates reference interval establishment to individual labs. The Thai FDA, Thai Medical Council, and Department of Medical Sciences publish no centralized national reference range tables. Each accredited lab (201 as of 2019) chooses its own approach — typically adopting manufacturer ranges and verifying against their patient population.

This means BodyCypher faces **no legal barrier** to using international reference ranges. More importantly, Thai FDA guidance explicitly classifies general wellness monitoring software — including fitness apps, BMI calculators, and health progress trackers — as **not a medical device** under the Medical Device Act B.E. 2551. The critical regulatory boundary is between "wellness monitoring" and "diagnostic indication." As long as the platform avoids language like "diagnosis," "disease detection," or "medical advice," it falls outside medical device regulation. The Thai FDA's October 2024 Software as a Medical Device guidance, aligned with the ASEAN Medical Device Directive, reinforces this classification.

**The PDPA (Personal Data Protection Act) is the more pressing compliance concern.** Health data is classified as "sensitive personal data" under Section 26, requiring explicit granular consent, robust security measures, data subject rights (access, deletion, portability), and a Data Protection Officer if processing health data at scale. PDPC enforcement is active — a **THB 21.5 million fine** was issued in August 2025.

### Published Thai population reference interval studies

Despite the absence of a national database, several Thai academic studies provide directly usable data:

| Study | Year | Analytes | Sample size | Access |
|-------|------|----------|-------------|--------|
| **Thammasat University biochemistry** (Kongkhum & Sarnkhaow) | 2025 | 14 analytes: FBG, TC, HDL-C, TG, total protein, albumin, BUN, creatinine, uric acid, AST, ALT, ALP, amylase, lipase | 197,897 test results | Open access, CC BY-NC-ND 4.0 via TCI-ThaiJO |
| **Siriraj Hospital CBC** (Wongkrajang et al., Mahidol University) | 2018 | All CBC parameters: Hb, Hct, RBC, WBC, platelets, differentials, MCV, MCH, MCHC, RDW | Healthy adults 18–60 | PubMed (Int J Lab Hematol) |
| **Thai NHES IV thyroid function** | ~2014 | TSH (0.34–5.11 mIU/L), FT4 (0.98–1.79 ng/dL) | 2,545 healthy non-pregnant subjects | ResearchGate |
| **Chulalongkorn HbA1c** | 2005 | HbA1c DCCT/NGSP: 4.79–6.15%; HbA1c IFCC: 2.88–4.44% | Thai adults | PubMed |
| **King Chulalongkorn chemistry** (Chamnanpai et al.) | 2004 | 10 analytes: FBG, BUN, creatinine, uric acid, cholesterol, TG, HDL-C, AST, ALT, ALP | 164 subjects | Academia.edu |
| **Khon Kaen biochemistry** (Chatchawal et al.) | 2023 | Biochemistry parameters | Check-up records | Asia Pac J Sci Technol |
| **Nong Khai chemistry** (Yotsakullert et al.) | 2020 | Clinical chemistry | Regional | Arch AHS |

The **2025 Thammasat study is the most valuable** — it used 197,897 results via indirect methods and found that Thai reference intervals for total cholesterol, triglycerides, and uric acid are **higher than previous reports**, reflecting metabolic shifts toward Western diet and obesity patterns. The 2018 Siriraj CBC study is the gold standard for Thai hematology parameters.

**Key gap:** No Thai studies cover hormones (testosterone, estradiol, DHEA-S, cortisol), vitamins (B12, folate, vitamin D), minerals (magnesium, zinc), tumor markers, or advanced metabolic markers (insulin, HOMA-IR, ApoB, Lp(a)). For these ~200+ analytes, you must rely on international or Asian regional data.

Major Thai private lab networks — **N Health** ([[bdms-wellness|BDMS]] subsidiary, 80+ branches), **Bumrungrad**, **Samitivej** — do not publish their reference ranges publicly. Partnership or NDA-based access would be required to obtain their internal validated ranges.

---

## Layer 2: Global datasets range from freely downloadable raw data to locked-down proprietary directories

### The essential sources, ranked by utility for BodyCypher

**NHANES (National Health and Nutrition Examination Survey)** is the single most comprehensive freely available source. The CDC publishes individual-level laboratory data covering **200–500+ biomarkers** depending on survey cycle, spanning clinical chemistry, endocrine markers, nutritional biomarkers (vitamins A, B12, folate, D, iron), hematology, and environmental exposures. Data files are in SAS Transport format (.XPT), convertible to CSV. R packages `nhanesA` and `RNHANES` enable direct download. A curated harmonized dataset published in Nature Scientific Data merges data covering **134,310 participants and 4,740 variables** (1988–2018) into ready-to-use CSV files. NHANES is **completely free** and publicly available — it requires only a Data User Agreement. The limitation: it represents the US population and requires significant statistical expertise (survey weighting) to derive proper reference intervals. Access at https://wwwn.cdc.gov/nchs/nhanes/.

**Mayo Clinic Laboratories Test Catalog** covers **4,400+ tests** with reference intervals, interpretive information, and clinical algorithms. Uniquely, the **full catalog is downloadable as PDF** at their print catalog page. Free web access. This is the most complete single-source reference lab catalog available and an excellent cross-referencing tool. Access at https://www.mayocliniclabs.com/test-catalog.

**ARUP Laboratories Test Directory** (University of Utah, nonprofit academic lab) offers a comprehensive, freely accessible web directory with reference intervals, methodology details, and clinical context. The companion ARUP Consult site provides free clinical decision support. Not bulk-downloadable, but the most useful free online resource for individual test lookups. Access at https://ltd.aruplab.com/.

**Tietz Textbook of Laboratory Medicine, 7th Edition (2023)** remains the gold-standard compendium. Edited by Nader Rifai, it covers ~700+ entries with method-, age-, and sex-specific reference intervals in both conventional and SI units. The reference intervals appendix sources pediatric values from CALIPER. Available as hardcover and eBook via Elsevier ExpertConsult for **$150–250**. Not available as structured data — extraction is manual. Essential as a validation reference.

**IFCC C-RIDL / TF-GRID (Task Force on Global Reference Interval Database)** provides globally harmonized intervals for **~50 commonly tested analytes** based on 13,386 healthy adults across 12+ countries. The GRID interactive visualization is at https://grid.ifcc.org/. Data is distributed across multiple journal publications (Clinical Chemistry and Laboratory Medicine, Clinica Chimica Acta), not available as a single download. The methodology is the global gold standard — these intervals carry the highest authority for the core chemistry analytes they cover.

**CALIPER** covers **200+ biomarkers** across 5 analytical platforms, with a free searchable online database and mobile app. Primarily pediatric (birth to 18 years), with adult extension via the Canadian Health Measures Survey. Free for all users. Access at https://caliperproject.ca/. Most relevant if BodyCypher ever extends to pediatric populations.

**NORIP (Nordic Reference Interval Project)** covers only **25 chemistry + 8 hematology analytes** from 3,002 reference individuals across 5 Nordic countries. Published in Scandinavian Journal of Clinical and Laboratory Investigation (2004). Useful for validation of core markers but too narrow for a 100–300 biomarker platform. Data available in published tables, not as structured downloads.

**Quest Diagnostics and LabCorp** each maintain searchable web directories covering **3,500+ tests** with reference ranges, but neither offers bulk download. Ranges are proprietary, method-specific, and designed for per-test lookup. Terms of service prohibit systematic scraping. Useful for spot-checking only.

**CLSI EP28-A3c** is not a dataset but the internationally recognized **methodological guideline** for defining, establishing, and verifying reference intervals. Any platform deriving its own ranges should follow this standard. Available from CLSI for ~$100–200.

### Summary comparison

| Resource | Biomarkers | Format | Free | Raw data | Best use |
|----------|-----------|--------|------|----------|----------|
| NHANES (harmonized) | 200–500+ | SAS XPT → CSV | Yes | Yes (individual-level) | Deriving population intervals |
| Mayo Clinic Labs | 4,400+ tests | Web + downloadable PDF | Yes | No | Most complete downloadable catalog |
| ARUP Laboratories | Thousands | Web directory | Yes | No | Free comprehensive reference |
| Tietz Textbook 7th ed | 700+ entries | Book/eBook | No ($150–250) | No | Gold-standard validation |
| IFCC C-RIDL/GRID | ~50 analytes | Journal articles, web map | Partial | No | Globally harmonized core intervals |
| CALIPER | 200+ | Web DB, mobile app | Yes | No | Pediatric intervals |
| NORIP | 33 analytes | Journal PDFs | Partial | No | Nordic validation reference |
| Quest/LabCorp | 3,500+ tests | Web directory | Web only | No | Per-test spot checks |

**Critical finding: No comprehensive, structured, open-source reference interval dataset exists on GitHub, Kaggle, or elsewhere.** Building one from NHANES raw data combined with published sources would itself represent significant intellectual property.

---

## Layer 3: Asian populations show clinically significant differences in over half of common biomarkers

A landmark NHANES-based study (Lim et al., 2015) found significant racial/ethnic differences in **almost all 38 laboratory tests examined**. A separate EHR study confirmed that **>50% of common tests** show significant differences across racial groups, yet only creatinine is currently ethnicity-adjusted in mainstream clinical practice. For a Thai wellness platform, ignoring these differences risks systematically misclassifying healthy users as abnormal (or vice versa).

### The most actionable Asian-specific dataset

The **2009 APFCB/IFCC Asian Multicenter Study** is the single most important resource for BodyCypher. Led by Kiyoshi Ichihara (Yamaguchi University), it enrolled **3,541 healthy individuals aged 20–65 from 63 laboratories across Japan, South Korea, China, Vietnam, Malaysia, and Indonesia**, covering **72 analytes** (31 standardized + 40 non-standardized + isozymes). The data is freely accessible through an **interactive viewer at https://ccb-project.org/** (RefVal Viewer) with Source of Variation, Age Profile, and Correlation analysis tools. This is the closest proxy to Thai reference intervals for analytes not covered by Thai studies — Vietnamese and Malaysian data in the set are geographically and genetically closest to the Thai population.

### Other key Asian datasets

**KNHANES (Korea National Health and Nutrition Examination Survey)** has run since 1998, surveying ~10,000 individuals annually with comprehensive biochemical profiles, CBC, lipids, thyroid hormones, vitamins, and bone density. Public data access at https://knhanes.kdca.go.kr (application required). Most notable finding: Korean **TSH upper reference limit is 6.8–7.03 mIU/L** versus the Western ~4.0 mIU/L, attributed to high dietary iodine. Thai TSH (0.34–5.11) is closer to Western ranges.

**China's IFCC/C-RIDL Nationwide Study** (Xia et al., 2016) enrolled 3,148 healthy volunteers from 6 cities for 28 biochemistry analytes. A separate 2024 nationwide lipid study (11,333 adults) established the first Chinese age- and sex-specific lipid reference intervals, confirming significant differences from Western-derived intervals. Both available via PubMed.

**Japan's JSCC Common Reference Intervals Project** (2016) merged three multicenter studies totaling 6,345 individuals for 40 analytes, establishing the most rigorously validated national reference interval set in Asia. Published in Annals of Clinical Biochemistry.

### Biomarkers with documented Asian-Western differences

The following biomarkers require Asian-adjusted ranges, listed by clinical significance for a wellness platform:

**Creatinine and eGFR** show the largest practical impact. Asian populations have systematically **lower serum creatinine** due to lower average muscle mass. The Japanese eGFR correction coefficient is **0.808** (standard equations overestimate GFR). The 2021 CKD-EPI equation removed race but may still misclassify ~30% of Asian patients. Cystatin C-based eGFR performs better in Asian populations.

**White blood cell count** is **significantly lower** in Asians (p = 7.5 × 10⁻¹¹ versus Europeans) through a mechanism distinct from the benign ethnic neutropenia seen in African Americans. Using Western WBC lower limits would over-flag leukopenia in Thai users.

**Hemoglobin, hematocrit, MCH, and MCHC** are all **lower** in Asian populations. The Siriraj Hospital Thai CBC study provides the correct baseline here. Note that thalassemia trait prevalence in Thailand (~30–40% carrier rate for α- or β-thalassemia) further shifts these parameters.

**TSH** varies dramatically by country. Korean TSH upper limits (~7 mIU/L) differ from Thai (~5.1 mIU/L) and Western (~4.2 mIU/L) due to iodine intake differences. **BodyCypher should use the Thai NHES IV reference (0.34–5.11 mIU/L), not Western or Korean ranges.**

**Liver enzymes (ALT, AST, GGT)** are influenced by the **ALDH2 variant** (rs671), carried by ~30–50% of East and Southeast Asians but virtually absent elsewhere. This polymorphism is significantly associated with AST (P = 5.20 × 10⁻¹³) and ALT (P = 4.98 × 10⁻⁸). A wellness platform should ideally flag ALDH2 carrier status as relevant context.

**HbA1c** shows ethnic variation — a PIEZO1 locus variant common in South Asians lowers HbA1c independently of glucose. The Thai-specific reference of **4.79–6.15%** should be used rather than Western thresholds.

**Lipids** require sex- and age-specific Asian partitioning. The 2024 Chinese nationwide lipid study and the APFCB Asian data both show systematic differences from Western intervals, particularly for triglycerides and HDL-C.

**Immunoglobulins (IgG, IgA) and complement (C3, C4)** are **higher** in populations near the equator, attributed to microbial antigen exposure — directly relevant for Thailand.

**PSA** is generally **lower** in Asian men, with prostate cancer incidence ~1/30th of North American rates in Japanese populations.

---

## Layer 4: No downloadable "optimal range" database exists, but the raw materials are compilable

The distinction between standard reference intervals (central 95% of a sampled population, which may include subclinically unhealthy individuals) and optimal ranges (narrower bands associated with lowest disease risk) is fundamental to a wellness optimization platform. **No company or organization publishes a freely downloadable, machine-readable database of optimal ranges.** Every source is either proprietary SaaS, embedded in textbooks, or scattered across web pages. BodyCypher will need to compile its own.

### Key commercial platforms and their approaches

**InsideTracker** (48 blood biomarkers) uses a two-pronged methodology: literature extraction from peer-reviewed studies plus a population database of **180,000+ healthy Americans** with demographic segmentation. Optimal zones are personalized by age, gender, ethnicity, and activity level via their proprietary SegterraX AI engine trained on 2,500+ studies. They published one peer-reviewed paper in *Scientific Reports* (2018, co-authored by David Sinclair), but a correction noted all authors were employed by or advised InsideTracker. **Ranges are proprietary and dynamically generated — not downloadable.** US-centric population data limits Thai applicability.

**Function Health** (100–160+ tests) displays "optimal ranges" with color coding and clinician notes, backed by a scientific advisory board including JoAnn Manson (Harvard) and Andrew Huberman (Stanford). **No published methodology paper exists.** Ranges are visible only within the app portal. US-only via Quest Diagnostics labs. The biomarker list is useful as a reference for panel composition.

**Optimal DX** (100+ biomarkers) is the most transferable model. Built on Dr. Dicken Weatherby's textbook *Blood Chemistry and CBC Analysis — Clinical Laboratory Testing from a Functional Perspective*, it provides evidence-based functional ranges with scoring, weighting, and inference rules. Downloadable tracking forms (US and SI units) provide partial data. The textbook itself contains the most complete published compilation of functional medicine ranges. **SaaS subscription required for full access; textbook purchasable on Amazon.**

**Rupa Health** publishes optimal ranges with **linked research citations** at https://www.rupahealth.com/optimal-ranges — one of the more transparent sources. Free to browse.

### Freely accessible functional range compilations

Several web resources publish functional/optimal ranges that can be cross-referenced:

- **Rupa Health Optimal Ranges** (https://www.rupahealth.com/optimal-ranges) — literature-cited, free
- **The Path to Health Functional Lab Ranges** (https://myhealthmanual.com/selfhelp/functional_ranges/) — 50+ biomarkers, free downloadable table
- **Mind Body Functional Medicine lab values chart** — complete functional ranges for thyroid, CBC, CMP, lipids, inflammation markers, free
- **Functional Medicine University sample form** — includes functional ranges for key markers, free PDF
- **Optimal Health longevity biomarker guide** (https://optimalhealth.co/resources/blood-testing/biomarkers-longevity) — evidence-based optimal ranges, free

### Consensus optimal ranges for key wellness biomarkers

Based on cross-referencing multiple functional medicine sources and peer-reviewed literature:

| Biomarker | Standard "normal" | Optimal/functional range | Evidence basis |
|-----------|------------------|--------------------------|----------------|
| Vitamin D (25-OH) | 30–100 ng/mL | **50–80 ng/mL** | Endocrine Society; COVID outcomes research |
| TSH | 0.45–4.5 mIU/L | **0.5–2.0 mIU/L** | 95% of healthy individuals have TSH <2.5 |
| Fasting insulin | 2–25 μIU/mL | **2–5 μIU/mL** | Framingham data; earliest metabolic dysfunction marker |
| HbA1c | <5.7% (normal) | **4.8–5.2%** | Centenarian studies; each 1% above optimal = 20–30% CV mortality increase |
| hs-CRP | <3.0 mg/L | **<1.0 mg/L** (ideal <0.5) | Emerging Risk Factors Collaboration (160K+ individuals) |
| Homocysteine | 0–15 μmol/L | **<7 μmol/L** | >10 associated with atherosclerosis; >11 with cognitive decline |
| Ferritin | M: 20–380; F: 10–150 ng/mL | **M: 30–200; F: 30–100 ng/mL** | Iron deficiency vs. inflammation/hemochromatosis risk |
| ApoB | <130 mg/dL | **<90 mg/dL** (ideal 60–80) | European Atherosclerosis Society consensus |
| Triglycerides | <150 mg/dL | **<100 mg/dL** (ideal 50–80) | TG/HDL ratio <2 ideal |
| Omega-3 Index | N/A (not routine) | **>8%** | <4% highest risk; 8–12% protective |
| Vitamin B12 | 211–911 pg/mL | **>600 pg/mL** | Low-normal causes neurological symptoms |

### Regulatory framing for optimal ranges

Under both US FDA and Thai FDA frameworks, presenting "optimal" ranges is permissible for a wellness product as long as it avoids diagnostic claims. The US FDA's January 2026 General Wellness Product guidance confirms it will not regulate low-risk products intended solely for "general wellness use." Thailand's equivalent guidance similarly exempts general wellness monitoring software. **Required safeguards:** frame as educational/informational, include "not medical advice" disclaimers, avoid auto-generating treatment plans without physician oversight, and never claim to diagnose, treat, or prevent specific diseases.

---

## Building BodyCypher's reference range architecture: a practical roadmap

The research points to a layered architecture that combines the best available sources in a specific priority order:

**Priority 1 — Use Thai-specific data where available.** The 2025 Thammasat biochemistry study (14 analytes), 2018 Siriraj CBC study, Thai NHES IV thyroid data, and Chulalongkorn HbA1c study collectively cover approximately **30–35 biomarkers** with Thai population validation. These should be your primary ranges for those analytes.

**Priority 2 — Fill gaps with Asian regional data.** The APFCB/IFCC Asian Multicenter Study (72 analytes, free interactive viewer at ccb-project.org) provides the next-best approximation using Vietnamese and Malaysian population data as proxies. The Chinese nationwide lipid study adds lipid-specific ranges. This adds roughly **40–50 unique analytes** not covered by Thai studies.

**Priority 3 — Use global gold-standard data for remaining analytes.** NHANES raw data (free, 200+ biomarkers) can be used to derive intervals for hormones, vitamins, minerals, and specialty markers lacking Asian-specific studies. Cross-reference against Tietz 7th edition, ARUP, and Mayo Clinic catalog entries. Apply documented Asian correction factors where they exist (creatinine, WBC, hemoglobin, liver enzymes).

**Priority 4 — Layer in optimal ranges.** For each biomarker, maintain both the population-based "normal" reference interval and a literature-cited "optimal" zone. Compile from the freely available functional medicine sources listed above, validated against peer-reviewed outcome studies. This dual-range display is what differentiates a wellness platform from a clinical lab report.

**Longer-term investment:** Consider partnering with a Thai medical school (Mahidol, Chulalongkorn, or Thammasat) to conduct a comprehensive Thai reference interval study covering your full panel. Given the 197,897-result Thammasat study was accomplished using existing hospital databases via indirect methods, a similar approach could cost-effectively establish Thai-validated ranges for 100+ analytes — creating a proprietary dataset that no competitor could replicate.

## Conclusion

The reference range landscape is fragmented by design — ISO 15189 deliberately delegates interval establishment to individual laboratories rather than centralizing it. This fragmentation is both the challenge and the opportunity. **No competitor has assembled a comprehensive, multi-layered, ethnicity-aware, optimal-range-inclusive biomarker database for the Thai market.** The ~dozen sources identified here provide the raw materials to build one. The most immediate wins are: downloading the harmonized NHANES CSV datasets, accessing the APFCB Asian interactive viewer at ccb-project.org, obtaining the 2025 Thammasat and 2018 Siriraj papers for Thai-specific anchoring, and compiling optimal ranges from the freely available functional medicine sources. Thailand's regulatory environment is permissive for wellness platforms — the PDPA data protection compliance, not reference range selection, is the higher-stakes legal requirement. The resulting database, if built rigorously and documented with citations, becomes both a product differentiator and a defensible data asset.

---

## Sources

1. Comparing Ethnicity-Specific Reference Intervals for Clinical Laboratory Tests from EHR Data (PMC) - https://pmc.ncbi.nlm.nih.gov/articles/PMC8404742/
2. Thailand Health Checkup Insights for Startup (Google Drive) - https://docs.google.com/document/d/1mShQ4QGYf9HXQD1KKxJyIdVaCmFVUSvCaproTn7YoTI/edit
3. Thai ISO 15189 Laboratory Quality Standards Development (TCI-ThaiJO) - https://he02.tci-thaijo.org/index.php/dmsc/article/view/247391
4. Thailand PDPA Guide (Cookie Information) - https://cookieinformation.com/what-is-the-thailand-pdpa/
5. nhanesA: achieving transparency and reproducibility in NHANES research (Oxford Academic) - https://academic.oup.com/database/article/doi/10.1093/database/baae028/7646470
6. Harmonized US NHANES 1988-2018 for high throughput exposome-health discovery (PMC) - https://pmc.ncbi.nlm.nih.gov/articles/PMC9934713/
7. Mayo Clinic Laboratories Test Catalog - https://www.mayocliniclabs.com/
8. CALIPER Project (SickKids) - http://www.sickkids.ca/Caliperproject/intervals/index.html
9. Reference intervals for 12 clinical laboratory tests in a Danish population: The Lolland-Falster Health Study (Taylor & Francis) - https://www.tandfonline.com/doi/full/10.1080/00365513.2020.1864833
10. Nordic Reference Interval Project Bio-bank and Database (NOBIDA) (PubMed) - https://pubmed.ncbi.nlm.nih.gov/15223705/
11. The Nordic Reference Interval Project 2000: recommended reference intervals for 25 common biochemical properties (PubMed) - https://pubmed.ncbi.nlm.nih.gov/15223694/
12. The Nordic Reference Interval Project 2000 (NORIP) (Westgard QC) - https://westgard.com/essays/guest-essay/guest28.html
13. Racial/Ethnic-Specific Reference Intervals for Common Laboratory Tests: A Comparison among Asians, Blacks, Hispanics, and White (PMC) - https://pmc.ncbi.nlm.nih.gov/articles/PMC4578165/
14. Racial/Ethnic-Specific Reference Intervals (PubMed) - https://pubmed.ncbi.nlm.nih.gov/26468426/
15. RefVal Viewer / APFCB-IFCC Asian Multicenter Study (CCB Project) - https://ccb-project.org/
16. Reference intervals for cardiometabolic risk factors in China: a national multicenter cross-sectional study (PMC) - https://pmc.ncbi.nlm.nih.gov/articles/PMC10904295/
17. Korea National Health and Nutrition Examination Survey (KNHANES) Biobank Project (ResearchGate) - https://www.researchgate.net/publication/392611736_Data_Resource_Profile_The_Statistics_of_the_Korea_National_Health_and_Nutrition_Examination_Survey_KNHANES_Biobank_Project
18. Functional Blood Test Ranges (OptimalDX) - https://www.optimaldx.com/optimal-range
19. Functional Blood Chemistry Analysis (OptimalDX) - https://www.optimaldx.com/
20. Functional Blood Chemistry Analysis Mastery Training Program (OptimalDX Academy) - https://academy.optimaldx.com/p/functional-blood-chemistry-mastery-training-program
21. The ODX Platform (Medical-Xprt) - https://www.medical-xprt.com/software/the-odx-platform-977916
22. InsideTracker Review: Personalized Health Optimization (Body Freedom) - https://www.bodyfreedom.org/insidetracker-review/
23. InsideTracker Science Page - https://www.insidetracker.com/science
24. InsideTracker: personalised potential for a longer life (Longevity.Technology) - https://longevity.technology/news/insidetracker-personalised-potential-for-a-longer-life/
25. Algorithm-Based Personalized Nutrition Platform Improves Key Blood Biomarkers (PR Newswire) - https://www.prnewswire.com/news-releases/algorithm-based-personalized-nutrition-platform-improves-key-blood-biomarkers-in-healthy-humans-300722478.html
26. Longitudinal analysis of biomarker data from a personalized nutrition platform (Nature Scientific Reports) - https://www.nature.com/articles/s41598-018-35249-y
27. Function Health - https://www.functionhealth.com/
28. Functional Lab Ranges (MyHealthManual) - https://myhealthmanual.com/selfhelp/functional_ranges/
29. Functional Medicine Lab Values Chart (Mind Body Functional Medicine) - https://mindbodyfunctionalmedicine.com/blog/functional-medicine-lab-values-chart/
30. Blood Biomarkers for Longevity: Evidence-Based Guide 2025 (Optimal Health) - https://optimalhealth.co/resources/blood-testing/biomarkers-longevity
31. Key Updates in FDA's 2026 General Wellness and Clinical Decision Support Software Guidance (Faegre Drinker) - https://www.faegredrinker.com/en/insights/publications/2026/1/key-updates-in-fdas-2026-general-wellness-and-clinical-decision-support-software-guidance
32. AI wellness or regulated medical device? A lawyer's guide to navigating FDA rules (Hogan Lovells) - https://www.hoganlovells.com/en/publications/ai-wellness-or-regulated-medical-device-a-lawyers-guide-to-navigating-fda-rulesand-what-could
33. How Functional Medicine Providers Look at "Optimal" Lab Ranges (Rupa Health) - https://www.rupahealth.com/post/how-functional-medicine-provider-look-at-optimal-lab-ranges
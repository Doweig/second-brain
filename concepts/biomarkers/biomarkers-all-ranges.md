---
type: product-research
date: 2026-02-01
source: manual
tags: [biomarkers, optimal-ranges, methodology]
people: [bryan-johnson, peter-attia, mark-hyman, andrew-huberman]
companies: [bodycypher, superpower, insidetracker, function-health, selfdecode, labsmarts, siphox-health, marek-health, optimaldx]
status: raw
---

# Building defensible optimal biomarker ranges: methodology and competitive landscape

**[[bodycypher|BodyCypher]]'s core challenge — that NHANES-derived ranges reflect "common among healthy" rather than "truly optimal" — is a well-documented limitation in laboratory medicine.** The IFCC formally distinguishes between Reference Intervals (descriptive population statistics) and Clinical Decision Limits (prescriptive thresholds from outcome data), and the two should never be conflated. The solution is a tiered hybrid system: clinical evidence overrides population data when strong trial evidence exists, while NHANES-filtered distributions serve as the best available proxy when it doesn't. [[insidetracker|InsideTracker]] is the closest commercial precedent, using exactly this dual approach with published validation, while most competitors (Function Health, [[superpower|Superpower]]) lack transparent methodology. Below is a comprehensive framework for building BodyCypher's system.

---

## The academic framework separates three distinct range types

Laboratory medicine formally recognizes three categories of interpretive limits, each with different derivation methods and purposes — and confusing them is BodyCypher's exact problem.

**Reference Intervals (RIs)** are defined by the CLSI standard EP28-A3c (formerly C28-A3) as the central 95% of values in a well-defined healthy reference population, using the 2.5th and 97.5th percentiles. The minimum recommended sample is 120 individuals using the non-parametric percentile method. By definition, **5% of healthy people fall outside the RI** — it describes what's typical, not what's optimal. This is what BodyCypher currently has from NHANES.

**Clinical Decision Limits (CDLs)** are thresholds above or below which a specific medical action is recommended. The IFCC Committee on Reference Intervals and Decision Limits (C-RIDL) published a definitive review (Ozarda et al., *Critical Reviews in Clinical Laboratory Sciences*, 2018) clarifying that RIs are *descriptive* while CDLs are *prescriptive* — derived from ROC curves, clinical trial outcomes, and expert consensus. Examples include AHA's LDL targets and ADA's HbA1c cutoffs. Ken Sikaris's Stockholm Hierarchy (2012) ranks CDLs based on clinical outcome studies as the **highest-quality** reference limits.

**Optimal/aspirational ranges** have no formal CLSI or IFCC standard. This is an emerging concept driven by wellness companies (InsideTracker, SelfDecode, OptimalDX) and longevity practitioners. These are narrower bands within the RI associated with lowest disease risk and best outcomes, typically derived from epidemiological outcome studies. The concept of **"Functional Reference Limits"** — inflection points in physiological relationships between paired biomarkers (e.g., vitamin D and PTH) — was introduced by Chuah et al. (*Annals of Laboratory Medicine*, 2023) as a formal category sitting between RIs and CDLs.

BodyCypher's NHANES-derived ranges are RIs. The company needs to layer CDLs and outcome-based optimal targets on top. The IFCC explicitly recommends clearly labeling which type of limit is being reported.

---

## Seven statistical pitfalls undermine population-based "optimal" ranges

BodyCypher's current approach — computing percentiles from a healthy NHANES subpopulation — has well-documented limitations that must be addressed before these ranges can be called "optimal."

**Right-skewed distributions invalidate symmetric methods.** CRP, ferritin, triglycerides, ALT, and insulin follow heavily right-skewed distributions. Applying mean ± 1 SD (as LabSmarts does by default) produces asymmetric intervals that may include physiologically implausible lower bounds. CRP requires natural-log transformation to approximate normality (Shapiro-Francia test p < 0.001 before transformation, p = 0.61 after). The CLSI recommends non-parametric percentile methods or Box-Cox transformation for non-Gaussian biomarkers.

**The "reference range fallacy"** is the core problem: even a carefully filtered healthy population reflects what's *common*, not what's *optimal*. Population means include individuals with subclinical or undiagnosed disease. For TSH, the standard lab range (0.4–4.5 mIU/L) is far wider than the range associated with lowest thyroid dysfunction risk (~1.0–2.0 mIU/L), because **95% of truly healthy individuals maintain TSH below 2.5**. The majority of the U.S. population is metabolically unhealthy, so even "healthy" filters leave residual confounding from subclinical insulin resistance, inflammation, and environmental exposures.

**Confounding persists even after strict filtering.** Genetic variation affects biomarker distributions by ethnicity. Subclinical conditions escape questionnaire-based exclusion. NHANES uses a posteriori exclusion (filtering after sampling) rather than a priori selection, which the IFCC notes produces inferior reference populations. Additionally, **age/sex stratification creates a sample-size tradeoff**: more granular partitioning improves precision but reduces subjects per stratum. The Harris-Boyd test (z* > 3.0) should be used to objectively determine when separate intervals are statistically warranted.

**P90 of healthy people ≠ optimal.** BodyCypher's LDL upper bound of 150 mg/dL (P90 of healthy population) illustrates this perfectly. The P90 describes where 90% of healthy people fall — it says nothing about whether 150 mg/dL minimizes cardiovascular risk. Clinical trial data (FOURIER, ODYSSEY) demonstrates continuous benefit down to LDL levels of 30–50 mg/dL.

---

## Outcome-based mortality curves define where "optimal" actually sits

The strongest evidence for truly optimal ranges comes from large prospective cohort studies modeling nonlinear dose-response relationships (U-curves, J-curves) between biomarker levels and mortality. These studies typically use **Cox proportional hazards models with restricted cubic splines** to identify the nadir — the biomarker level associated with lowest risk.

**The Pho et al. study (2021, *Clinical Chemistry*)** is the most directly relevant published work. Using NHANES 1999–2010 (N=30,651), the researchers tested 152 biomarkers within standard 10th–90th percentile reference intervals against all-cause mortality. **Twenty biomarkers within "normal" reference intervals significantly predicted mortality**, including albumin, RDW, alkaline phosphatase, and CRP. However, all 152 biomarkers combined explained only an additional **0.8% of mortality variance** beyond demographics — tempering expectations about individual biomarker predictive power.

Several large-scale studies reveal where optimal really sits:

- **Total cholesterol**: Yi et al. (2019, *Scientific Reports*, N=12.8 million) found a U-curve with optimal TC of **210–249 mg/dL** for most age-sex groups — *above* the standard guideline target of <200 mg/dL. This tension between CVD-focused guidelines and all-cause mortality data is critical for BodyCypher to navigate.
- **LDL cholesterol**: Liu et al. (2021, NHANES 1999–2014) found a U-shaped relationship with nadir around **100–129 mg/dL**. The lowest LDL group (<70 mg/dL) had HR 1.37 for all-cause mortality — likely reflecting reverse causation (severe illness lowering LDL) rather than true harm from low LDL.
- **HDL cholesterol**: ChinaHEART study (N=3.4 million) showed U-shaped association with optimal HDL of **50–79 mg/dL**. Very high HDL (>90–100 mg/dL) paradoxically increased mortality, particularly in men.
- **Hemoglobin**: Culleton et al. (*Blood*, 2006) found an inverse J-curve with lowest mortality at **13.0–15.0 g/dL (women)** and **14.0–17.0 g/dL (men)**.

These mortality-curve nadirs should inform BodyCypher's optimal ranges but require careful interpretation. Observational associations cannot establish causation (reverse causation is pervasive), and all-cause mortality nadirs sometimes conflict with disease-specific clinical targets. BodyCypher should document these tensions transparently.

---

## Evidence-based optimal targets for key biomarkers

For biomarkers where strong clinical evidence exists, the following targets should override NHANES-derived population ranges. These are drawn from major clinical guidelines (AHA/ACC, ESC/EAS, ADA, Endocrine Society) and the longevity medicine literature.

**Cardiovascular markers with overwhelming evidence:**

| Biomarker | Standard Range | Clinical Optimal | Longevity Target | Key Evidence |
|-----------|---------------|-----------------|-----------------|--------------|
| LDL-C | <130 mg/dL | **<100 mg/dL** (primary prevention) | <70 mg/dL | FOURIER, ODYSSEY; Mendelian randomization shows log-linear benefit |
| ApoB | 60–130 mg/dL | **<90 mg/dL** (primary prevention) | <60 mg/dL | ESC 2019 prefers ApoB over LDL-C; NLA 2024 confirms superiority |
| Triglycerides | <150 mg/dL | **<100 mg/dL** | <75 mg/dL | TG/HDL ratio is insulin resistance surrogate |
| hsCRP | <3.0 mg/L | **<1.0 mg/L** | <0.5 mg/L | JUPITER: LDL <70 + CRP <1 = 79% CVD risk reduction |
| Lp(a) | <50 mg/dL | **<30 mg/dL** | <14 mg/dL | Genetically determined; Mendelian randomization confirms causality |
| Homocysteine | 5–15 µmol/L | **<10 µmol/L** | 5–7.2 µmol/L | >9.8 µmol/L = 28% increased all-cause mortality |

**Metabolic markers with strong evidence:**

| Biomarker | Standard Range | Clinical Optimal | Longevity Target | Key Evidence |
|-----------|---------------|-----------------|-----------------|--------------|
| HbA1c | <5.7% normal | **<5.4%** | <5.0% | Continuous CVD/cancer/dementia association even in non-diabetic range |
| Fasting glucose | 70–99 mg/dL | **72–90 mg/dL** | 72–85 mg/dL | Continuous risk above 85 mg/dL in epidemiological data |
| Fasting insulin | 2.6–24.9 µU/mL | **<8 µU/mL** | <5 µU/mL | Rises years before glucose becomes abnormal |
| HOMA-IR | <2.5 | **<1.5** | <1.0 | Identifies subclinical atherosclerosis in normoglycemic individuals |

**Markers with moderate evidence (observational data, less RCT support):**

| Biomarker | Standard Range | Evidence-Based Optimal | Notes |
|-----------|---------------|----------------------|-------|
| Vitamin D | 30–100 ng/mL | **40–60 ng/mL** | 2024 Endocrine Society retreated from 2011 position; field contentious |
| TSH | 0.45–4.5 mIU/L | **1.0–2.0 mIU/L** | 95% of healthy individuals <2.5; upper limit has been inflated |
| Ferritin | 24–336 ng/mL (M) | **30–100 ng/mL** | Very high levels (>200) linked to inflammation and metabolic syndrome |
| Uric acid | 3.5–7.2 mg/dL (M) | **<5.0 mg/dL (M)** | URRAH study: <4.7 for all-cause mortality |
| ALT | 7–56 U/L | **<25 U/L (M), <20 (F)** | Attia notes "normal" upper limit inflated by worsening population liver health |
| GGT | 9–48 U/L (M) | **<25 U/L** | Independent predictor of CV and all-cause mortality |
| Testosterone (M) | 264–916 ng/dL | **>450 ng/dL** | Low T = 40% higher all-cause mortality |

**Markers where population data is the best proxy:** For albumin, MCV, RDW, total protein, globulin, electrolytes (Na, K, Cl, CO2), and most CBC components (WBC, RBC, hemoglobin, hematocrit, platelets), limited interventional evidence exists for targets distinct from normal ranges. NHANES-derived healthy population ranges are reasonable proxies, though lower-normal WBC (4–6K) is associated with lower inflammation, and elevated RDW independently predicts mortality.

---

## LabSmarts uses a simplistic mean ± 1 SD default — not peer-reviewed

Despite thorough searching, **no peer-reviewed academic publications authored by LabSmarts were found**. [[labsmarts|LabSmarts]] (labsmarts.com) is a commercial "functional blood chemistry analysis" software platform, not a research group. Their methodology uses a three-tier system:

1. **Lab Reference Ranges**: Sourced from clinical labs and the Fulgoni et al. (2019) NHANES study, which used piecewise regression on 44,000 healthy individuals to establish age/sex-specific RBC reference intervals.
2. **Optimal Ranges**: Default is **mean ± 1 standard deviation** (~68% of population). Where clinical outcome studies exist (e.g., hemoglobin mortality data from Culleton et al.), evidence-based thresholds replace this default.
3. **Alarm Ranges**: Mean ± 3 standard deviations.

The mean ± 1 SD approach is a pragmatic simplification with two critical flaws: it assumes the population mean *is* optimal (the reference range fallacy), and it assumes symmetric distributions (invalid for CRP, ferritin, triglycerides). BodyCypher should avoid this methodology and instead adopt the tiered clinical-evidence-first approach described below.

---

## Longevity practitioners push aggressive targets but rarely publish formal ranges

**[[peter-attia|Peter Attia]]** (author of *Outlive*) advocates ApoB of **30–40 mg/dL** (equivalent to a child's level), with an absolute ceiling of <60 mg/dL. He considers ApoB, Lp(a), OGTT with insulin, and hsCRP the most important tests, and views standard cholesterol panels as oversimplified. He notes ALT upper limits should be **<25 U/L (males)** and **<20 U/L (females)**, arguing the "normal" ceiling has been inflated by worsening population liver health. Most specific ranges are behind his premium paywall.

**[[bryan-johnson|Bryan Johnson]]** (Blueprint protocol) uses "Optimal Clinical Outcome Range" (OCOR) — self-coined terminology targeting levels seen in healthy 18-year-olds. His published targets are extremely aggressive: HbA1c <5.2% (achieves 4.5%), fasting insulin <5 µU/mL (achieves 3.0), LDL <70 mg/dL (achieves 45 using PCSK9 inhibitor), hsCRP <1.0 mg/L (achieves <0.1), and testosterone >450 ng/dL (achieves 941). His protocol costs reportedly $2M+/year and includes prescription medications (metformin, acarbose, rapamycin, Repatha) — making it an n=1 experiment, not a generalizable framework.

**[[mark-hyman|Mark Hyman]]** does not publish specific numeric ranges publicly. He emphasizes fasting insulin as "probably the most important test" and advocates ApoB and Lp(a) over standard lipid panels. His optimal ranges are embedded in Function Health's platform (which he co-founded), but the methodology is undocumented.

---

## InsideTracker leads in methodology transparency among competitors

### InsideTracker: the closest commercial precedent

InsideTracker (Segterra, Inc., founded 2009 by Gil Blander, PhD) operates the most scientifically rigorous and transparent methodology in the wellness blood testing space. Their dual-method approach directly parallels what BodyCypher aims to build:

**Method 1 — Literature curation**: A science team reviews peer-reviewed publications linking biomarker levels to longevity, disease prevention, and athletic performance. They claim to have curated **7,000+ clinical studies** from 35,000+ reviewed, using only human studies. Each recommendation is graded 1–5 stars based on study count, population size, journal impact factor, study design, and effect magnitude.

**Method 2 — Population database**: They explicitly use **NHANES data** (confirmed in their 2018 blog post updating optimal zones for LDL, HDL, total cholesterol, triglycerides, hsCRP, potassium, sodium, and SHBG) combined with their proprietary database of 120,000+ users. They "tease out the healthy population" from these data to establish distributional context.

InsideTracker personalizes optimal zones by **age, sex, ethnicity, and athletic activity level** — the most granular stratification among competitors. Their three-tier result system (red/at-risk, yellow/normal, green/optimal) places optimal zones as narrower bands within clinically normal ranges.

Critically, InsideTracker has **three peer-reviewed publications**: a 2018 *Scientific Reports* paper (co-authored with David Sinclair of Harvard) validating that their personalized recommendations improved 14 of 17 commonly out-of-range biomarkers; a 2023 *PLOS One* study on dose-response of running on biomarkers (N=28,000+ users); and a microbiome review co-authored with Jeffery Blumberg of Tufts.

**Key weakness**: No randomized controlled trial demonstrates that achieving InsideTracker's optimal zones improves hard clinical outcomes (mortality, disease incidence). Harvard's Dr. Pieter Cohen has publicly questioned whether sufficient evidence exists to define narrow optimal zones for every biomarker.

### Function Health: significant methodology gap

[[function-health|Function Health]] (founded 2022, $300M raised, Mark Hyman as Chief Medical Officer) tests **100+ biomarkers for $499/year** via Quest Diagnostics — the broadest panel at the most competitive price. Their advisory board includes JoAnn Manson (Harvard), [[andrew-huberman|Andrew Huberman]] (Stanford), and Toby Cosgrove (former Cleveland Clinic CEO).

However, **Function Health has published zero methodology documentation, white papers, or peer-reviewed research**. STAT News ran a November 2025 headline directly questioning: "Function Health has won over consumers. When will it publish evidence?" Their optimal ranges appear rooted in functional medicine clinical tradition — one collaborator attributed them to "the ranges Dr. Hyman uses in his clinical practice, based on years of clinical experience." Multiple reviewers have noted inconsistencies between visual plots and text descriptions, generic rather than truly personalized recommendations, and potential for inducing health anxiety through aggressive out-of-range flagging.

### SelfDecode: transparent literature review but no peer-reviewed validation

[[selfdecode|SelfDecode]] uses a three-step process: (1) Is there a range within normal associated with better outcomes? (2) Are there meaningful lifestyle interventions to reach it? (3) Do association studies link that range to longevity/disease prevention? Only when all three criteria are met do they define an optimal range. They publish extensive blog articles with **~22+ citations per biomarker** — more transparent than most competitors. They combine DNA analysis (83M+ variants) with lab results. However, they have **no peer-reviewed methodology papers**, and their supplement marketplace creates a conflict of interest.

### Other competitors vary widely in rigor

**Blueprint (Bryan Johnson)** uses "Optimal Clinical Outcome Range" (OCOR) — extremely aggressive, physician-developed targets. But OCOR is self-coined terminology, not an established standard, and the protocol includes prescription drugs unavailable to general consumers.

**Life Extension** (founded 1980) has advocated optimal ranges for 40+ years, publishing specific targets in their magazine (e.g., vitamin D optimal 50–80 ng/mL). Their longevity as a brand provides legitimacy, but they also sell supplements.

**Superpower** and **[[siphox-health|SiPhox Health]]** provide optimal ranges but with minimal published methodology. **[[marek-health|Marek Health]]** takes a clinician-directed approach rather than automated ranges. **Levels Health** publishes research-backed glucose targets (fasting 72–85 mg/dL) that are more conservative than ADA standards. **[[optimaldx|OptimalDX]]** (Dr. Dicken Weatherby) provides the foundational textbook and software for functional blood chemistry analysis, referenced by many companies.

**No published cross-company comparison of optimal ranges exists**, though platforms like OptimizeBiomarkers.com and LongevityAdvice.com provide informal comparisons.

---

## The recommended hybrid system: a three-tier evidence architecture

Based on all research, BodyCypher should implement the following framework, which mirrors IFCC terminology, uses GRADE-like evidence grading, and follows InsideTracker's commercial precedent.

### Tier classification

**Tier 1 — Clinical guideline override (strong RCT evidence).** These biomarkers have randomized controlled trial data establishing specific thresholds and multi-society guideline consensus. The clinical target replaces the NHANES-derived range entirely, with the NHANES distribution stored as supplementary context. Biomarkers: LDL-C, ApoB, triglycerides, HbA1c, fasting glucose, blood pressure, hsCRP.

**Tier 2 — Epidemiological evidence cap (strong observational data).** These biomarkers have consistent large-cohort epidemiological data linking levels to outcomes, with some guideline mentions but fewer RCTs defining precise thresholds. The optimal range is derived from outcome data and cross-referenced against the NHANES distribution. Biomarkers: HDL-C, fasting insulin, HOMA-IR, homocysteine, Lp(a), vitamin D, TSH, ferritin, uric acid, ALT, AST, GGT, testosterone.

**Tier 3 — Population proxy (limited clinical evidence).** NHANES healthy population data serves as the optimal range, using P25–P75 as the "optimal" band within a P10–P90 "normal" range. These are flagged for periodic evidence review. Biomarkers: albumin, MCV, RDW, total protein, globulin, electrolytes, most CBC components, BUN/creatinine.

### Decision algorithm

For each biomarker, the system should execute the following logic:

1. **If Tier 1**: Set range = clinical guideline target; cite specific guideline with recommendation class and level of evidence (e.g., "AHA/ACC 2018, Class I, LOE A"); compute the percentile of the clinical target within the NHANES healthy distribution as a sanity check — if the target falls below the 5th percentile of healthy adults, flag for review; store NHANES distribution as supplementary context.

2. **If Tier 2**: Set range = epidemiological evidence target; cite observational studies with outcome data; cross-reference against NHANES P10–P90 to validate achievability; label as "based on observational evidence; no RCT-validated threshold."

3. **If Tier 3**: Set range = NHANES P25–P75 (optimal) within P10–P90 (normal); use non-parametric methods for skewed biomarkers (CRP, ferritin, triglycerides); apply Harris-Boyd test for age/sex stratification; flag as "population-derived; periodic evidence review scheduled."

### Critical NHANES implementation details

BodyCypher must use **survey-weighted percentiles** (WTMEC2YR weights for single-cycle, combined weights for multi-cycle analysis) — failure to apply weights produces biased estimates. Use **reference method variables** (LBXGLU for glucose, not LBXSGL; LBXTC for cholesterol, not LBXSCH). Apply the Harris-Boyd partitioning test to determine when sex- or age-stratified intervals are statistically warranted (z* > 3.0). For skewed biomarkers, use log-transformation or non-parametric methods rather than assuming Gaussian distributions.

### Documentation requirements

Each biomarker record should contain: evidence tier, primary source type (guideline/epidemiological/population), specific citations with DOIs, NHANES distribution context, guideline disagreement notes (e.g., AHA vs. ESC LDL targets), semantic version number, last-reviewed date, and a changelog. This creates the "transparent and citable" methodology BodyCypher needs.

---

## A practical decision matrix for BodyCypher's ~49 biomarkers

For immediate implementation, BodyCypher should classify its biomarkers as follows:

**Override with clinical targets (Tier 1, ~7 biomarkers):** LDL-C (<100 mg/dL), ApoB (<90 mg/dL), triglycerides (<100 mg/dL), HbA1c (<5.4%), fasting glucose (72–90 mg/dL), hsCRP (<1.0 mg/L), and blood pressure (<120/80 mmHg). These have the strongest evidence and the largest gap between population ranges and optimal targets.

**Cap with epidemiological evidence (Tier 2, ~15 biomarkers):** HDL-C (40–80 mg/dL, noting J-curve), fasting insulin (<8 µU/mL), HOMA-IR (<1.5), Lp(a) (<30 mg/dL), homocysteine (<10 µmol/L), vitamin D (40–60 ng/mL), TSH (1.0–2.0 mIU/L), free T3/T4 (mid-range), testosterone (>450 ng/dL for males), ferritin (30–100 ng/mL), uric acid (<5.0 mg/dL for males), ALT (<25 U/L), AST (<25 U/L), GGT (<25 U/L), RDW (<13%).

**Use NHANES population proxy (Tier 3, ~25+ biomarkers):** Albumin, total protein, globulin, MCV, BUN, creatinine, electrolytes (Na, K, Cl, CO2), CBC components (WBC, RBC, hemoglobin, hematocrit, platelets, lymphocytes, neutrophils), total bilirubin, alkaline phosphatase, and any remaining biomarkers without strong outcome data.

---

## Conclusion: defensibility through transparency, not novelty

BodyCypher's competitive advantage should not come from inventing novel ranges — it should come from **the most transparent, citable, and evidence-graded system in the market**. Function Health's $300M valuation proves consumer demand exists, but their refusal to publish methodology (flagged by STAT News) creates a vulnerability. InsideTracker's published validation provides a credible precedent but lacks the tiered evidence framework that BodyCypher can build.

Three principles should guide implementation. First, adopt IFCC terminology — call NHANES ranges "Reference Intervals" and clinical targets "Clinical Decision Limits" to align with international laboratory medicine standards. Second, use GRADE-style evidence grading so users understand *why* each range is set where it is and how confident the evidence base is. Third, implement guideline surveillance (monitoring annual ADA Standards, ACC/AHA updates, ESC focused updates, and biennial NHANES releases) with semantic versioning so ranges evolve as evidence does.

The Pho et al. XWAS study (2021) provides the foundational academic justification: it proved that values *within* standard NHANES reference intervals predict mortality, validating the entire premise that "normal" ranges are insufficient. Pairing that finding with the tiered clinical-evidence-override system described here gives BodyCypher a defensible, publishable methodology that no current competitor has fully articulated.

---

## Sources

1. Chuah LL et al. "Functional Reference Limits: Describing Physiological Relationships and Determination of Physiological Limits for Enhanced Interpretation of Laboratory Results." *Annals of Laboratory Medicine*, 2023. https://pmc.ncbi.nlm.nih.gov/articles/PMC10151278/
2. Ozarda Y et al. "Distinguishing reference intervals and clinical decision limits — A review by the IFCC Committee on Reference Intervals and Decision Limits." *Critical Reviews in Clinical Laboratory Sciences*, 2018. https://pubmed.ncbi.nlm.nih.gov/30047297/
3. CLSI EP28-A3c (formerly C28-A3). "Defining, Establishing, and Verifying Reference Intervals in the Clinical Laboratory; Approved Guidelines." https://webstore.ansi.org/preview-pages/CLSI/preview_CLSI+C28-A3.pdf
4. Sikaris K. "Application of the Stockholm Hierarchy to defining the quality of reference intervals and clinical decision limits." *Clinical Biochemist Reviews*, 2012. https://pubmed.ncbi.nlm.nih.gov/23267246/
5. Jones GRD et al. "The Role and Limitations of the Reference Interval Within Clinical Chemistry and Its Reliability for Disease Detection." *Advances in Clinical Chemistry*, 2024. https://pmc.ncbi.nlm.nih.gov/articles/PMC10932992/
6. Haeckel R et al. "Big data and reference intervals: rationale, current practices, harmonization and standardization prerequisites and future perspectives of indirect determination of reference intervals using routine data." *Clinical Chemistry and Laboratory Medicine*, 2023. https://pmc.ncbi.nlm.nih.gov/articles/PMC10197285/
7. Pho N et al. "Association of 152 Biomarker Reference Intervals with All-Cause Mortality in Participants of a General United States Survey from 1999 to 2010." *Clinical Chemistry*, 2021. https://pmc.ncbi.nlm.nih.gov/articles/PMC8142683/
8. Yi SW et al. "Total cholesterol and all-cause mortality by sex and age: a prospective cohort study among 12.8 million adults." *Scientific Reports*, 2019. https://pmc.ncbi.nlm.nih.gov/articles/PMC6367420/
9. Liu X et al. "Association between low density lipoprotein cholesterol and all-cause mortality: results from the NHANES 1999–2014." *Scientific Reports*, 2021. https://www.nature.com/articles/s41598-021-01738-w
10. Wang Y et al. "Association of high-density lipoprotein cholesterol with all-cause and cause-specific mortality in a Chinese population of 3.3 million adults: a prospective cohort study." *The Lancet Regional Health – Western Pacific*, 2023. https://www.thelancet.com/journals/lanwpc/article/PIIS2666-6065(23)00192-X/fulltext
11. Ridker PM et al. "The JUPITER Trial: C-Reactive Protein, LDL Cholesterol, and Cardiovascular Risk." *Circulation: Cardiovascular Quality and Outcomes*, 2010. https://www.ahajournals.org/doi/10.1161/circoutcomes.109.868299
12. AHA/ACC. "Standardization of Apolipoprotein B, LDL-Cholesterol, and Non-HDL-Cholesterol." *Journal of the American Heart Association*, 2024. https://www.ahajournals.org/doi/10.1161/JAHA.123.030405
13. National Lipid Association. "Role of apolipoprotein B in the clinical management of cardiovascular risk in adults: An Expert Clinical Consensus." 2024. https://pubmed.ncbi.nlm.nih.gov/39256087/
14. Kozakowski J et al. "Early insulin resistance in normoglycemic low-risk individuals is associated with subclinical atherosclerosis." *Cardiovascular Diabetology*, 2023. https://link.springer.com/article/10.1186/s12933-023-02090-1
15. Endocrine Society. "2024 Vitamin D Clinical Practice Guideline Update." https://endocrinenews.endocrine.org/to-d-or-not-to-d-what-questions-does-the-latest-endocrine-society-guideline-answer-about-vitamin-d-supplements/
16. Horváth-Szalai Z et al. "Reference intervals: current status, recent developments and future considerations." *Biochemia Medica*, 2016. https://pmc.ncbi.nlm.nih.gov/articles/PMC4783089/
17. GRADE Working Group. "Assessment of the strength of recommendation and quality of evidence: GRADE checklist." 2022. https://pmc.ncbi.nlm.nih.gov/articles/PMC9671561/
18. InsideTracker. "How We Define Your Optimized Zones of Health and Performance." https://blog.insidetracker.com/how-we-define-your-optimized-zones-health-and-performance
19. InsideTracker. "Surviving Vs. Thriving: An Update To Our Optimal Zones." https://blog.insidetracker.com/surviving-versus-thriving-updated-optimal-zones
20. InsideTracker. "How does InsideTracker determine optimized zones?" https://support.insidetracker.com/en-US/how-does-insidetracker-determine-optimized-zones-288940
21. InsideTracker Science Page. https://www.insidetracker.com/science
22. Blander G et al. "Longitudinal analysis of biomarker data from a personalized nutrition platform in healthy subjects." *Scientific Reports*, 2018. https://pmc.ncbi.nlm.nih.gov/articles/PMC6168584/
23. STAT News. "Function Health has won over consumers. When will it publish evidence?" November 2025. https://www.statnews.com/2025/11/20/function-health-won-consumers-when-evidence-health-tech/
24. SelfDecode. "Lab Tests: Normal Range vs. Optimal Range." https://selfdecode.helpscoutdocs.com/article/415-optimal-range-explained
25. LabSmarts. "Functional Blood Chemistry Analysis — Bibliography." https://labsmarts.com/bibliography/
26. OptimalDX (Dr. Dicken Weatherby). "Functional Blood Test Ranges." https://www.optimaldx.com/optimal-range
27. Nucleus. "Peter Attia's Recommended Blood Tests." https://mynucleus.com/blog/peter-attia-recommended-blood-tests
28. Fast Life Hacks. "Peter Attia's Top 5 Most Important Blood Tests." https://fastlifehacks.com/peter-attia-top-5-blood-tests/
29. YourDailyWay. "Bryan Johnson's Blueprint Protocol — The Definitive 2025 Guide." https://www.yourdailyway.com/posts/bryan-johnson-testing-protocol/
30. Life Extension. "Top Annual Blood Tests." https://www.lifeextension.com/magazine/2020/5/top-annual-blood-tests
31. Crown Counseling. "Function Health vs InsideTracker vs Superpower: Best Lab Work." https://crowncounseling.com/reviews/function-health-vs-superpower-vs-outlive/
32. CDC NHANES Data Portal. https://wwwn.cdc.gov/nchs/nhanes/
33. MedCalc. "Reference Interval — Statistical Software Manual." https://www.medcalc.org/en/manual/referenceinterval.php
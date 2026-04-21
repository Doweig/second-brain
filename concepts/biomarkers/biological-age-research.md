---
type: product-research
date: 2026-02-01
source: manual
tags: [biomarkers, biological-age, phenoage, health-scoring]
people: []
companies: [bodycypher]
status: raw
---

# Biological age from blood: what BodyCypher needs to know before v1

**Blood-based biological age is a scientifically validated population-level metric being marketed as a consumer product before the science fully supports individual-level precision — but it remains a powerful engagement driver that can be implemented defensibly.** PhenoAge, the most practical approach, uses just 9 standard blood biomarkers available from routine Thai health checkups, has published open-source code, and predicts mortality with a C-Index of 0.750. However, day-to-day fluctuation in blood markers can swing the score by several years, and no medical body recognizes biological age for clinical decision-making. The recommended path for [[bodycypher|BodyCypher]]: **build it as a secondary "Health Score" feature atop your primary biomarker tracking product, not as the headline value proposition.**

---

## The science is real but the precision is overstated

Two validated, blood-biomarker-only methods dominate the field. **PhenoAge** (Levine et al., 2018) was trained on NHANES III (n=9,926) using elastic-net Cox regression on aging-related mortality. It requires exactly 9 markers — albumin, creatinine, fasting glucose, CRP (log-transformed), lymphocyte percentage, mean cell volume, red cell distribution width, alkaline phosphatase, and white blood cell count — plus chronological age. Each 1-year increase in PhenoAge above chronological age corresponds to a **9% increase in all-cause mortality risk**. The formula is published, open-source, and can be computed in 5 lines of Python.

The **Klemera-Doubal Method (KDM)** takes a different approach: it regresses each biomarker independently on chronological age, then combines them via weighted average minimizing estimation error. It uses 10–12 markers (albumin, ALP, BUN, creatinine, CRP, HbA1c, total cholesterol, SBP, uric acid, lymphocyte %, MCV, WBC) and is sex-specific. InsideTracker's InnerAge 2.0 is built on this framework. The BioAge R package by Kwon & Belsky implements both PhenoAge and KDM with NHANES data pre-loaded.

A critical 2023 advance came from **Bortz et al.**, who trained an Elastic-Net Cox model on 306,116 UK Biobank participants, achieving a **C-Index of 0.778** — an 11% improvement over PhenoAge. Their key finding: using common clinical panels with as few as **5–8 biomarkers plus imputation** of missing markers barely degraded accuracy (average C-Index drop of only 0.008). This is the most practical paper for a startup to build on. The code is open-source on GitHub.

The epigenetic clocks — GrimAge, DunedinPACE — remain the gold standard for mortality prediction (**GrimAge HR = 1.81 per SD**) but require DNA methylation arrays costing $300–500+ per assay. They are impractical for a consumer app in Thailand. GrimAge uses methylation surrogates for 7 plasma proteins plus smoking pack-years. DunedinPACE uniquely measures the *pace* of aging (how fast you're aging now) rather than accumulated age, making it the most sensitive to interventions — but still requires expensive lab processing.

## How consumer companies actually do it

The market divides cleanly into two tiers: companies using standard blood panels (accessible, less validated) and those using epigenetic/proteomic assays (expensive, more validated).

**[[insidetracker|InsideTracker]]** ($99–499) is the closest analogue to what BodyCypher would build. Their InnerAge 2.0 uses **17 markers for males, 13 for females** via the Klemera-Doubal framework, spanning metabolic, liver, immune, and hormone categories. Each biomarker individually adds or subtracts years from chronological age. User reviews praise actionable recommendations but criticize score volatility — one user reported their immune markers alone added 7 years after testing with a mild cold. **[[function-health|Function Health]]** ($365–499/year) tests 100+ biomarkers and offers a biological age metric, though their algorithm is undisclosed. **[[mito-health|Mito Health]]** (Singapore, YC-backed, $399) similarly tests 100+ markers with an undisclosed proprietary algorithm. None of these companies have published independent peer-reviewed validation of their specific biological age algorithms.

On the epigenetic side, **[[trudiagnostic|TruDiagnostic]]** ($229–499) offers the most comprehensive reports: DunedinPACE plus 11 organ-system ages from 900,000+ CpG methylation sites, backed by 15+ peer-reviewed publications. **[[elysium-health|Elysium Index]]** ($299–499), developed with Morgan Levine, claims the best precision (0–1.5 year deviation between replicates vs. 3–9 years for competitors). **[[glycanage|GlycanAge]]** ($348–599) takes a novel approach, measuring IgG glycan ratios that respond to lifestyle changes in weeks rather than months — but has no mortality prediction studies.

The free option worth noting: **[[agelessrx|AgelessRx]] hosts a PhenoAge calculator** requiring just those 9 standard markers. **Aging.AI** by [[insilico-medicine|Insilico Medicine]] offers a free deep-learning-based calculator using 10–41 blood markers. Both demonstrate that the technical barrier to building a biological age feature is negligible — the challenge is in framing, UX, and scientific credibility.

## NHANES makes implementation straightforward

A startup can realistically build a biological age model from publicly available data in weeks, not months. NHANES III data (freely available from CDC) with linked mortality follow-up provides the training set. NHANES IV provides validation. The **Biolearn Python library** loads NHANES data automatically and computes PhenoAge with minimal code. The **BioAge R package** implements KDM, PhenoAge, and homeostatic dysregulation with built-in NHANES training and validation pipelines.

For adults, predicting chronological age from standard blood biomarkers yields a **mean absolute error of 5–7 years** with 9–12 markers, dropping to ~4.5–5.5 years with 25+ markers and ML methods. The overall R² across the full lifespan is **0.60–0.92**, but for the working-age adult population (18–65), it drops to **0.25–0.77** depending on age band. Biological age estimates typically range **±20 years from chronological age** across populations, with chronically ill individuals showing PhenoAge approximately **5–10 years older** than their calendar age.

The age-prediction-residual approach (predicted age minus actual age) is scientifically valid but inferior to the mortality-based approach. PhenoAge directly optimizes for health-relevant outcomes rather than chronological age prediction, avoiding what researchers call the "biomarker paradox" — a marker that perfectly predicts chronological age is useless for biological age because the residual would be zero. The mortality-based approach is preferred in the literature and only marginally more complex to implement.

The most predictive standard blood biomarkers, consistently ranked across studies: **albumin** (ranked #1 most often), **glucose/HbA1c**, **alkaline phosphatase**, **creatinine**, **CRP**, and **red cell distribution width**. Going from 5 to ~10 markers provides the largest accuracy improvement; beyond 15–20 markers, returns diminish sharply. Adding **cystatin C** — not standard in most panels — produces the single largest incremental improvement per the UK Biobank analysis.

## Organ-level scoring is desirable but the science isn't there yet for standard panels

The Wyss-Coray lab's 2023 Nature paper is the landmark work: training LASSO models on **893 organ-enriched plasma proteins** measured via SomaScan assay across 11 organs (brain, heart, liver, kidney, lung, immune, fat, arteries, intestines, muscle, pancreas). They found ~20% of healthy adults over 50 have at least one organ aging significantly faster than average, and **multi-organ agers face 6.5× mortality risk**. Heart aging confers a **250% increased heart failure risk**. The 2025 UK Biobank follow-up (44,498 individuals, Olink proteomics) confirmed these associations over 17-year follow-up.

This research is scientifically groundbreaking but **completely impractical for a consumer app** — SomaScan measures ~5,000 proteins at $1,000–5,000+ per assay. The brain aging model alone requires 202 specialized low-abundance proteins undetectable on standard panels.

What BodyCypher *can* do is **organ system health scoring** from standard markers — conceptually different from organ biological age but still valuable. The feasible systems from a Thai health checkup panel:

- **Kidney** (★★★★★): creatinine, BUN, eGFR (calculated), uric acid — highly stable, well-validated
- **Metabolic** (★★★★★): fasting glucose, HbA1c, TG/HDL ratio — very stable (HbA1c CVw just 1.5%)
- **Liver** (★★★★☆): ALT, AST, ALP, albumin, bilirubin, GGT, FIB-4 score — moderately stable
- **Hematologic** (★★★★☆): full CBC provides 15+ parameters — remarkably stable over time
- **Cardiovascular** (★★★☆☆): TC, LDL, HDL, triglycerides, ±hsCRP — more variable (TG CVw 5–25%)
- **Immune** (★★★☆☆): WBC differential, NLR ratio, ±hsCRP — useful but fluctuates with acute illness

InsideTracker's 10 "Healthspan Category Scores" using 6–14 blood biomarkers each represents the closest consumer model. No company currently offers organ-specific biological *age* from standard blood panels — only organ *health scores*. Frame accordingly: call these "system health scores," not "organ age."

## The honest reckoning: fluctuation, credibility, and what users actually want

The single largest risk for BodyCypher is **day-to-day marker fluctuation producing misleading results**. Dehydration concentrates blood, inflating albumin, creatinine, and WBC — all PhenoAge inputs. Acute exercise transiently raises WBC by 10–20% and CRP within 24–48 hours. A common cold can dramatically spike WBC and CRP while dropping albumin. A study of ~5 million individuals found that **51 of 75 blood assays** were significantly affected by ambient temperature on the day of the blood draw. These fluctuations can produce **several years of variation in PhenoAge** between measurements taken days apart with no real change in underlying aging rate.

No medical association (AMA, WHO, or Thai medical bodies) recognizes biological age testing for clinical decision-making. Luigi Ferrucci, Scientific Director of the National Institute on Aging, states plainly: **"At this point, if you want to do it, it must be based on curiosity."** Different clocks give different results for the same person — the Berlin Aging Study II found "at best moderate correlations between the various biological age measures."

Yet user research consistently shows biological age scores are powerful engagement drivers. Users value, in order: **(1) trend tracking** ("Am I improving?"), **(2) actionable recommendations** ("What should I change?"), **(3) the score itself** (as emotional anchor and conversation starter), and **(4) biomarker-level breakdown** ("What's driving my score?"). The number without guidance frustrates users. Multiple Trustpilot reviews of InsideTracker complain about paying for "the same blood test my doctor does" when recommendations feel generic. The value is in the interpretation layer, not the computation.

## The Thailand-specific picture and what to build

Standard Thai health checkup packages (3,700–25,000 THB) include most PhenoAge inputs. A basic package covers CBC (yielding WBC, lymphocyte %, MCV, RDW), fasting glucose, creatinine, and usually ALT/AST/ALP. **CRP is the critical gap** — absent from basic packages but included in comprehensive/premium packages. Albumin appears in full liver panels but not always in basic ones. A startup would need to either require comprehensive packages, partner with labs to add CRP (~200–500 THB incremental cost), or develop a degraded-accuracy mode without CRP.

PhenoAge was trained on American (NHANES) data. Thai users may have systematically different baseline biomarker distributions — particularly for glucose metabolism, lipid profiles, and inflammatory markers. Without population recalibration, accuracy for Thai users is uncertain. The Bortz model's imputation approach offers a partial solution, and NHANES does include Asian-American subgroups, but this remains a genuine limitation that should be disclosed.

Under Thai FDA guidelines, a wellness app calculating scores from user-inputted blood results would likely classify as a **Non-Medical Device** — similar to "fitness apps and general sleep monitoring tools." Making diagnostic or disease-prevention claims would trigger medical device classification. The PDPA (Thailand's GDPR equivalent, effective since June 2022) treats blood test results as sensitive personal data requiring explicit consent.

## The build-vs-defer decision matrix

**Build for v1** if BodyCypher can implement these safeguards:

- Use PhenoAge as the underlying model (published, peer-reviewed, open-source, zero licensing cost)
- Present it as a "Health Score" or "Vitality Index," not "Biological Age" — show a range (e.g., "38–44") rather than a single number like "41.3"
- Design the UX around **trends and trajectories**, not point-in-time scores
- Bundle **actionable, biomarker-specific recommendations** — this is where users perceive value
- Provide standardized pre-test instructions (fasting, morning, no exercise 48h, no alcohol 24h) and flag results when conditions weren't met
- Include clear disclaimers: wellness tool, not diagnostic, population-based estimate, results vary with testing conditions
- Add system-level health scores (kidney, metabolic, liver, blood, cardiovascular) as the richer, more defensible product layer

**Defer if** the product cannot guarantee CRP availability across target labs, or if the v1 scope is too constrained to build proper framing (ranges, trends, disclaimers, recommendations). A biological age number without the interpretation layer is worse than no number — it becomes a source of anxiety rather than motivation.

**The minimum viable implementation**: Implement PhenoAge using the published formula (available in Python via Biolearn or from the original paper's coefficients). Require the 9 markers from a comprehensive Thai panel. Show results as a band with ±3-year confidence range. Display trend arrows comparing to previous tests. Provide 3–5 specific, biomarker-linked recommendations per test. This is scientifically defensible, technically trivial (days of engineering, not months), and delivers genuine user value — all while acknowledging its limitations honestly. The deeper product moat lies in the system-level health scores, longitudinal tracking, and personalized recommendations that sit alongside the biological age metric.

**Cost to implement**: Essentially zero for the algorithm (open-source code, published coefficients). The investment is in UX design, recommendation engine, disclaimer framework, and lab partnerships — all of which serve BodyCypher's core product regardless of whether the bio-age feature ships.

---

## Conclusion

Biological age from bloodwork occupies a scientifically legitimate but commercially overhyped middle ground. The population-level validity is strong — PhenoAge and KDM genuinely predict mortality with meaningful effect sizes. The individual-level precision is weak — daily fluctuations, population calibration mismatches, and the absence of clinical recognition all constrain what a single score can honestly claim. For BodyCypher, the right move is to **build it as an engagement wrapper around the more defensible core product of biomarker tracking and system-level health scoring**. PhenoAge provides a published, zero-cost, 9-marker foundation that works with Thai comprehensive checkup panels. Frame it with humility — ranges not numbers, trends not snapshots, insights not diagnoses. The companies winning in this space (InsideTracker, Function Health) succeed not because their biological age algorithms are superior, but because their recommendation engines make abstract lab numbers feel personally actionable. That interpretation layer, not the age calculation itself, is where BodyCypher should invest its v1 engineering budget.

---

## Sources

1. [Biological age estimation using circulating blood biomarkers | Communications Biology](https://www.nature.com/articles/s42003-023-05456-z)
2. [A new aging measure captures morbidity and mortality risk across diverse subpopulations from NHANES IV: A cohort study | PLOS Medicine](https://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.1002718)
3. [A 25 Component Blood Biomarker Aging Clock Improves on 9 Component PhenoAge – Fight Aging!](https://www.fightaging.org/archives/2025/10/a-25-component-blood-biomarker-aging-clock-improves-on-9-component-phenoage/)
4. [PhenoAge Calculator – Biological Age Calculator | Vitadel](https://www.vitadel.com/biological-age-calculator)
5. [PhenoAge Test – My Aging Tests](https://myagingtests.com/product/phenoage-biological-age-test/)
6. [A toolkit for quantification of biological age from blood chemistry and organ function test data: BioAge - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC8602613/)
7. [An epigenetic biomarker of aging for lifespan and healthspan - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC5940111/)
8. [Biological Age Test - Entering Results | AgelessRx](https://agelessrx.com/biological-age-test-entering-result/)
9. [Biological Ageing: More Than Just a Number](https://www.i-screen.com.au/blog/biological-ageing-more-than-just-a-number)
10. [Calculating Phenotypic Age from biomarkers with Python and numpy | Synth & Syntax](https://omux.dev/blog/calculating-phenotypic-age-with-python/)
11. [Guide to Biological Age Testing | Levels | Levels](https://www.levels.com/blog/guide_to_biological_age)
12. [An epigenetic biomarker of aging for lifespan and healthspan - PubMed](https://pubmed.ncbi.nlm.nih.gov/29676998/)
13. [A Biomarker-based Biological Age in UK Biobank: Composition and Prediction of Mortality and Hospital Admissions - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC8202154/)
14. [Why You Need a Biological Age Blood Test - Unlocking Insights - Explore Our Articles](https://www.insidetracker.com/a/articles/why-you-need-a-biological-age-blood-test)
15. [A toolkit for quantification of biological age from blood chemistry and organ function test data: BioAge - PubMed](https://pubmed.ncbi.nlm.nih.gov/34725754/)
16. [GitHub - dayoonkwon/BioAge: Biological Age Calculations Using Several Biomarker Algorithms](https://github.com/dayoonkwon/BioAge)
17. [(PDF) Biological age estimation using circulating blood biomarkers](https://www.researchgate.net/publication/375018228_Biological_age_estimation_using_circulating_blood_biomarkers)
18. [Biological age estimation using circulating blood biomarkers - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC10603148/)
19. [GitHub - bortzjd/bloodmarker_BA_estimation: Code walkthrough of calculation of biological age acceleration using blood biomarkers and Full ENC model for a single sample observation, as per article "Biological Age Estimation Using Circulating Blood Biomarkers"](https://github.com/bortzjd/bloodmarker_BA_estimation)
20. [GrimAge Outperforms Other Epigenetic Clocks in the Prediction of Age-Related Clinical Phenotypes and All-Cause Mortality | The Journals of Gerontology: Series A | Oxford Academic](https://academic.oup.com/biomedgerontology/article/76/5/741/5992253)
21. [Epigenetic and Metabolomic Biomarkers for Biological Age: A Comparative Analysis of Mortality and Frailty Risk | The Journals of Gerontology: Series A | Oxford Academic](https://academic.oup.com/biomedgerontology/article/78/10/1753/7194006)
22. [An epigenetic predictor of death captures multi-modal measures of brain health | Molecular Psychiatry](https://www.nature.com/articles/s41380-019-0616-9)
23. [DNA methylation GrimAge strongly predicts lifespan and healthspan | Aging](https://www.aging-us.com/article/101684/text)
24. [Biological Age Test - Private Blood Test at Home – Alchemy by Effect Doctors](https://alchemybyeffectdoctors.com/products/biological-age-test)
25. [“GrimAge,” an epigenetic predictor of mortality, is accelerated in major depressive disorder | Translational Psychiatry](https://www.nature.com/articles/s41398-021-01302-0)
26. [What your fears about the future might reveal about your cellular age](https://www.psypost.org/what-your-fears-about-the-future-might-reveal-about-your-cellular-age/)
27. [DunedinPACE, a DNA methylation biomarker of the pace of aging - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC8853656/)
28. [A Unified Framework for Systematic Curation and Evaluation of Aging Biomarkers | bioRxiv](https://www.biorxiv.org/content/10.1101/2023.12.02.569722v6.full)
29. [Best Blood Tests for Biological Age | 2026 Guide & Discounts](https://simplyantiaging.com/best-blood-tests-for-biological-age/)
30. [InsideTracker Review - Keep Health](https://keep.health/insidetracker-review/)
31. [InsideTracker Ultimate Review: The Best Online Blood Biomarker Testing?](https://outliyr.com/insidetracker-ultimate-review)
32. [InsideTracker Review: Is InsideTracker Legit?](https://www.generationlab.com/blog/insidetracker-review)
33. [Function | 100 Healthy Years](https://www.functionhealth.com/)
34. [Mito Health - Products, Competitors, Financials, Employees, Headquarters Locations](https://www.cbinsights.com/company/mito-health)
35. [Know Your Kits: The Difference Between TruAge and Elysium Index | GlycanAge](https://glycanage.com/blog/lifestyle/truage-vs-elysium-index-review)
36. [DunedinPACE, a DNA methylation biomarker of the pace of aging - PubMed](https://pubmed.ncbi.nlm.nih.gov/35029144/)
37. [TruDiagnostic](https://www.rupahealth.com/lab-companies/trudiagnostic)
38. [The Top Biological Age Tests For Maximum Longevity](https://outliyr.com/best-biological-age-tests)
39. [TruDiagnostic™ Biological Age Test](https://www.trudiagnostic.com/)
40. [Index – Biological Age Test | Elysium Health](https://www.elysiumhealth.com/products/index)
41. [The Science Behind Index | Elysium Health](https://www.elysiumhealth.com/pages/science-behind-index)
42. [Biological Age Test - Discover Your Biological Age | GlycanAge](https://glycanage.com/)
43. [Best Biological Age Test 2026: GlycanAge, TruDiagnostic & More Compared | AevumAI](https://theaevumai.com/post/biological-age-test-2026)
44. [Metabolic Age: All You Need To Know About | GlycanAge](https://glycanage.com/blog/lifestyle/metabolic-age-all-you-need-to-know-about)
45. [Aging.AI | Deep Biomarkers Of Human Aging](http://www.aging.ai/)
46. [Biological Age Predictors: The Status Quo and Future Trends - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC9739540/)
47. [BioAge/README.md at master · dayoonkwon/BioAge](https://github.com/dayoonkwon/BioAge/blob/master/README.md)
48. [Biolearn, an open-source library for biomarkers of aging | bioRxiv](https://www.biorxiv.org/content/10.1101/2023.12.02.569722v4.full)
49. [A toolkit for quantification of biological age from blood-chemistry and organ-function-test data: BioAge | medRxiv](https://www.medrxiv.org/content/10.1101/2021.08.28.21262759v1.full)
50. [Deep biomarkers of human aging: Application of deep neural networks to biomarker development | Aging](https://www.aging-us.com/article/100968/text)
51. [Prediction of chronological and biological age from laboratory data | Aging](https://www.aging-us.com/article/102900/text)
52. [Biological Age Estimation Using Circulating Blood Biomarkers | medRxiv](https://www.medrxiv.org/content/10.1101/2023.02.23.23285864v1.full)
53. [https://doi.org/10.1038/s41514-025-00312-2 Received: 23 June 2025](https://www.nature.com/articles/s41514-025-00312-2_reference.pdf)
54. [Clarifying the biological and statistical assumptions of cross-sectional biological age predictors: an elaborate illustration using synthetic and real data | BMC Medical Research Methodology | Full Text](https://bmcmedresmethodol.biomedcentral.com/articles/10.1186/s12874-024-02181-x)
55. [Deep learning for biological age estimation | Briefings in Bioinformatics | Oxford Academic](https://academic.oup.com/bib/article/22/2/1767/5828124)
56. [Explainable machine learning framework for biomarker discovery by combining biological age and frailty prediction | Scientific Reports](https://www.nature.com/articles/s41598-025-98948-3)
57. [Biological age estimation using circulating blood biomarkers - PubMed](https://pubmed.ncbi.nlm.nih.gov/37884697/)
58. [Organ aging signatures in the plasma proteome track health and disease | Nature](https://www.nature.com/articles/s41586-023-06802-1)
59. [Tracking organ aging and disease | National Institutes of Health (NIH)](https://www.nih.gov/news-events/nih-research-matters/tracking-organ-aging-disease)
60. [Full article: Age is Just a Number: Can Proteomic Analysis Provide Insight into the Aging Body?](https://www.tandfonline.com/doi/full/10.2144/btn-2024-0008)
61. [Organ aging signatures in the plasma proteome track health and disease - PubMed](https://pubmed.ncbi.nlm.nih.gov/38057571/)
62. [(PDF) Organ aging signatures in the plasma proteome track health and disease](https://www.researchgate.net/publication/376268309_Organ_aging_signatures_in_the_plasma_proteome_track_health_and_disease)
63. [Plasma proteomics links brain and immune system aging with healthspan and longevity | Nature Medicine](https://www.nature.com/articles/s41591-025-03798-1)
64. [Blood proteins reveal biological age of human organs to help track health and disease - SomaLogic](https://somalogic.com/blog/blood-proteins-reveal-biological-age-of-human-organs-to-help-track-health-and-disease/)
65. [Within-Person Variability in Kidney Measures - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC3628297/)
66. [Biological variation in serum lipid concentrations - PubMed](https://pubmed.ncbi.nlm.nih.gov/2189212/)
67. [InsideTracker Review: Is This Optimized Health Plan Worth It? - Unlocking Insights - Explore Our Articles](https://www.insidetracker.com/a/articles/insidetracker-review-is-this-optimized-health-plan-worth-it)
68. [The 10 Blood Tests That Focus on Your Health Goals](https://blog.insidetracker.com/healthspan-category-testing)
69. [Ultimate—Live healthier longer](https://store.insidetracker.com/products/ultimate)
70. [Why Do Blood Test Results Vary? | imaware](https://www.imaware.health/blog/why-do-blood-test-results-vary)
71. [Reference Values for Athlete Hydration Assessment During Competition, | OAJSM](https://www.dovepress.com/reference-values-for-hydration-biomarkers-optimizing-athletic-performa-peer-reviewed-fulltext-article-OAJSM)
72. [Blood Biomarker Profiling and Monitoring for High-Performance Physiology and Nutrition: Current Perspectives, Limitations and Recommendations - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC6901403/)
73. [Variation in Laboratory Reports: Causes other than Laboratory Error - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC9200014/)
74. [Variation in common laboratory test results caused by ambient temperature - ScienceDirect](https://www.sciencedirect.com/science/article/pii/S2666634021003779)
75. [Can You Really Measure Your Biological Age? The Science Behind the Hype](https://hslongevity.com/can-you-really-measure-your-biological-age/)
76. [You can order a test to find out your biological age. Is it ...](https://www.npr.org/sections/health-shots/2024/02/05/1228753141/biological-age-test-dna)
77. [Using blood test parameters to define biological age among older adults: association with morbidity and mortality independent of chronological age validated in two separate birth cohorts - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC9768057/)
78. [American Journal of Epidemiology](https://moffittcaspi.trinity.duke.edu/sites/moffittcaspi.trinity.duke.edu/files/Belsky_AJE_reduced_0.pdf)
79. [InsideTracker Reviews | Read Customer Service Reviews of insidetracker.com | 3 of 30](https://www.trustpilot.com/review/insidetracker.com?page=3)
80. [Bangkok Health Checkup: Costs, Packages, and Hospitals](https://www.expatden.com/thailand/medical-check-up-bangkok/)
81. [Health check-up in Thailand – Bangkok Health Service](https://bangkokhealthservice.com/health-check-up-in-thailand/)
82. [Quantifying Biological Age | Michael Lustgarten](https://michaellustgarten.com/2019/09/09/quantifying-biological-age/)
83. [Genetic associations for two biological age measures point to distinct aging phenotypes - Kuo - 2021 - Aging Cell - Wiley Online Library](https://onlinelibrary.wiley.com/doi/10.1111/acel.13376)
84. [Population Specific Biomarkers of Human Aging: A Big Data Study Using South Korean, Canadian, and Eastern European Patient Populations - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC6175034/)
85. [Thailand: Guidelines for Determining Health-Type Software Products](https://andamanmed.com/thailand-guidelines-for-determining-health-type-software-products/)
86. [Digital Health in Thailand, Vietnam, and Indonesia - Lexology](https://www.lexology.com/library/detail.aspx?g=b469d284-4867-49bd-abd3-ec15439ca1aa)
87. [Full article: Reference Values for Hydration Biomarkers: Optimizing Athletic Performance and Recovery](https://www.tandfonline.com/doi/full/10.2147/OAJSM.S508656)
88. [GitHub - KyteProject/phenotypic-age-calc: A simple script that translates Dr Levines Phenotypic Age algorithm into a biological age.](https://github.com/KyteProject/phenotypic-age-calc)
89. [The Most Affordable Lab-Based Epigenetic Age Tool - The PhenoAge Calculator](https://www.drkarafitzgerald.com/2024/08/01/the-most-affordable-lab-based-epigenetic-age-tool-the-phenoage-calculator/)
90. [Younger You - PhenoAge - Dr. Kara Fitzgerald](https://www.drkarafitzgerald.com/younger-you-phenoage/)
91. [Biomarkers selection and mathematical modeling in biological age estimation | npj Aging](https://www.nature.com/articles/s41514-023-00110-8)
92. [Association of accelerated biological aging with brain volumes: A cross-sectional study - ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S0165032724012886)
93. [Ranking Biomarkers of Aging by Citation Profiling and Effort Scoring - PMC](https://pmc.ncbi.nlm.nih.gov/articles/PMC8176216/)
94. [How We Select the Blood Biomarkers in Our Tests](https://blog.insidetracker.com/select-blood-biomarkers-tests)

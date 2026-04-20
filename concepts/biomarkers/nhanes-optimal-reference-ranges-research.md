---
type: product-research
date: 2026-02-01
source: manual
tags: [biomarkers, reference-ranges, nhanes]
people: []
companies: [bodycypher]
status: raw
---

# NHANES-derived optimal reference ranges: what exists and where to find it

**No single, comprehensive "optimal reference range" dataset derived from NHANES exists as a ready-to-download file -- but the building blocks are remarkably close.** The gap between raw NHANES data and finished optimal ranges has been partially bridged by several academic papers publishing reference intervals for specific biomarker panels, one complete open-source R pipeline, and powerful indirect-estimation R packages that can automate much of the work. The most actionable resources are a published R pipeline that computes reference intervals directly from NHANES, two landmark papers covering 152 and 27 biomarkers respectively, and the `refineR` package that can estimate reference intervals without manually filtering healthy subjects.

---

## The closest things to a finished dataset

Three published works come closest to a downloadable table of NHANES-derived reference intervals:

**Pho et al. (2021), *Clinical Chemistry* 67(3):500-507** computed reference intervals (10th-90th percentiles) for **152 biomarkers** from NHANES 1999-2010 (N=30,651) and tested their association with all-cause mortality. Twenty biomarkers showed mortality risk even when values fell within standard reference intervals -- exactly the kind of evidence that motivates "optimal" ranges. The supplementary materials include the full biomarker list with computed intervals. This is the broadest single-paper coverage of NHANES-derived reference intervals available. (PMC8142683; authors: Pho, Manrai, Leppert, Chertow, Ioannidis, **Patel**)

**Nguyen, Colacino, Chung, Le Goallec, Jolliet, Patel (2021), *The Lancet Healthy Longevity* 2(10):e651-e662** analyzed 27 physiological indicators versus all-cause mortality in 47,266 NHANES adults and derived **mortality-based cutoffs** -- thresholds at which mortality risk increases by 10%. These are conceptually closer to "optimal ranges" than percentile-based intervals because they define boundaries based on health outcomes rather than population statistics. Of the 27 indicators, 25 showed non-linear mortality associations, and many cutoffs differed substantially from current clinical thresholds. (PMID: 34825242)

**Horn & Pesce (2005), *Reference Intervals: A User's Guide*, AACC Press** -- this book shipped with a **CD-ROM containing NHANES III data for 27,900 individuals across 33 clinical chemistry analytes** in SAS and Excel formats, plus pre-calculated reference intervals using both nonparametric and robust methods. Their earlier paper (Horn & Pesce 2003, *Clinica Chimica Acta* 334:5-23) computed reference intervals for those 33 analytes from NHANES III, filtering for physician-rated "Excellent" health status, stratified by age, sex, and ethnicity. The book is out of print but findable, and the methodology remains the gold standard for direct NHANES reference interval computation.

---

## The best open-source code pipeline

**Bunch (2022), *J Mass Spectrom Adv Clin Lab* 24:22-30** published a complete, peer-reviewed R pipeline with full source code at **https://github.com/dustinrbunch/jmsacl_reference_interval** that computes indirect reference intervals directly from NHANES data. The pipeline ingests NHANES 2017-2018 biochemistry data (BIOPRO_J.XPT, DEMO_J.XPT, ALQ_J.XPT, MCQ_J.XPT), partitions by sex and health conditions, normalizes distributions via Box-Cox transformation, removes outliers using the Tukey method, and estimates reference intervals using Gaussian mixture models (`mixtools`). It demonstrates the full workflow for **testosterone and AST** and can be extended to any NHANES biomarker. This is the single most directly actionable resource -- a working, published, reproducible pipeline that does exactly the task in question. (PMC8889237)

A complementary tutorial from **Ghent University's PSLS biostatistics course** (https://gtpb.github.io/PSLS20/pages/04-dataExploration/04-Data-exploration-NHANES.html) walks through filtering the R `NHANES` package for healthy subjects (non-smoker, non-diabetic, healthy BMI, age 40-65), assessing normality, and computing a reference interval for systolic blood pressure -- a clean pedagogical example of the direct method.

---

## Two R packages that change the calculus

The **`refineR`** package (CRAN; v2.0.0, November 2025) deserves special attention because it eliminates the hardest step -- filtering for healthy subjects. Developed by Roche scientists and published in *Scientific Reports* (Ammer et al. 2021, 11:16023), refineR uses an **indirect method** that statistically separates pathological from non-pathological distributions using Box-Cox transformed normal distributions with regularized maximum likelihood. In benchmarks it achieved **2.77% mean percentage error**. The practical workflow is simple: partition NHANES data by age and sex, then call `findRI(data_vector)` to get estimated 2.5th and 97.5th percentiles of the healthy distribution -- no exclusion criteria needed. A step-by-step practical guide was published in *J Applied Lab Medicine* (Ammer et al. 2023, 8(1):84).

The **`referenceIntervals`** package (CRAN; v1.3.1) implements the **CLSI EP28-A3c** standard directly -- parametric, nonparametric, and robust reference interval calculation with confidence intervals and multiple outlier detection methods. For the direct method (pre-filtered healthy subset), this is the standard tool: filter NHANES for healthy subjects using exclusion criteria, then pass each biomarker vector to `refLimit()`.

For NHANES data access, the **`nhanesA`** package (CRAN; v1.4.1) provides comprehensive download/browsing of all NHANES tables and is the standard R interface. The **`RNHANES`** package from Silent Spring Institute adds survey-weighted quantile computation via `nhanes_quantile()`, which handles NHANES's complex survey design properly.

---

## Published reference intervals for specific biomarker panels

Multiple high-quality papers have computed and published NHANES-derived reference intervals for specific biomarker groups, each with detailed methodology and supplementary tables:

- **CBC/RBC markers**: Fulgoni et al. (2019), *Am J Clin Pathol* 151(2):128-142 -- reference intervals for RBC count, hemoglobin, hematocrit, MCH, MCHC, MCV, and RDW from NHANES 1999-2012 (n=44,328; ~21,139 healthy after excluding 27 conditions). Used piecewise regression for age breakpoints, stratified by sex. This paper's exclusion criteria list (Table 1) is a directly reusable template for defining a "healthy" NHANES subset. (PMC6306047)

- **Thyroid function**: Hollowell et al. (2002), *JCEM* 87:489-499 -- the landmark US population TSH/T4 reference intervals from NHANES III. Boucai & Surks (2009), *Thyroid* 19(6):549-554 -- age/sex/ethnicity-specific TSH reference limits with programmable predictive equations. Zhang et al. (2025), *Annals of Internal Medicine* 178(7) -- the most recent, reclassifying **48.5%** of subclinical hypothyroidism diagnoses as normal when using demographic-specific intervals.

- **Testosterone**: Vesper et al. (2015), *Clin Chem* 61(12):1495-1504 -- LC-MS/MS-measured testosterone percentiles by age, sex, and race from NHANES 2011-2012. Jasuja et al. (2019), *JCEM* (PMC6735742) -- testosterone percentiles in a rigorously healthy NHANES subset (never-smoking, lean, no comorbidities).

- **NT-proBNP**: Selvin et al. (2023), *Clinical Chemistry* (PMID: 37279581) -- reference intervals from NHANES 1999-2004 for children, adolescents, and adults using robust methods, partitioned by age and sex.

- **Vitamin B6**: Masse et al. (2020) (PMID: 32791332) -- race-, sex-, and age-specific reference intervals for pyridoxal 5'-phosphate from NHANES 2007-2010 (n=9,069; 4,463 healthy after exclusions).

---

## What the specific organizations actually offer

**LabSmarts** has the most transparent commercial methodology. Their bibliography page (https://labsmarts.com/bibliography/) documents every reference range source with PubMed links. Their approach: **optimal ranges = 1 standard deviation from the lab mean** (covering ~68% of the population), versus the standard 2 SD (~95%). For RBC markers specifically, they use the Fulgoni et al. 2019 NHANES-derived ranges with adjustments for gender, age, elevation, and pregnancy. No peer-reviewed papers or downloadable data, but the methodology is openly described.

**OptimalDX / Dicken Weatherby** does not derive ranges from NHANES or population statistics. Their ranges combine literature review with clinical tradition from "early pioneers in FBCA" -- they explicitly acknowledge some ranges are "not substantiated by research" but based on "clinical observations after examining thousands of results." Their textbook (*Blood Chemistry and CBC Analysis*) is the field's standard reference but uses a different methodology than population-based computation.

**Chirag Patel's lab at Harvard** produced the Pho et al. 2021 paper (152 biomarkers) and co-authored the harmonized NHANES dataset. Their NHANES browser (https://nhanes.hms.harvard.edu) and exposome-phenome atlas (http://apps.chiragjpgroup.org/pe_atlas/) provide powerful exploration tools, but they have not published a standalone "optimal reference range" table -- their framing is exposome-health associations and mortality prediction rather than clinical reference interval reform.

**The Nguyen/Patel/Jolliet team** published the harmonized NHANES 1988-2018 dataset (https://figshare.com/articles/dataset/NHANES_1988-2018/21743372) with 135,310 participants and 5,078 variables -- the most comprehensive cleaned NHANES substrate available (also on Kaggle and HuggingFace). Their Lancet Healthy Longevity paper provides mortality-based cutoffs for 27 indicators, but no comprehensive reference interval table.

**CALIPER** (https://caliperproject.ca/) offers a **free online lookup tool and mobile app** for pediatric reference intervals across 200+ biomarkers from 14,000+ healthy Canadian children, following CLSI methodology -- but it is pediatric-only and provides individual lookups, not bulk downloadable data. Their white paper (Taylor & Francis, 2017, doi:10.1080/10408363.2017.1379945) contains extensive reference interval tables.

**NORIP** (Nordic Reference Interval Project) published common adult reference intervals for 25 biochemical/hematological parameters from ~3,000 healthy Scandinavian adults across 102 labs. Results are published in *Scandinavian Journal of Clinical and Laboratory Investigation* but the raw data is not freely downloadable. **IFCC GRID** (https://grid.ifcc.org/) aims to compile reference intervals globally but functions as a portal rather than a downloadable database.

---

## A practical recipe for computing optimal ranges

The most efficient path to a comprehensive set of NHANES-derived optimal reference ranges, given what exists today, combines existing resources:

1. **Start with the Nguyen harmonized NHANES dataset** (Figshare) or use `nhanesA` to pull specific lab tables -- this gives you 134K+ participants with labs, demographics, and health questionnaires already merged.

2. **Define "healthy" using Fulgoni et al.'s exclusion criteria** -- their 27-condition exclusion list (no anemia, CHF, CHD, angina, MI, cancer, gout, emphysema, liver disease, celiac, stroke, thyroid conditions, HepC, HIV, specific medications) is the most rigorously defined healthy-subset filter published for NHANES and maps directly to NHANES questionnaire variables.

3. **Choose your method**: the **direct method** (filter healthy subjects -> `referenceIntervals::refLimit()`) gives you traditional CLSI-compliant intervals. The **indirect method** (`refineR::findRI()` on the full unfiltered dataset, partitioned by age/sex) is faster and arguably more robust, as it statistically separates pathological distributions without subjective exclusion criteria.

4. **For "optimal" (1 SD) rather than "normal" (2 SD) ranges**, simply adjust the percentile boundaries -- compute the mean +/- 1 SD (or 16th-84th percentiles) of the healthy distribution instead of the 2.5th-97.5th. The `refineR` package outputs the estimated non-pathological distribution parameters, from which any percentile can be derived.

5. **Validate against published ranges** using the individual-biomarker papers cited above (Fulgoni for CBC, Hollowell/Zhang for TSH, Vesper/Jasuja for testosterone, etc.) and against the Pho et al. 152-biomarker table as a broad cross-check.

---

## Conclusion

The gap in the literature is clear and specific: **many researchers have computed NHANES-derived reference intervals for individual biomarker panels, but no one has assembled these into a single comprehensive, freely downloadable dataset covering the full clinical chemistry panel with age/sex stratification.** The Bunch (2022) R pipeline at https://github.com/dustinrbunch/jmsacl_reference_interval provides the closest thing to a turnkey solution -- extend it from its two demo biomarkers to the full panel. The `refineR` package dramatically simplifies the statistical work by eliminating the need for subjective healthy-subject filtering. And the Pho et al. and Nguyen et al. mortality papers provide an evidence base for outcome-optimized thresholds that goes beyond simple percentile narrowing. The tools and data are all freely available; what's missing is someone stitching them together into a single comprehensive output -- which, given these resources, is now a tractable weekend project rather than a research program.

---

## Sources

1. **Pho et al. (2021)** -- "Association of 152 Biomarker Reference Intervals with All-Cause Mortality" -- *Clinical Chemistry* 67(3):500-507 -- https://pubmed.ncbi.nlm.nih.gov/33674838/ / https://pmc.ncbi.nlm.nih.gov/articles/PMC8142683/ / https://academic.oup.com/clinchem/article/67/3/500/6016141
2. **Nguyen et al. (2021)** -- "Characterising the relationships between physiological indicators and all-cause mortality (NHANES)" -- *The Lancet Healthy Longevity* 2(10):e651-e662 -- https://www.thelancet.com/journals/lanhl/article/PIIS2666-7568(21)00212-9/fulltext
3. **Nguyen et al. (2023)** -- "Harmonized US NHANES 1988-2018 for high throughput exposome-health discovery" -- *Scientific Data* -- https://pubmed.ncbi.nlm.nih.gov/36798185/ / https://www.medrxiv.org/content/10.1101/2023.02.06.23284573v1.full
4. **Nguyen et al. harmonized NHANES dataset** -- Figshare -- https://figshare.com/articles/dataset/NHANES_1988-2018/21743372
5. **Bunch (2022)** -- "Indirect reference intervals using an R pipeline" -- *J Mass Spectrom Adv Clin Lab* 24:22-30 -- https://pmc.ncbi.nlm.nih.gov/articles/PMC8889237/ / https://pubmed.ncbi.nlm.nih.gov/35252947/
6. **Bunch (2022) GitHub repo** -- R pipeline source code -- https://github.com/dustinrbunch/jmsacl_reference_interval
7. **Ammer et al. (2021)** -- "refineR: A Novel Algorithm for Reference Interval Estimation from Real-World Data" -- *Scientific Reports* 11:16023 -- https://www.nature.com/articles/s41598-021-95301-2
8. **Ammer et al. (2023)** -- "Estimation of Reference Intervals from Routine Data Using the refineR Algorithm -- A Practical Guide" -- *J Applied Lab Medicine* 8(1):84 -- https://academic.oup.com/jalm/article/8/1/84/6847917
9. **refineR R package** -- CRAN -- https://cran.r-project.org/web/packages/refineR/vignettes/refineR_package.html
10. **referenceIntervals R package** -- CRAN -- https://cran.r-project.org/web/packages/referenceIntervals/index.html / https://github.com/cran/referenceIntervals/blob/master/DESCRIPTION
11. **nhanesA R package** -- CRAN / GitHub -- https://cran.r-project.org/web/packages/nhanesA/vignettes/Introducing_nhanesA.html / https://github.com/cjendres1/nhanes
12. **RNHANES R package** -- Silent Spring Institute -- https://github.com/SilentSpringInstitute/RNHANES
13. **Fulgoni et al. (2019)** -- "Establishing Pediatric and Adult RBC Reference Intervals With NHANES Data Using Piecewise Regression" -- *Am J Clin Pathol* 151(2):128-142 -- https://pmc.ncbi.nlm.nih.gov/articles/PMC6306047/ / https://pubmed.ncbi.nlm.nih.gov/30285066/
14. **Hollowell et al. (2002)** -- TSH/T4 reference intervals from NHANES III -- *Clinical Chemistry* 48(10):1802 -- http://clinchem.aaccjnls.org/content/48/10/1802
15. **Boucai & Surks (2009)** -- "An Approach for Development of Age-, Gender-, and Ethnicity-Specific Thyrotropin Reference Limits" -- *Thyroid* -- https://pmc.ncbi.nlm.nih.gov/articles/PMC3012447/
16. **Zhang et al. (2025)** -- "Thyroid Function Reference Intervals by Age, Sex, and Race: A Cross-Sectional Study" -- *Annals of Internal Medicine* -- https://pubmed.ncbi.nlm.nih.gov/40324200/
17. **Vesper et al. (2015)** -- "Serum Total Testosterone Concentrations in the US Household Population from the NHANES 2011-2012 Study Population" -- *Clinical Chemistry* -- https://pmc.ncbi.nlm.nih.gov/articles/PMC5698798/
18. **Jasuja et al. (2019)** -- "Nationally Representative Estimates of Serum Testosterone Concentration in Never-Smoking, Lean Men Without Aging-Associated Comorbidities" -- *JCEM* -- https://pmc.ncbi.nlm.nih.gov/articles/PMC6735742/
19. **Selvin et al. (2023)** -- "NT-proBNP Reference Intervals in Healthy U.S. Children, Adolescents, and Adults" -- *Clinical Chemistry* -- https://pubmed.ncbi.nlm.nih.gov/37279581/
20. **Masse et al. (2020)** -- "Establishing race-, gender- and age-specific reference intervals for pyridoxal 5'-phosphate in the NHANES population" -- https://pubmed.ncbi.nlm.nih.gov/32791332/
21. **LabSmarts** -- Bibliography / reference range methodology -- https://labsmarts.com/bibliography/ / https://labsmarts.com/rbc-reference-range-adjustments/
22. **OptimalDX** -- Optimal ranges documentation -- https://kb.optimaldx.com/the-odx-optimal-ranges
23. **Weatherby & Ferguson** -- *Blood Chemistry and CBC Analysis: Clinical Laboratory Testing from a Functional Perspective* -- https://www.amazon.com/Blood-Chemistry-CBC-Analysis-Perspective/dp/0976136716
24. **Chirag Patel's lab** -- Harvard -- https://www.chiragjpgroup.org/ / https://dash.harvard.edu/entities/person/25d1d89b-efd6-46da-ada0-b9bfbffefc8a
25. **CALIPER Project** -- https://caliperproject.ca/
26. **CALIPER white paper (2017)** -- https://pubmed.ncbi.nlm.nih.gov/29017389/
27. **CALIPER -- Abbott ARCHITECT reference intervals** -- https://www.researchgate.net/publication/222051094
28. **ADLM (formerly AACC)** -- "Modern Reference Intervals" (2021) -- https://myadlm.org/cln/articles/2021/july/modern-reference-intervals
29. **Ghent University PSLS biostatistics tutorial** -- NHANES reference interval walkthrough -- https://gtpb.github.io/PSLS20/pages/04-dataExploration/04-Data-exploration-NHANES.html
30. **Semantic Scholar** -- Nguyen et al. harmonized NHANES paper -- https://www.semanticscholar.org/paper/Harmonized-US-National-Health-and-Nutrition-Survey-Nguyen-Middleton/2fe5f1f66b7840d2b5d8cdccded5ee90f04a2b25

---
type: product-research
date: 2026-02-01
source: manual
tags: [biomarkers, reference-ranges, data-sources]
people: []
companies: [bodycypher]
status: raw
---

# Biomarker Data Sources Research

*February 2026*

---

## Purpose

Identify open-source databases and datasets that provide biomarker reference ranges for [[bodycypher|BodyCypher]]'s blood testing platform. The goal is to find either a ready-to-use reference range dataset (biomarker, healthy low, healthy high, unit, sex) or the tools to build one efficiently.

---

## Key Finding

**There is no single downloadable open-source CSV of "reference ranges for common blood biomarkers."** This is partly because reference ranges vary by lab method, population, and who defines "healthy" vs "optimal." Labs like Quest and Labcorp each publish their own. The landscape splits into three tiers:

1. **Clinical reference range tables** (PDF/web) - Available from ABIM, Medscape, Geeky Medics, Wikipedia. Comprehensive but not machine-readable. Best option for a quick manual compilation (~4-6 hours of work for 50-80 biomarkers).
2. **Raw population data** (NHANES) - 134,000+ participants with lab results. Gold mine for computing custom "optimal" ranges, but requires significant data processing. This is the LabSmarts/OptimalDX methodology.
3. **Biomarker databases** (MarkerDB, awesome-biomarkers) - Built for researchers studying disease-biomarker associations, not for building clinical reference range tables. Limited practical value for BodyCypher's use case.

---

## 1. NHANES Harmonized Dataset (1988-2018)

### What it is
The National Health and Nutrition Examination Survey, harmonized by Nguyen et al. (2023) into a single clean dataset. Merges 614 separate CDC files across 30 years of surveys. Published in Nature Scientific Data with peer-reviewed curation.

### The dataset
- **134,310 participants**, 5,078 variables across 10 modules
- **Direct download:** Figshare [1], 5.62 GB total (version 9, updated Feb 2025)
- **Format:** CSV files + R data objects + data dictionary
- **License:** CC BY 4.0 - fully open for commercial use

### The 10 modules

| Module | Variables | BodyCypher relevance |
|---|---|---|
| response | 1,040 | Lab results: CBC, lipids, metabolic panels, hormones, vitamins. **The gold mine.** |
| demographics | 281 | Age, sex, ethnicity, income. For stratifying reference ranges. |
| questionnaire | 1,444 | Medical conditions, physical activity, diabetes. For filtering "healthy" subjects. |
| chemicals | 598 | Environmental exposures (lead, mercury, pesticides). Low relevance. |
| dietary | 324 | Food consumption data. Low relevance. |
| medications | 29 | Drug usage. Moderate - useful for filtering. |
| mortality | 15 | Death records from National Death Index. Low for now. |
| occupation | 61 | Job-related data. Not relevant. |
| weights | 857 | Survey sampling weights. Technical - needed for proper population estimates. |
| comments | 505 | Flags for measurements below/above detection limits. Technical companion. |

### Files you actually need (4 of 35)
- Cleaned response CSV (lab results)
- Cleaned demographics CSV (age/sex)
- Cleaned questionnaire CSV (health status for filtering)
- dictionary_nhanes.csv (Rosetta Stone for all 5,078 variables)

### The LabSmarts methodology
Companies like LabSmarts and OptimalDX sell proprietary "optimal reference ranges" computed from NHANES. Their approach:

1. Take the NHANES response module (lab results)
2. Filter for healthy subjects using the questionnaire module (no chronic diseases, no smoking, healthy BMI, etc.)
3. Join with demographics for age/sex stratification
4. Compute tighter "optimal" ranges (mean +/- 1 SD) vs broad clinical "normal" ranges (mean +/- 2 SD)
5. Stratify by age groups (18-30, 31-45, 46-60, 60+) and sex

**Assessment:** Powerful for building proprietary optimal ranges, but this is a research project, not a quick data pull. Requires Python/R skills and several days of work. More relevant for Phase 2 differentiation than MVP.

### Alternative NHANES access methods
- **CDC direct (raw files):** Individual .xpt files by cycle, requires manual merging [2]
- **Python package:** `pip install nhanes` (poldrack/nhanes on GitHub) [3]
- **R package:** CRAN NHANES package - subset of data for teaching [4]
- **Mirador scripts:** Python scripts to download and aggregate from CDC FTP [5]

### Key paper
Nguyen et al. (2023). "Harmonized US NHANES 1988-2018 for high throughput exposome-health discovery." Nature Scientific Data. medRxiv preprint [6].

### Next step: Deep research needed
A deep research prompt has been prepared to find whether anyone has already computed optimal reference ranges from NHANES and published the results as a downloadable dataset, step-by-step tutorial, or supplementary table in an academic paper. This would eliminate the need to process raw NHANES data from scratch.

---

## 2. MarkerDB 2.0

### What it is
A biomedical research database mapping 40,000+ biomarkers to disease conditions with concentration values. Built by the Wishart Lab at the University of Alberta.

### Access
- **Web interface:** markerdb.ca [7]
- **Downloads page:** old.markerdb.ca/downloads [8]
- **License:** CC BY-NC 4.0 - requires permission for commercial use

### What the downloads actually contain
The download page offers TSV/XML files organized by biomarker type (Chemical, Protein, Genetic, Karyotype) and category (Diagnostic, Predictive, Exposure). We downloaded and analyzed the "Diagnostic Chemical markers" file:

- **3,275 rows** mapping **981 chemical metabolites** to **304 disease conditions**
- Each row says: "when someone has [condition X], this chemical is at [concentration Y] in [biofluid Z]"
- Biofluids: Blood (1,642 rows), Urine (1,025), Cerebrospinal Fluid (414), Feces (93), Saliva (85)

### Why it's NOT useful for BodyCypher
MarkerDB categorizes biomarkers by molecular type. Standard blood panel markers are split across categories in unintuitive ways:

- **Missing entirely:** Ferritin, Hemoglobin, TSH, HbA1c, Triglycerides (zero rows in the chemicals file - these are proteins or not in the database)
- **Present but buried:** Glucose (26 rows), Testosterone (10 rows), Cholesterol (38 rows) - each spread across multiple disease conditions and biofluids
- **"Creatinine" = 1,040 rows** - because it appears as the normalization unit (umol/mmol creatinine) in most urine measurements

**Assessment:** Built for researchers asking "which metabolites change in disease X?" Not for building clinical reference ranges for a wellness blood panel. Skip this for MVP purposes.

### Citation
Jackson et al. (2025). "MarkerDB 2.0: a comprehensive molecular biomarker database for 2025." Nucleic Acids Research, 53(D1), D1415-D1426 [9].

---

## 3. awesome-biomarkers (GitHub)

### What it is
A community-driven open-source database of blood tests and biomarkers created by Mark Koester.

### Access
- **Repository:** github.com/markwk/awesome-biomarkers [10] (434 stars)
- **License:** CC0 (public domain) - fully open, free for commercial use
- **Clone:** `git clone https://github.com/markwk/awesome-biomarkers.git`

### What's inside
Two key data files:
- `blood_tests_db.json` - Machine-readable database of blood tests/biomarkers
- `blood_tests_schema.json` - JSON schema defining data structure

Coverage: ~52 biomarkers with descriptions across CBC, Lipids, CMP, hormones, vitamins. Fields include biomarker name, test grouping, descriptions, health categories, common test flag.

Also includes:
- Google Sheets BiomarkerDB (community-built) [11]
- Biomarker Tracker template (Google Sheets) [12]

### Assessment
Good structural scaffold but NOT comprehensive enough for BodyCypher's 50-100+ marker panels. No reference ranges included - just descriptions and categorizations. Useful as a starting point for data schema design, not as a reference range source.

---

## 4. Clinical Reference Range Sources (Best for MVP)

These are the most practical sources for building a reference range table manually. Not machine-readable, but comprehensive and authoritative.

### ABIM Laboratory Reference Ranges
- **Source:** American Board of Internal Medicine [13]
- **Format:** PDF
- **Coverage:** ~200 lab tests with sex-specific ranges
- **Status:** Gold standard used by US physicians. Updated January 2025.

### Medscape Lab Values
- **Source:** Medscape/WebMD [14]
- **Format:** Web page
- **Coverage:** Comprehensive lab values with sex-specific ranges, units in both conventional and SI
- **Includes:** Testosterone, glucose, ferritin, hormones, CBC, metabolic panels

### Wikipedia Reference Ranges for Blood Tests
- **Source:** Wikipedia [15]
- **Format:** Web page with tables
- **Coverage:** Surprisingly comprehensive, well-sourced, with both conventional and SI units
- **Includes:** Visual scale showing concentration ranges across biomarker types

### Geeky Medics Reference Ranges
- **Source:** Geeky Medics [16]
- **Format:** Clean web tables
- **Coverage:** Common panels (CBC, U&E, LFT, TFT, lipids, glucose, hormones)
- **Good for:** Quick reference with clean formatting

### ACCP/PSAP Lab Values Table
- **Source:** American College of Clinical Pharmacy [17]
- **Format:** PDF table
- **Coverage:** Core lab values with SI conversion

### Monash Health Pathology Reference Intervals
- **Source:** Monash Health [18]
- **Format:** PDF master list
- **Coverage:** Very detailed with age/sex stratification, method-specific intervals, and citations for each range

### Assessment
For BodyCypher's MVP, a manual compilation from these sources (~4-6 hours) would produce a working reference range table for 50-80 biomarkers. This is the pragmatic path. The doctor co-founder can then refine ranges based on clinical experience and Thai lab standards.

---

## 5. Additional Resources Discovered

### LOINC (Lab Test Codes)
- **Download:** loinc.org/downloads [19] (free account required)
- **What it is:** 108,000+ standardized lab test codes
- **Relevance:** Essential for normalizing Thai lab reports to standard identifiers
- **License:** Free for commercial use with attribution

### HMDB (Human Metabolome Database)
- **Access:** hmdb.ca [20]
- **What it is:** Contains nutrient-biomarker relationships, age/sex-specific concentration ranges
- **Relevance:** Source for many MarkerDB reference values. Free access.

### CALIPER Project
- **What it is:** Canadian Laboratory Initiative on Pediatric Reference Intervals
- **Coverage:** Reference ranges from 14,000 healthy children (ages 0-18)
- **Relevance:** Pediatric ranges only. Integrated into MarkerDB 2.0.

### BIONDA Database
- **Access:** bionda.mpc.ruhr-uni-bochum.de [21]
- **What it is:** Text-mining-based database of published biomarker-disease associations
- **Coverage:** 520,000+ biomarker-disease tuples from automated literature mining
- **Relevance:** Research tool, not reference range source

### Biomarker Data Repository (BmDR)
- **Managed by:** C-Path (Critical Path Institute) [22]
- **Focus:** Novel translational safety biomarkers (kidney, liver, muscle)
- **Access:** Restricted, requires data sharing agreement
- **Relevance:** Drug development focused, not consumer wellness

---

## 6. Licensing Summary

| Source | License | Commercial use |
|---|---|---|
| NHANES (Figshare harmonized) | CC BY 4.0 | Yes - fully open |
| awesome-biomarkers | CC0 (public domain) | Yes - no restrictions |
| MarkerDB 2.0 | CC BY-NC 4.0 | Requires permission from Wishart Lab |
| LOINC | Free with account | Yes - with attribution |
| HMDB | Free access | Check terms for redistribution |
| ABIM/Medscape/Wikipedia | Various | Reference only, do not redistribute |

---

## Recommended Approach for BodyCypher

### For MVP (now)
**Manual compilation from clinical sources.** Pull reference ranges for your 50-80 target biomarkers from ABIM, Medscape, and Geeky Medics into a spreadsheet. ~4-6 hours of work. Have your doctor co-founder review and adjust for Thai lab standards. This gets you a working reference range table immediately.

### For differentiation (later)
**NHANES optimal ranges.** Once the MVP is validated, invest in computing "optimal" ranges from NHANES data. This creates a proprietary dataset that competitors (LabSmarts, OptimalDX) charge subscription fees for. Requires Python/R skills and ~1-2 weeks of focused work. Alternatively, find whether someone has already published computed ranges (see deep research prompt).

### For enrichment (ongoing)
**Biomarker descriptions from awesome-biomarkers + HMDB.** Use these to populate the per-marker education content in [[decypher|the app]] ("click any marker to learn what it means").

---

## Sources

1. Nguyen et al. - Cleaned NHANES 1988-2018 (Figshare dataset): https://figshare.com/articles/dataset/NHANES_1988-2018/21743372
2. CDC NHANES Laboratory Data (raw files): https://wwwn.cdc.gov/nchs/nhanes/search/datapage.aspx?Component=Laboratory
3. poldrack/nhanes Python package (GitHub): https://github.com/poldrack/nhanes
4. CRAN NHANES R package: https://github.com/cran/NHANES
5. Mirador NHANES scripts (GitHub): https://github.com/mirador/nhanes
6. Nguyen et al. (2023) medRxiv preprint: https://doi.org/10.1101/2023.02.06.23284573
7. MarkerDB 2.0 (web interface): https://markerdb.ca
8. MarkerDB downloads page: https://old.markerdb.ca/downloads
9. Jackson et al. (2025) MarkerDB 2.0 paper (Nucleic Acids Research): https://academic.oup.com/nar/article/53/D1/D1415/7899528
10. awesome-biomarkers GitHub repository: https://github.com/markwk/awesome-biomarkers
11. BiomarkerDB Google Sheet (community): https://docs.google.com/spreadsheets/d/1WVhjSNUQh4xuc41cLuChE-DthZzEemHxeHghbCdQ2sA/edit
12. Biomarker Tracker template (Google Sheet): https://docs.google.com/spreadsheets/d/1gpESrmjD6TpOIlYB0-tu9uZk2fRaHkgFAsMPK9mzMKQ/edit
13. ABIM Laboratory Test Reference Ranges (January 2025): https://www.abim.org/Media/bfijryql/laboratory-reference-ranges.pdf
14. Medscape Lab Values - Normal Adult Reference Ranges: https://emedicine.medscape.com/article/2172316-overview
15. Wikipedia - Reference ranges for blood tests: https://en.wikipedia.org/wiki/Reference_ranges_for_blood_tests
16. Geeky Medics - Reference Ranges: https://geekymedics.com/reference-ranges/
17. ACCP/PSAP Lab Values Table: https://www.accp.com/docs/sap/Lab_Values_Table_PSAP.pdf
18. Monash Health Pathology Reference Interval Master List: https://monashpathology.org/wp-content/uploads/2024/08/WIN-QS-19.pdf
19. LOINC (Logical Observation Identifiers Names and Codes) downloads: https://loinc.org/downloads/
20. HMDB (Human Metabolome Database): https://hmdb.ca
21. BIONDA biomarker database: http://bionda.mpc.ruhr-uni-bochum.de
22. Biomarker Data Repository (BmDR) by C-Path: https://c-path.org/program/biomarker-data-repository/
23. Patel et al. (2016) NHANES exposome database (Nature Scientific Data): https://www.nature.com/articles/sdata201696
24. CDC NHANES main page: https://wwwn.cdc.gov/nchs/nhanes/
25. Mark Koester - Biomarkers blog post (awesome-biomarkers context): https://www.markwk.com/biomarkers.html
26. MarkerDB 1.0 paper - Wishart et al. (2021, Nucleic Acids Research): https://academic.oup.com/nar/article/49/D1/D1259/6007662
27. NBME Laboratory Reference Values: https://www.nbme.org/sites/default/files/2025-03/NBME_Laboratory_Reference_Values.pdf
28. Optimal Health - How to Interpret Blood Test Results guide: https://optimalhealth.co/resources/blood-testing/interpreting-results
29. Hone Health - Reference Ranges Optimal vs Normal: https://honehealth.com/edge/optimal-vs-normal/

---

*Document created: February 2026*

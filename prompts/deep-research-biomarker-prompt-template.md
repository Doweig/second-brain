---
type: product-research
date: 2026-02-01
source: manual
tags: [biomarkers, prompt-template, deep-research]
people: []
companies: [bodycypher]
status: raw
---

# Deep Research Prompt Template — Biomarker Range Research

> **Usage:** Copy the prompt below and replace `[BIOMARKER]` with the specific biomarker name (e.g., "LDL Cholesterol", "Fasting Insulin", "Vitamin D (25-hydroxyvitamin D)", "HbA1c", etc.). Submit to deep research.

---

## Prompt

```
Research the biomarker [BIOMARKER] comprehensively. I need two outputs: (1) structured data for a health product, and (2) educational content for a blog article. Both must be evidence-based with cited sources.

## OUTPUT 1: Structured Range Data

Find and recommend the following ranges. Where sex-specific ranges are clinically warranted, provide separate values for males and females. Otherwise, provide a single universal range.

**Standard Reference Range** — The conventional clinical reference range used by major laboratories (Quest, LabCorp, or equivalent). This is the range printed on a standard lab report. Provide the low and high bounds.

**Optimal Range** — A tighter range within the standard reference range associated with the lowest disease risk and best health outcomes based on current evidence. This is NOT the standard lab range — it should be narrower and reflect what longevity medicine, large epidemiological studies, or clinical guidelines recommend as ideal. Provide the low and high bounds.

For each range, specify:
- The exact numeric low and high values
- The unit of measurement
- Whether it is sex-specific (and if so, provide male and female values separately)
- Whether fasting is required for accurate measurement
- The primary source or guideline the range is derived from

Format the range data as a structured table.

## OUTPUT 2: Educational Blog Content

Write a comprehensive, evidence-based article about [BIOMARKER] suitable for a health-conscious general audience. The article should be written so that someone Googling "[BIOMARKER] optimal range", "[BIOMARKER] normal range", "what is [BIOMARKER]", or "[BIOMARKER] blood test" would find it useful and authoritative.

The article must cover ALL of the following sections:

### What is [BIOMARKER]?
Explain what this biomarker measures, what organ or system produces it, and why doctors order this test. Use plain language but be scientifically accurate. Include the full medical name and any common abbreviations.

### Why does [BIOMARKER] matter for your health?
Explain what this biomarker tells you about your health. What conditions or risks are associated with levels that are too high or too low? Why should someone care about this number even if they feel fine?

### Standard reference range vs. optimal range
Explain the difference between the standard lab reference range and the optimal range. Present both ranges with their numeric values. Explain WHY the optimal range is tighter than the standard range — what evidence supports it? Reference specific studies, guidelines, or clinical data.

### What does the research say?
Summarize the most important and recent research findings about this biomarker. This should include:
- Any large epidemiological studies linking levels to mortality or disease outcomes (cite study name, year, journal, sample size)
- Any relevant clinical guidelines from major medical societies (AHA, ACC, ADA, ESC, Endocrine Society, etc.)
- Any U-shaped or J-shaped dose-response curves if they exist (what level is associated with lowest risk?)
- Any debate or controversy in the scientific community about optimal levels
- Findings from longevity medicine practitioners if relevant (Peter Attia, Bryan Johnson's Blueprint, etc.)

### What factors affect [BIOMARKER] levels?
List the key factors that can raise or lower this biomarker: diet, exercise, sleep, stress, medications, supplements, genetics, age, sex, and any other relevant factors.

### How to improve your [BIOMARKER] levels
Provide actionable, evidence-based recommendations for someone whose levels are outside the optimal range. Separate into lifestyle interventions (diet, exercise, sleep) and supplementation if applicable. Note when medical consultation is warranted.

## RESEARCH REQUIREMENTS

- Cite all claims with specific sources (author, year, journal, DOI or URL when available)
- Prioritize peer-reviewed research, major clinical guidelines, and large cohort studies
- Include sample sizes for epidemiological studies when available
- Note when evidence is from RCTs vs. observational studies
- If there is scientific debate or conflicting guidelines, present both sides
- Use the most recent available data and guidelines
- Do not fabricate or hallucinate citations — only cite sources you can verify

## FORMAT REQUIREMENTS

- Use markdown formatting with clear headers
- Present range data in a clean table
- Include a numbered reference list at the end with full citations
- Write in clear, accessible English (will be translated to Thai)
- Target word count: 2,000–3,000 words for the blog content
- Tone: authoritative but accessible, like a knowledgeable doctor explaining to a smart patient
```

---

## Example Usage

Replace `[BIOMARKER]` with any of these:

| Biomarker | Search Term to Use |
|-----------|-------------------|
| LDL Cholesterol | LDL Cholesterol (LDL-C) |
| HDL Cholesterol | HDL Cholesterol (HDL-C) |
| Triglycerides | Triglycerides |
| Total Cholesterol | Total Cholesterol |
| ApoB | Apolipoprotein B (ApoB) |
| Lp(a) | Lipoprotein(a) — Lp(a) |
| hsCRP | High-Sensitivity C-Reactive Protein (hsCRP) |
| HbA1c | Hemoglobin A1c (HbA1c) |
| Fasting Glucose | Fasting Blood Glucose |
| Fasting Insulin | Fasting Insulin |
| HOMA-IR | HOMA-IR (Homeostatic Model Assessment for Insulin Resistance) |
| Homocysteine | Homocysteine |
| Vitamin D | Vitamin D (25-Hydroxyvitamin D) |
| TSH | Thyroid Stimulating Hormone (TSH) |
| Free T3 | Free Triiodothyronine (Free T3) |
| Free T4 | Free Thyroxine (Free T4) |
| Ferritin | Ferritin |
| Iron | Serum Iron |
| TIBC | Total Iron-Binding Capacity (TIBC) |
| Testosterone | Total Testosterone |
| Free Testosterone | Free Testosterone |
| SHBG | Sex Hormone-Binding Globulin (SHBG) |
| ALT | Alanine Aminotransferase (ALT) |
| AST | Aspartate Aminotransferase (AST) |
| GGT | Gamma-Glutamyl Transferase (GGT) |
| Uric Acid | Uric Acid |
| BUN | Blood Urea Nitrogen (BUN) |
| Creatinine | Creatinine |
| eGFR | Estimated Glomerular Filtration Rate (eGFR) |
| Albumin | Albumin |
| Total Protein | Total Protein |
| Globulin | Globulin |
| Bilirubin | Total Bilirubin |
| Alkaline Phosphatase | Alkaline Phosphatase (ALP) |
| WBC | White Blood Cell Count (WBC) |
| RBC | Red Blood Cell Count (RBC) |
| Hemoglobin | Hemoglobin |
| Hematocrit | Hematocrit |
| MCV | Mean Corpuscular Volume (MCV) |
| RDW | Red Cell Distribution Width (RDW) |
| Platelets | Platelet Count |
| Sodium | Sodium (Na) |
| Potassium | Potassium (K) |
| Chloride | Chloride (Cl) |
| CO2 | Carbon Dioxide (CO2 / Bicarbonate) |
| Calcium | Calcium |
| Magnesium | Magnesium |
| Phosphorus | Phosphorus |

## Notes

- For Tier 3 biomarkers (CBC, electrolytes) where no strong evidence-based optimal range exists, the research will likely return standard ranges only. That's fine — the prompt asks the AI to note when evidence is limited.
- The structured data table from Output 1 can be directly imported into your biomarker database.
- The blog content from Output 2 can be published as-is after translation, or split into multiple shorter articles per biomarker.
- Run this once per biomarker. For ~49 biomarkers, that's ~49 deep research sessions.

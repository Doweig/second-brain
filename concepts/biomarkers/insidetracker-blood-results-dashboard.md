---
type: product-research
date: 2026-03-01
source: manual
tags: [competitor, mystery-shopping, dashboard, blood-testing]
people: []
companies: [bodycypher]
status: raw
---

# InsideTracker — Blood results dashboard (screenshot)

- Source: InsideTracker web app dashboard ("Blood results")
- Evidence type: full-page screenshot
- Captured: 2026-03-03
- Asset: `assets/insidetracker-blood-results-dashboard.jpg`
- SHA256-12: 95c87e7fc272

## What’s visible (UI/UX + feature extraction)

### Page-level structure
- Page title: **Blood results**
- Above-the-fold controls: dropdown filters and at least one prominent green action button (labels not legible at this resolution).

### Repeating result cards (domain-level grouping)
The page is composed of many vertically stacked cards, each representing a health domain/category. Each card uses a consistent 3-column layout:

1) **Left column — score + trend**
- Large **circular gauge/dial** with a single-word status (appears often as “Good”, but not reliably readable everywhere).
- Small **trend/history mini-chart** below the gauge.
- Dark-green CTA chip/button near the bottom of the left column (text too small to transcribe).

2) **Center column — interpretation + education/action**
- Short paragraph explaining the domain status.
- One or more green CTA buttons (e.g., “learn more / recommendations” style; exact labels not readable).

3) **Right column — biomarker table/list**
- A vertical list of biomarker rows, each with:
  - biomarker name (left),
  - numeric value + unit (middle/right),
  - reference/target range (small text),
  - colored status pill (green/yellow/orange/red) indicating in-range vs out-of-range.

### Visual design system
- Status colors map across gauges, left-side card border accents, and biomarker status pills.
- Consistent card scaffolding suggests a template-based report system.

## Data extraction status

### What is readable now
- “Blood results” title.
- High-level layout and recurring elements (gauge, trend chart, biomarker list with range + status pill).

### What is NOT readable (needs higher-res crops)
- Most biomarker names.
- Nearly all numeric values, units, and reference ranges.
- Card titles / domain names and CTA button labels.

## Next step (to complete competitor data capture)
Upload **higher-resolution crops** of the biomarker list area (right column) per card (or export/download report if available). Then we can transcribe:
- biomarker name
- value
- units
- reference range
- flag/status label


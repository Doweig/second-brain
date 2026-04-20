---
stepsCompleted: [1, 2, 3, 4, 5, 6]
status: complete
inputDocuments:
  - '_bmad-output/brainstorming/brainstorming-session-2026-01-28.md'
date: 2026-01-28
author: Doweig
people:
  - guillaume-doweig
companies:
  - bodycypher
tags:
  - product-brief
  - mvp
  - validation
---

# Product Brief: BodyCypher

## Executive Summary

A health optimization platform for health-conscious individuals who want more than "you're not sick" from their checkups. We deliver comprehensive blood panels focused on performance markers (including hormones), paired with structured, referable action plans accessible via a mobile app.

**The gap we fill:** Premium clinics provide good doctors but oral-only advice that's forgotten in weeks. Hospital checkups are affordable but skip critical markers. ChatGPT can interpret results but lacks structure and consistency. We combine lab-direct pricing with expertly structured AI interpretation and doctor oversight.

**Target market:** Health-conscious English speakers in Thailand - expats pursuing optimization and affluent Thai professionals who want control over their health, not just reassurance.

---

## Core Vision

### Problem Statement

Health-conscious individuals in Thailand face a frustrating tradeoff: affordable hospital checkups that skip performance markers (especially hormones) and deliver generic results, or premium clinics charging 30-40k baht for comprehensive panels with insights delivered orally and forgotten within weeks.

The problem isn't the quality of doctors - it's the format. An hour of expert advice becomes scattered memories: "something about creatinine... drink more water?" There's no persistent reference, no structured action plan, no way to slowly digest complex health information over time.

### Problem Impact

- Valuable insights lost to memory decay within 1-2 weeks
- PDF reports accumulate unused ("dead data")
- Multiple doctor opinions create confusion rather than clarity
- Health-conscious people feel frustrated, not empowered
- The gap between "knowing" and "doing" remains unbridged
- People resort to ChatGPT uploads but get inconsistent, unstructured output

### Why Existing Solutions Fall Short

| Solution | What's Good | What's Missing |
|----------|-------------|----------------|
| Hospital checkups | Affordable, accessible | Skip performance markers, minimal interpretation |
| Premium clinics | Good doctors, comprehensive | Overpriced, oral-only advice, no action plan |
| ChatGPT + PDF upload | Quick second opinion | Unstructured, inconsistent, no marker depth |
| DIY interpretation | Free | Requires expertise, time, patience |

### Proposed Solution

A mobile app delivering:

1. **Comprehensive blood panels** - Performance-focused markers including full hormones, at lab-direct pricing
2. **Structured action plans** - Executive summary, dietary guidance, supplement recommendations - referable and digestible over time
3. **Per-marker education** - Click any marker to understand what it means, why it matters, and how to improve it
4. **Historical context** - Ingest old PDFs to track trends (with clear expectation-setting on limited markers)

Doctor oversight ensures V1 quality - not just interpretation, but structuring the experience based on real patient questions and needs.

### Key Differentiators

- **Control the input, control the output** - Comprehensive panels we design, not garbage-in-garbage-out from random PDFs
- **Written > oral** - Action plans you can reference weekly, not advice you forget
- **Premium quality, lab-direct pricing** - Cut out the clinic markup
- **Structured AI + doctor review** - Better than DIY ChatGPT prompts
- **First mover in Thailand** - Data lock-in and switching costs create defensibility over time

---

## Target Users

### Primary User Hypothesis

**"The Optimizer"** - Health-conscious individual, 30-55, who wants more than "you're not sick"

**What we know:**
- Pursues health optimization, not just disease prevention
- Frustrated by oral-only advice and forgotten recommendations
- Willing to pay for comprehensive panels but feels current premium options are overpriced
- English-speaking (expat or affluent Thai professional)
- Likely triggered by: aging, health scare, or performance goals

**What we need to validate:**
- Current checkup frequency and spend
- Primary motivation (longevity vs performance vs specific concern)
- App usage patterns and preferences
- Price sensitivity thresholds

**Founder as User:** The founder fits this profile exactly - this is a dogfooding product with strong founder-market fit.

### Secondary User Hypotheses (to explore)

| Segment | Hypothesis | Validation Needed |
|---------|------------|-------------------|
| Athletes | Performance optimization, hormone focus | Do they already track biomarkers? |
| Doctors | Professional credibility, detailed data | Would they use for themselves? Refer patients? |
| Biohackers | Data-obsessed, want raw numbers + trends | Overlap with optimizer or distinct? |

### User Journey (V1 Hypothesis)

1. **Discovery** - Word of mouth from trust ladder (friends → friends of friends)
2. **Onboarding** - Book blood draw, complete intake questionnaire
3. **Core moment** - Receive structured action plan in app
4. **Aha moment** - "This is what my doctor told me, but written down and actionable"
5. **Retention** - Return weekly to reference plan, track progress over time
6. **Expansion** - Retest in 3-6 months, see trends, share with friends

*Note: Personas are hypotheses. Update after each trust ladder round with real user feedback.*

---

## Success Metrics

### User Success Metrics

**Core Value Delivered:** Clarity and feeling of control over health

| Metric | What It Measures | How We Know It's Working |
|--------|------------------|--------------------------|
| Action plan engagement | Users reference their plan | Weekly app opens, return visits |
| Recommendation follow-through | Users act on advice | Self-reported or tracked behavior changes |
| Retest rate | Users want ongoing optimization | Prepaid or booked follow-up tests |
| Referral behavior | Users see enough value to share | Organic word-of-mouth, friend invites |

**User "Aha" Moment:** "This is what my doctor told me, but written down and I can actually follow it."

### Business Objectives

**Stage-Gated Validation Model:**

| Stage | Target | Success Signal | Pivot Signal |
|-------|--------|----------------|--------------|
| Round 0 | Self | Output quality good enough to share | Embarrassed to show friends |
| Round 1 | 5-10 friends | Someone pays for something (supplements, prepaid retest) | Nobody willing to pay |
| Round 2 | Friends of friends | Honest feedback, referrals happen organically | Only polite feedback, no referrals |
| Round 3 | Strangers | Marketing converts without founder selling | Only works face-to-face |
| **Real Business** | 100 paying customers | System works independent of founder | — |

**Payment = Truth:** Revenue doesn't matter early. Payment validates that the product solves a real problem worth paying for. Upsell vectors to test:
- Supplement delivery ("you need this, we'll ship it")
- Prepaid next test at discount ("20% off if you book now")

### Key Performance Indicators

**V1 KPIs (Trust Ladder Phase):**

| KPI | Target | Measurement |
|-----|--------|-------------|
| Round 1 completion | 5-10 users served | Count of completed action plans delivered |
| Payment conversion | ≥1 paid transaction | Any upsell or prepaid purchase |
| Qualitative signal | "Worth it" feedback | Post-delivery interview or survey |
| Referral intent | Willing to refer | "Would you recommend this to a friend?" |

**Milestone KPI:**
- **100 paying customers** = real business, celebration-worthy, system works at scale

*Note: Metrics focus on validation, not revenue. Selling at cost is fine - payment proves value.*

---

## MVP Scope

### Prototype vs MVP Distinction

This product has two distinct phases before "real business":

| Phase | Prototype (Round 1) | MVP (Round 2) |
|-------|---------------------|---------------|
| **Goal** | Validate output quality, get first payment signal | Validate with non-friends, prove system works |
| **Audience** | 5-10 friends | Friends of friends, early strangers |
| **Delivery** | PDF reports | Mobile app |
| **Success gate** | Someone pays for something | Marketing converts without founder selling |

### Core Features (Both Phases)

**Blood Test + Action Plan Pipeline:**
1. Comprehensive blood panel (founder-defined markers, including hormones)
2. Intake questionnaire (context for personalization)
3. AI-generated action plan - multi-section format:
   - Executive summary
   - Dietary recommendations
   - Supplement recommendations
   - (Additional sections as validated)
4. Doctor validation of AI output
5. Doctor's Notes page (handwritten, no AI - personalized human touch)

**Data-Driven Design:**
- One prompt = one section (modular)
- Track which sections users view, time spent, return frequency
- Iterate based on actual usage, not assumptions

### MVP-Specific Features (Round 2)

- Mobile app delivery
- Usage analytics (which sections matter?)
- Basic user accounts

### Out of Scope (Prototype & MVP)

| Feature | Rationale |
|---------|-----------|
| Per-marker education (click to learn) | Wait for users to ask |
| Old PDF ingestion | Nice-to-have, not core value |
| Trend tracking across tests | Post-MVP, when users retest |
| Supplement commerce | Upsell test only, not core product |
| Social/referral features | Organic word-of-mouth first |

### MVP Success Criteria

**Prototype → MVP Gate:**
- 5-10 friends served with PDF reports
- At least one payment (supplements or prepaid retest)
- Qualitative "worth it" feedback

**MVP → Scale Gate:**
- Friends-of-friends convert without founder selling face-to-face
- Users engage with app (return visits, section views)
- Payment conversion continues

### Future Vision (Intentionally Flexible)

**After 100 paying customers:**
- Increase LTV: successful upsells, longer retention
- Establish marketing pipelines that work without founder
- Evaluate expansion: Thai language (deeper market), Southeast Asia

**Features to evaluate based on data:**
- Trend tracking (when users retest)
- Per-marker education (if users request)
- Subscription model
- Additional markets

*Note: Future scope intentionally vague. Learn from Rounds 1-2 before committing to roadmap.*

---
type: meeting-notes
date: 2026-03-10
source: transcript
tags: [dr-c, operations, ai-action-plan, prompt-engineering, n8n, pricing, compensation, merger, aspire, clinic, prewell]
people: [art-chawapon-kidhirunkul, guillaume-verbal, dan-aspire, nick-warot]
companies: [bodycypher, aspire-coaching-physio, prewell-clinic, bnh-hospital]
status: reviewed
---

# Meeting with Dr. C — 2026-03-10

## Action Items

- [ ] Guillaume: Set up N8n and provide access to [[art-chawapon-kidhirunkul|Dr. C]]
- [ ] Dr. C: Share email address for N8n registration
- [ ] Dr. C: Generate usual AI-powered blood test report using current workflow and send to Guillaume (baseline comparison)
- [ ] Guillaume: Send personal blood test results to Dr. C for sample analysis
- [ ] Dr. C: Check with team about number of available part-time nurses
- [ ] Guillaume: Finalize starting arrangements and confirm Tuesday work schedule
- [ ] Guillaume: Continue merger negotiations with [[dan-aspire|Dan]]'s company ([[aspire-coaching-physio|Aspire]])
- [ ] Guillaume: Send urine organic acid test information to Dr. C

## Blood Test Process & Workflow (Agreed)

1. Guillaume qualifies customer via initial call
2. Customer pays ฿10,000
3. Nurse booked through [[prewell-clinic|Prewell]] clinic (P-R-E-W-E-L-L)
4. Nurse collects blood at customer location, brings to clinic, sends to N Health
5. Customer uploads results to system → triggers AI action plan generation
6. Optional "Request Doctor Review" button → Dr. C reviews and adds notes
7. Video consultation with Dr. C

**Pricing breakdown per patient:**
- Customer pays: ฿10,000
- Guillaume covers: N Health lab costs (variable, e.g. ฿7,000 if package is ฿17,000) + ฿1,000 nurse fee + ฿2,000 operational costs

**Nurses:** 2-3 part-time nurses available through Prewell, flexible any day of the week.

## AI Action Plan Development

**Current state:** Dr. C uses single-prompt approach — "as a functional medicine doctor, review the result, conclude key issues, give action plan including lifestyle + supplements."

**Agreed approach — prompt chaining:**
1. Data preparation (extract from PDF, organize, add flag columns: okay/high/low/optimal high/optimal low)
2. Find conditions
3. Dietary plan
4. Supplements
5. Final summary

**Key decisions:**
- Each prompt does ONE thing only → enables A/B testing per step
- N8n for automated prompt chaining (not manual Claude/ChatGPT copy-paste)
- Claude preferred over ChatGPT (will be used in production)
- Blood panel categories based on InsideTracker model, needs expansion: gut health, brain health, cognitive function
- Doctor's notes shown verbatim — broken English preferred for authenticity ("looks like a real doctor, not AI")

**Baseline test:** Dr. C will analyze Guillaume's blood results using her current workflow → provides comparison point for the automated pipeline.

## Dr. C's Schedule

| Day | Commitment |
|-----|-----------|
| Monday | [[bnh-hospital|BNH]] (whole day) |
| Tuesday | **Free — proposed for [[bodycypher|BodyCypher]] work** |
| Wednesday | BNH |
| Thursday | Rotating: 2 days/month Thai Nakharin Hospital (Bangna), 1 day/month Lifespan Clinic, 1 free Thursday/month |
| Friday | Morning: charity/public health center (Watthathong). Afternoon: BNH |
| Saturday | Off |
| Sunday | BNH morning, afternoon free |

Schedule is flexible — can adjust and take leave from BNH as needed.

## Compensation & Partnership (Agreed Start)

- **Starting:** 1 day/week (Tuesday) for ฿50,000/month
- **Scale path:** 2 days/week = ฿100K/month (comparable to BNH rate: 3 days/week = ฿150K)
- **Equity:** Dr. C will receive salary + shares in technology company (negotiation pending)
- **Investment:** Dr. C not investing capital at this time (has other financial plans)
- **Start date:** Next Tuesday

**Two-entity structure discussed:**
- Technology company (where shares are held, where value accrues)
- Clinic operations (outsourced service model — Prewell, potentially multiple clinics)
- Guillaume wants to keep maximum capital in tech company, clinic relationship is outsourcing

## Dr. C's Responsibilities

- AI action plan development and prompt engineering
- Medical oversight and report review
- Blood panel design and lab relationship management
- Video consultations (free days or after 5pm on working days)
- Content creation / podcast appearances (Thai language focus)

## Aspire Merger Discussion

- **Company:** Aspire Coaching/Physio, Asoke area (near Interchange)
- **Team:** Dan (52, Australian, charismatic personal trainer) + Ukrainian software engineer partner
- **Assets:** Gym, physio clinic, opening medical clinic — taking over entire building
- **Their blood panel:** Basic ฿3,000 panel with ~40 markers (inadequate)
- **Status:** Early negotiations, Guillaume pushing for CEO position
- **Guillaume's concern:** Dan doing too many things, focus risk
- **Funding:** ฿3M available this year across entities

## Dr. Nick Discussion

- Smart and sharp but less experienced/opinionated than Dr. C
- Has full-time job (can't do public-facing content)
- Planning to move back to hometown (has job offer there)
- Risk: full-time-or-nothing situation, risky for him to join early-stage
- Decision deferred — Dr. C can recruit additional doctors as needed later

## Additional Medical Discussion

- Guillaume disclosed Asperger's to Dr. C
- Dr. C recommended urine organic acid test (~฿18,000) for metabolic/gut health assessment
- Focus areas: mitochondrial function, gut dysbiosis, neurotransmitter balance
- Gut-brain axis connection — fungal infections (mycotoxin) can prevent neurological recovery
- Dr. C has seen improvement in autism-spectrum patients through gut health optimization

## Tools & Communication

- LINE translation bot (Papago) added to group chat for Thai-English communication
- Security note: no medical documents in translated group chat (third-party recording risk)
- N8n for prompt chaining automation (Guillaume to set up)

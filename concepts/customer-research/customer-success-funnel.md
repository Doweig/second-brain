---
type: growth
date: 2026-02-01
source: manual
tags: [customer-success, funnel, supplements]
people: []
companies: [bodycypher]
status: raw
---

# BodyCypher Customer Success Funnel

*Documented from whiteboard session — January 2026*

---

## Overview

The Customer Success funnel begins after payment. It's the journey from "just paid" to "taking personalized supplements based on blood test results."

```
PAYMENT → REGISTER → BOOK → REMINDERS → CLINIC → BLOOD TEST → RESULTS (2-3D) → DOCTOR NOTE → ACTION PLANS → SUPPLEMENTS ($$$)
```

---

## Handoff: Sales → Customer Success

When someone pays on the sales page:
1. Payment confirmed via Stripe
2. Account created in database
3. Welcome email triggered
4. User enters registration flow

---

## Stage 1: Registration

**Goal:** Complete user profile, capture consent

### Flow

```
SIGN LINK (email) 
     ↓
  REGISTER
     ↓
 App / Web Interface
     ↓
 Complete Profile
     ↓
 CONSENT FORM ✓
```

### Registration Steps

1. **Sign Link**
   - Sent via email after payment
   - Deep link to app or web registration

2. **Account Setup**
   - Confirm email
   - Set password (or magic link)
   - Download app (if mobile-first)

3. **Complete Profile**
   - Personal details
   - Health history
   - Current supplements
   - Goals

4. **Consent Form**
   - Medical consent
   - Data privacy (PDPA)
   - Terms of service
   - Checkbox confirmations

### Database ($DB)

At this point, we have:
- User account
- Payment confirmed
- Profile data
- Consents captured

---

## Stage 2: Booking

**Goal:** Schedule blood test appointment

### Booking Interface

```
┌─────────────────────────────┐
│     NURSE SCHEDULING        │
├─────────────────────────────┤
│  Select Date:               │
│  [1] [2] [3] [4]           │
│         📅                  │
├─────────────────────────────┤
│  Select Time:               │
│  9:00  2:00  10:00         │
├─────────────────────────────┤
│  [DD/DA] Date confirmation  │
└─────────────────────────────┘
```

### Booking Options

| Option | Description |
|--------|-------------|
| Clinic Visit | Go to partner lab location |
| Home Collection | Nurse comes to you (if available) |

### Booking Flow

1. **Choose type:** Clinic or Home
2. **Select date:** Calendar with available slots
3. **Select time:** Morning recommended (fasting)
4. **Confirm location:** Address for home or clinic details
5. **Confirmation:** Email + SMS/LINE with details

### Clinic Information

When user selects clinic:
- Provide clinic INFO (address, parking, etc.)
- WALK IN option (if supported)
- CONFIRM FROM CLINIC (lab confirms appointment)

---

## Stage 3: Pre-Appointment

**Goal:** Ensure user shows up prepared (fasted)

### Reminder Sequence

```
REMINDERS
    ↓
  FASTED ✓
```

### Reminder Timeline

| When | Channel | Content |
|------|---------|---------|
| 3 days before | Email | Appointment confirmed, prep instructions |
| 1 day before | Email + LINE | Reminder, fasting instructions |
| Morning of | SMS/LINE | "Your appointment is today at X" |
| 2 hours before | Push/SMS | Final reminder, directions |

### Fasting Instructions

**Must communicate clearly:**
- 8-12 hour fast required
- Water is OK
- No coffee/tea with sugar
- No alcohol 24 hours before
- Time test appropriately (morning ideal)

### "What's Gonna Happen" 😊

**Pre-appointment education:**
- What to expect at the clinic
- How long it takes (15-30 min)
- What tests are being done
- When to expect results

---

## Stage 4: Clinic Visit / Blood Draw

**Goal:** Smooth blood collection experience

### At the Clinic

```
CLINIC
   ↓
 Check-in
   ↓
 Blood Draw 🩸🩸🩸
   ↓
 Done!
```

### Blood Draw

- Multiple vials collected (as shown on whiteboard)
- Based on test panel selected
- Nurse/phlebotomist handles draw
- Results sent to lab for processing

### Post-Visit Communication

- Immediate: "Thanks for completing your test!"
- Set expectation: "Results in 2-3 days"

---

## Stage 5: Results Processing

**Goal:** Process results, prepare for delivery

### Timeline

```
BLOOD DRAW → 2D AFTER → 3D → RESULTS READY
```

| Day | Activity |
|-----|----------|
| Day 0 | Blood draw completed |
| Day 1 | Lab processing |
| Day 2 | Results available from lab |
| Day 3 | AI analysis + Doctor review |
| Day 3+ | Results delivered to user |

### Processing Steps

1. **Lab returns results** (electronic transfer)
2. **AI generates interpretation**
   - Flags abnormalities
   - Drafts recommendations
   - Identifies supplement opportunities
3. **Doctor review** (DOCTOR NOTE 📄)
   - Reviews AI output
   - Approves or modifies
   - Signs off on recommendations

---

## Stage 6: Results Delivery

**Goal:** Deliver clear, actionable results

### Doctor Note

```
📄 DOCTOR NOTE
     ↓
 AI-generated interpretation
 Clinician-approved
 Personalized to user
```

### Results Package

1. **Summary View**
   - Overall health score/status
   - Key findings
   - Priority areas

2. **Detailed Results**
   - Each biomarker with:
     - Your value vs optimal range
     - Simple explanation
     - Status indicator

3. **Doctor's Note**
   - Personalized message
   - Key takeaways
   - Concerns to address

---

## Stage 7: Action Plans

**Goal:** Translate results into action, drive supplement conversion

### Action Plans Structure

```
ACTION PLANS
    ↓
💊 💊 💊 💊
Supplement recommendations
```

### Action Plan Categories

| Category | Examples |
|----------|----------|
| Dietary | Foods to add/avoid |
| Supplements | Personalized stack |
| Lifestyle | Sleep, exercise, stress |
| Follow-up | What to retest, when |

### Supplement Recommendations

**This is the key monetization moment.**

For each deficiency/opportunity:
- Specific supplement recommendation
- Dosage guidance
- Why it helps (connected to their result)
- Option to add to subscription

### The Pitch

```
"Based on your results, here's your personalized supplement stack:"

→ Vitamin D (your level: 25 ng/mL, optimal: 50+)
→ Omega-3 (inflammation markers elevated)
→ Magnesium (supports 300+ bodily processes)

[Subscribe for THB X/month]
```

---

## Stage 8: Supplement Subscription

**Goal:** Convert to recurring supplement revenue

### Subscription Flow

```
ACTION PLANS → SUBSCRIBE → $$$ → RECURRING
```

### Subscription Tiers

| Tier | Monthly Price | Includes |
|------|---------------|----------|
| Essential | ฿1,500 | Core vitamins (D, B12, etc.) |
| Optimized | ฿3,000 | Essential + performance stack |
| Premium | ฿5,000 | Full personalized protocol |

### Subscription Features

- Monthly delivery
- Adjust based on next test
- Pause/cancel anytime
- Track progress in app

---

## Communication Touchpoints Summary

| Stage | Email | SMS/LINE | Push | In-App |
|-------|-------|----------|------|--------|
| Registration | ✓ Welcome | | | ✓ |
| Booking confirmation | ✓ | ✓ | | ✓ |
| 3 days before | ✓ Prep | | | |
| 1 day before | ✓ | ✓ | | |
| Morning of | | ✓ | ✓ | |
| Post-visit | ✓ Thanks | | | |
| Results ready | ✓ | ✓ | ✓ | ✓ |
| Action plans | ✓ | | | ✓ |
| Supplement offer | ✓ | | | ✓ |

---

## Key Metrics

| Stage | Metric | Target |
|-------|--------|--------|
| Registration | Completion rate | 95%+ |
| Booking | Book within 7 days | 80%+ |
| Appointment | Show-up rate | 90%+ |
| Results | Viewed within 24h | 85%+ |
| Action Plans | Engagement rate | 70%+ |
| Supplements | Conversion rate | 40%+ |
| Subscription | 3-month retention | 70%+ |

---

## Tech Requirements

| Component | Need |
|-----------|------|
| Registration | User auth, profile forms, consent capture |
| Booking | Calendar system, clinic integration |
| Reminders | Email + SMS/LINE automation |
| Results | PDF/data from lab, AI processing |
| Action Plans | Recommendation engine |
| Subscriptions | Stripe recurring, inventory management |
| Notifications | Multi-channel (email, SMS, push, LINE) |

---

## Open Questions

1. **Registration:** App-first or web-first?
2. **Booking:** Build own calendar or use Calendly/similar?
3. **Reminders:** What channels for Thai market? (LINE crucial)
4. **Lab integration:** API or manual upload?
5. **Doctor review:** How many users can one doctor handle/day?
6. **Supplement fulfillment:** Partner or build own?
7. **Timing:** When to pitch supplements relative to results?

---

## Next Steps

1. [ ] Map registration flow in detail
2. [ ] Design booking interface
3. [ ] Write reminder email/SMS templates
4. [ ] Define AI interpretation workflow
5. [ ] Draft action plan templates
6. [ ] Design supplement subscription page
7. [ ] Set up notification infrastructure

---

*Last updated: January 2026*
*Source: Whiteboard session with email marketing specialist*

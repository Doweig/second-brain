---
type: growth
date: 2026-02-01
source: manual
tags:
  - user-lifecycle
  - sales-funnel
  - customer-success
people: []
companies:
  - bodycypher
status: raw
---

# BodyCypher User Lifecycle

*Documented from whiteboard session — January 2026*

---

## Overview

The user lifecycle consists of three connected stages, each with its own email/communication strategy:

1. **Landing Page** — First touchpoint, captures interest
2. **Sales Funnel** — Moves prospects from awareness to payment
3. **Customer Success** — Post-payment journey through the product experience

```
ACQUISITION → LANDING PAGE → SURVEY → WELCOME SERIES → SALES PAGE → CSM (Customer Success)
                                                              ↓
                                              REGISTER → BOOKING → CLINIC → RESULTS → ACTION PLANS → SUBSCRIPTION
```

---

## The Two Funnels

### Funnel 1: Sales Funnel
**Goal:** Convert strangers into paying members

**Key stages:**
- Acquisition (traffic sources)
- Landing page (first impression)
- Survey (qualification + email capture)
- Welcome email series (nurture)
- Sales page (conversion)
- Payment (Stripe)

**See:** `bodycypher_sales_funnel.md`

---

### Funnel 2: Customer Success
**Goal:** Deliver value and convert to supplement subscription

**Key stages:**
- Registration (post-payment onboarding)
- Booking (schedule blood test)
- Pre-appointment (reminders, prep instructions)
- Clinic visit (blood draw)
- Results processing (2-3 days)
- Doctor review + action plans
- Supplement recommendations → subscription

**See:** `bodycypher_customer_success_funnel.md`

---

## Handoff Point

The **Sales Funnel** ends and **Customer Success** begins at the moment of payment.

```
SALES PAGE → Stripe Payment → CSM (Customer Success Management begins)
```

At this point:
- User has paid for membership
- System creates their account
- Welcome to product email triggers
- Registration/onboarding flow begins

---

## Email Strategy by Stage

| Stage | Email Type | Goal |
|-------|-----------|------|
| Post-Survey | Thank You | Confirm submission, set expectations |
| Welcome Series | 4-5 emails | Educate, build trust, drive to sales page |
| Post-Payment | Welcome to Product | Celebrate, guide to registration |
| Pre-Appointment | Reminders | Ensure they show up fasted |
| Post-Results | Action Plans | Deliver value, recommend supplements |
| Ongoing | Retention | Tips, community, retest reminders |

---

## Documents to Create

Based on this lifecycle, the following documents should be developed:

1. **Sales Funnel Document** ✅ (see `bodycypher_sales_funnel.md`)
   - Acquisition channels
   - Landing page structure
   - Survey questions
   - Welcome email series
   - Sales page

2. **Customer Success Document** ✅ (see `bodycypher_customer_success_funnel.md`)
   - Registration flow
   - Booking flow
   - Clinic experience
   - Results delivery
   - Supplement conversion

3. **Email Templates** (to create)
   - Welcome series (5 emails)
   - Pre-appointment reminders
   - Results delivery
   - Action plan follow-up

4. **Landing Page Copy** (to create)
   - Hero section
   - Problem/solution
   - CTA

5. **Survey Logic** (to refine)
   - Already have v3 survey
   - May need to add: Last blood test, Price ladder, Supplements Y/N

---

## Key Metrics to Track

### Sales Funnel
- Landing page → Survey start rate
- Survey completion rate
- Survey → Welcome series open rate
- Welcome series → Sales page click rate
- Sales page → Payment conversion rate

### Customer Success
- Registration completion rate
- Booking completion rate
- Show-up rate (booked → completed test)
- Results → Action plan engagement
- Action plan → Supplement subscription conversion
- Supplement subscription retention (30/60/90 day)

---

## Open Questions

1. What's in each of the 5 welcome emails?
2. What's the timing between welcome emails?
3. What happens if someone doesn't convert after welcome series?
4. How do we handle people who don't book after registering?
5. What's the doctor review workflow look like?
6. When do we send the supplement pitch relative to results?

---

*Last updated: January 2026*
*Source: Whiteboard session with email marketing specialist*

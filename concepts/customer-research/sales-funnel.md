---
type: growth
date: 2026-02-01
source: manual
tags:
  - sales-funnel
  - email-marketing
  - conversion
people: []
companies:
  - bodycypher
status: raw
---

# BodyCypher Sales Funnel

*Documented from whiteboard session — January 2026*

---

## Overview

The sales funnel moves people from first hearing about [[bodycypher|BodyCypher]] to becoming a paying member. It ends when someone pays — at that point, they enter the Customer Success funnel.

```
ACQUISITION → LANDING PAGE → SURVEY → THANK YOU EMAIL → WELCOME SERIES → SALES PAGE → PAYMENT → [CSM]
```

---

## Stage 1: Acquisition

**Goal:** Drive qualified traffic to the landing page

### Organic Channels
| Channel | Notes |
|---------|-------|
| SEO | Blog content, keyword targeting |
| Social | Instagram, LinkedIn, Facebook |
| Podcast | Guest appearances, own podcast? |
| Word of Mouth | Referrals from existing users |

### Paid Media
| Channel | Notes |
|---------|-------|
| Meta (Facebook/Instagram) | Primary paid channel |
| Google | Search + Display |
| TikTok | If targeting younger demo |
| Influencers | Wellness/fitness creators in Bangkok |
| PR (Magazines/Content) | Health publications, lifestyle media |
| Events | Wellness expos, fitness events |

### Other Channels
| Channel | Notes |
|---------|-------|
| Marketplace | Health/wellness platforms? |
| Referral | Structured referral program |
| Outreach (DM) | Direct messages to prospects |
| Outreach (Email) | Cold outreach campaigns |

---

## Stage 2: Landing Page

**Goal:** Capture interest, drive to survey

### Page Structure

```
┌─────────────────────────────┐
│          HERO               │
│   Headline + subhead        │
│   Primary value prop        │
│   CTA button               │
├─────────────────────────────┤
│      OLD vs NEW             │
│   Current way (problems)    │
│   vs                        │
│   BodyCypher way (better)   │
├─────────────────────────────┤
│          CTA                │
│   Secondary call to action  │
│   "Get Started" → Survey    │
├─────────────────────────────┤
│       THANK YOU             │
│   (Post-survey redirect?)   │
└─────────────────────────────┘
```

### Key Elements

1. **Hero Section**
   - Strong headline (pain or outcome focused)
   - Subhead explaining the product
   - Clear CTA: "Take the Survey" / "Get Started"

2. **Old vs New Comparison**
   - OLD: Hospital health checks (expensive, confusing, no action)
   - NEW: BodyCypher (affordable, clear, personalized supplements)

3. **CTA Section**
   - Reinforce the offer
   - Secondary push to take survey

4. **Social Proof** (not on whiteboard but needed)
   - Testimonials
   - Credibility markers

---

## Stage 3: Survey

**Goal:** Qualify leads + capture email

### Survey Structure (3 Pages)

**Page 1 (P1) — Basic Info**
- First Name
- Email

**Page 2 (P2) — Demographics**
- Age
- Gender

**Page 3 (P3) — Qualification**
- Last blood test (when/where)
- Price ladder (what would you pay?)
- Health goal
- Currently taking supplements? (Y/N)

### Survey Notes

- Keep it short (under 2 minutes)
- Mobile-optimized
- Progress indicator
- P3 questions are key for segmentation:
  - **Last blood test:** Recent = more health-conscious
  - **Price ladder:** Helps validate pricing
  - **Health goal:** For personalization
  - **Supplements Y/N:** High-value signal if yes

### Mapping to Existing Survey

Current survey (v3) has:
- Name, Email ✅
- Age, Gender ✅
- Location, Thai/Expat ✅
- Health motivation ✅
- Family history ✅

**To add based on whiteboard:**
- Last blood test (when?)
- Price ladder / willingness to pay
- Supplements Y/N

---

## Stage 4: Thank You Email

**Goal:** Confirm submission, set expectations

### Triggered: Immediately after survey completion

**Content:**
- Thank them for signing up
- Set expectations (what happens next)
- Mention welcome series coming
- Link to community (LINE/WhatsApp)

---

## Stage 5: Welcome Series

**Goal:** Educate, build trust, drive to sales page

### Email Sequence (5 emails)

| # | Email Focus | Goal |
|---|-------------|------|
| 1 | Welcome + Introduction | Who we are, what to expect |
| 2 | The Problem | Why health checks don't work |
| 3 | The Solution | How BodyCypher is different |
| 4 | Social Proof / Stories | Testimonials, case studies |
| 5 | Soft Pitch + CTA | Limited offer, drive to sales page |

### Email 4-5 Transition

- Email 4 ends with subtle pitch
- Email 5 includes clear CTA to sales page
- Consider urgency element (early access, limited spots, etc.)

### Timing (To Decide)

Options:
- Daily for 5 days
- Every 2 days
- Weekly

**Recommendation:** Start tight (daily or every 2 days) to maintain momentum while they're interested.

---

## Stage 6: Sales Page

**Goal:** Convert to paying member

### Page Elements

```
┌─────────────────────────────┐
│      CALENDAR BOOKING       │
│   or "Choose Your Package"  │
├─────────────────────────────┤
│         STRIPE              │
│      Payment form           │
│   Credit card / PromptPay   │
├─────────────────────────────┤
│          $$$                │
│   Payment confirmation      │
│   → Redirect to CSM         │
└─────────────────────────────┘
```

### Key Elements

1. **Clear offer summary**
   - What they get
   - Price
   - What's included

2. **Calendar/Booking element** (optional)
   - May include scheduling component
   - Or just payment, then schedule later

3. **Payment (Stripe)**
   - Credit card
   - PromptPay (Thailand)
   - Mobile-friendly

4. **Trust elements**
   - Money-back guarantee?
   - Security badges
   - Privacy assurance

---

## Stage 7: Non-Converter Follow-Up

**If someone doesn't convert after sales page visit:**

```
EMAIL + CALL
     ↓
Follow-up sequence
```

### Follow-Up Strategy

1. **Email sequence:**
   - "Saw you visited but didn't sign up"
   - Address objections
   - Offer help / Q&A

2. **Call/outreach:**
   - Personal touch for high-value leads
   - Could be WhatsApp/LINE message

---

## Conversion Points & Metrics

| Stage | Conversion | Target |
|-------|------------|--------|
| Landing → Survey Start | Click to start | 30%+ |
| Survey Start → Complete | Finish survey | 70%+ |
| Survey → Email Open | Open rate | 50%+ |
| Welcome Series → Sales Page | Click rate | 20%+ |
| Sales Page → Payment | Purchase | 10%+ |

---

## Tech Stack / Tools

| Component | Tool | Notes |
|-----------|------|-------|
| Landing Page | ? | Need to decide (Webflow, custom, etc.) |
| Survey | Tally | Already using |
| Email | ConvertKit | Or alternative |
| Payment | Stripe | + PromptPay integration |
| CRM | ? | Track lead status |

---

## Open Questions

1. **Landing page platform?** Build custom or use Webflow/Carrd?
2. **Welcome series timing?** Daily, every 2 days, or weekly?
3. **Email 4 soft pitch content?** What's the hook?
4. **Sales page: booking first or payment first?**
5. **Non-converter follow-up:** Manual or automated?
6. **What's the urgency/scarcity angle?** Early access, limited spots, etc.

---

## Next Steps

1. [ ] Finalize survey questions (add price ladder, supplements Y/N)
2. [ ] Write landing page copy (HERO, OLD vs NEW, CTA)
3. [ ] Draft 5 welcome emails
4. [ ] Design sales page wireframe
5. [ ] Set up Stripe + PromptPay
6. [ ] Connect survey → email automation

---

*Last updated: January 2026*
*Source: Whiteboard session with email marketing specialist*

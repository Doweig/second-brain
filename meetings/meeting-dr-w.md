---
type: meeting-notes
date: 2026-02-01
source: transcript
tags: [longevity, lab-testing, product-feedback, competitive-analysis, optimal-ranges]
people: [nick-warot, art-chawapon-kidhirunkul, kojchakorn, guillaume-doweig, ploylada-thanapaisarnvorakul]
companies: [bodycypher, bdms-wellness, bnh-hospital, nhealth, pathlab, vitalab-thailand, function-health, quest-diagnostics, circle-dna, superpower, grail, max-life, spotmas, equinox]
status: raw
---

# Meeting Dr. W

Date: February 13, 2026
Created by: Guillaume William
Summary: [[nick-warot|Dr. W]] is tasked with connecting with nHealth for pricing discounts and API access for lab results. He emphasizes the importance of personal health monitoring, utilizing genetic testing and AI for lab result interpretation. Concerns about optimal ranges for blood tests are discussed, advocating for more relevant data for Asian populations. Insights reveal a growing demand for home blood collection services and a competitive landscape with varying lab prices. Future plans include developing a prototype for direct-to-consumer lab testing, focusing on convenience and affordability.

Summary

### Action Items

- [ ]  Dr. W to connect with nHealth regarding pricing discounts and API access for lab results
- [ ]  Dr. W to inquire about nHealth's discount structure for clinic partnerships and volume commitments
- [ ]  Dr. W to ask nHealth if they have API access for retrieving test results programmatically
- [ ]  Find lawyer with medical expertise to review legal requirements for blood collection services
- [ ]  Dr. W to share contact information for software engineer friend (former Agoda employee, ~5 years experience)
- [ ]  Follow up on prototype testing once ready (estimated next month)

### Dr. W's Personal Health Practice

- Conducts annual comprehensive checkups at nHealth (last checkup January 2025, cost ~10,000-20,000 THB)
- No x-rays for past 3+ years; focuses primarily on blood work
- Monitors own health closely due to family history of diabetes, high blood pressure, cholesterol, and stroke
- Completed genetic testing via Circle DNA (whole exome sequencing) and specific APOE and MTHFR gene tests
- APOE results showed 0.6x risk for Alzheimer's (40% below average)
- Recent DEXA scan showed increased muscle mass but also increased fat mass compared to 6-7 years ago
- IGF-1 level at 200 (higher than optimal range for age, which should be 120-140)
- Currently planning to focus on muscle gain this year

### Clinical Interpretation Workflow

- Uses ChatGPT extensively to summarize patient lab results and prioritize findings
- Creates written summary reports for patients (new practice, not yet widely implemented)
- Finds ChatGPT superior to Gemini for medical interpretation
- Currently screenshots lab results due to inability to download PDFs from hospital system
- Expressed interest in API integration with hospital eClinical system for workflow automation

### Optimal Ranges Discussion

- [[bdms-wellness|BDMS]] and nHealth use NHANES data for optimal ranges on basic metabolic panels
- No optimal ranges currently used for hormones at BDMS; reference ranges only
- For hormone optimization, Dr. W considers 30-35 years old as 100% baseline target
- Expressed concern that presented optimal ranges for some markers (like fasting glucose, LDL) were too high
- Suggested using 25th-75th percentile for optimal ranges rather than 5th-95th percentile used for normal ranges
- Noted lack of Asian-specific population data; most reference ranges based on US, European, or Scandinavian populations

### Product Concept Feedback

- Confirmed that AI-generated interpretations with doctor review would be acceptable
- Strongly prefers simple, actionable recommendations over extensive data (top 3-5 action items maximum)
- Had negative experience with data overload from past self-tracking efforts
- Would personally use the product if priced similarly to direct lab costs (~10,000-20,000 THB annually)
- Prefers testing cadence of 2-3 times per year (every 4-6 months)
- Values nurse home visits for blood collection convenience (prior experience with Vitalab was positive)

### Patient Behavior Insights

- Growing number of Thai patients requesting nurse home visits for blood collection
- Patients increasingly using ChatGPT to select tests and interpret results independently
- Observed that patients prefer avoiding time-consuming clinic visits and fasting requirements

### Competitive Landscape Observations

- Vitalab experience: 15,000 THB for blood test, 7,000 THB/month for supplements, ~3 weeks total turnaround, 5-minute doctor consultation by phone
- ChatGPT analysis suggested Vitalab's supplement recommendations were not personalized
- Testosterone test results showed significant variance across labs: BDMS (900 ng/dL), nHealth (700 ng/dL), PathLab (550 ng/dL) on same day
- Variance potentially explained by stress hormone (cortisol) impact on testosterone levels

### Lab Partnership Considerations

- nHealth pricing generally more expensive than US Quest Diagnostics despite expectations
- Dr. W estimates 10-20% discount possible from nHealth for clinic partnerships
- PathLab perceived as less reliable based on public hospital experience, though cheaper
- Medtech personnel (not nurses) legally permitted to perform blood draws outside hospital/clinic settings
- Daily rate for medtech: 500-800 THB

### Target Market Validation

- Estimated Bangkok market size: ~100,000 potential customers
- At 10% market share with 30,000 THB annual spend: ~300 million THB revenue potential
- Foreigners (especially Middle Eastern) remain primary customer base for BDMS wellness services
- Thai customers highly price-sensitive; willing to travel outside Bangkok for cheaper alternatives

### BDMS Wellness Expansion Plans

- BDMS investing heavily in nHealth this year
- Planning luxury wellness residential complex combining Equinox gym, medical clinic, and retirement housing
- Currently partnering with Mövenpick hotel for wellness retreat packages
- Operating Sea Pangolin resort in Phuket with medical services upsell

### Supplement Strategy Discussion

- Custom supplement mixing (like Max Life, BDMS) is expensive and labor-intensive
- Repackaging finished supplements (e.g., from iHerb) into daily sachets is more cost-effective alternative
- Requires pharmacist license for supplement business in Thailand
- Estimated cost for Vitalab-style supplement package: 2,000-3,000 THB vs. 7,000 THB retail

### Conference & Networking

- Dr. W planning to attend NUS longevity conference in Singapore (end of February, 26-27)
- Also considering LA anti-aging conference at end of 2026
- Mentioned Thailand hosts annual anti-aging events but content has become repetitive

### Next Steps for BodyCypher

- Prototype target: completion next month
- Current blocker: legal review for blood collection services
- Budget committed: 3 million THB for development
- Focus on establishing nHealth partnership for lab pricing and API access
- Product positioning: direct-to-consumer lab testing, bypassing hospital/clinic markup

Notes

# Meeting with Dr. W — February 13, 2026

**Duration:** 3 hours (two ~60-min blocks + buffer)
**Goal:** Assess personal fit with [[bodycypher|BodyCypher]]'s mission + gauge intellectual engagement with the product problem

---

## Opening (~10 min)

Casual catch-up. Build rapport before going into structured conversation.

- How's everything at BDMS Wellness?
- How are the clinic plans progressing? Any updates on timing, the business partner situation?
- Is he still feeling hesitant about making the leap, or has that shifted?

> **Listen for:** Does his clinic venture overlap with what BodyCypher is building? Is there a complementary angle (his clinic could use BodyCypher's platform), or is it potentially competing?
> 

---

## Block 1: His Health, His Approach (~50 min)

**Purpose:** Understand whether Dr. W is the target customer — not just a doctor who treats the target customer. If he personally feels the pain point, partnership alignment becomes much stronger.

### His Personal Health Practice (20 min)

- How do you monitor your own health? Do you do regular blood work?
- How often do you test? What's your cadence — quarterly, annually, ad hoc?
- What markers do you personally care about most? Anything you always check that isn't in a standard panel?
- Do you follow a specific protocol or framework (e.g., longevity-focused, performance-focused)?
- Where do you get your own blood work done — at BDMS, or somewhere else? Why?
- Do you track anything longitudinally — trends over time?
- Do you take supplements? If so, based on what — blood results, general knowledge, something else?

> **Listen for:** Is he a "check the box" annual checkup guy, or genuinely into optimization? Does he track trends or just look at snapshots? Does he feel underserved by existing options even as a doctor?
> 

### The Gap He Experiences (15 min)

- When you get your own results back, what do you actually do with them?
- Do you have a system for tracking changes over time, or is it mostly mental?
- Have you ever felt like existing tools — even hospital systems — fall short for your own use?
- If you could design the perfect post-checkup experience for yourself, what would it look like?

> **Listen for:** Even doctors experience the "now what?" problem. If he describes frustration with his own results workflow, that's a strong signal. If he says "I just know what to look for" — he may not feel the pain point personally.
> 

### What He Sees in Patients (15 min)

- When you give patients advice after a checkup, what format is it in? Verbal only? Written?
- Do you think your patients actually follow through on your recommendations?
- Have you noticed the "forgotten in two weeks" problem — where patients come back and can't remember what you told them?
- What would make patients more likely to act on your advice?
- If a patient came back 3 months later with a structured action plan they'd been following — would that change the dynamic of the follow-up visit?

> **Listen for:** Does he recognize the format problem (oral → forgotten)? Is he frustrated by patient non-compliance? Does the idea of structured, written action plans resonate with him as a clinician?
> 

---

## Break (~10 min)

Coffee, bathroom, reset. Natural transition point.

---

## Block 2: The Science & The Format (~50 min)

**Purpose:** Show substance. Position yourself as someone doing real research, not just building an app. Gauge whether he's intellectually engaged with the problem space.

### NHANES Optimal Ranges Database (25 min)

**Setup:** "I've been working with a US national health survey database — NHANES — that's been running for 40+ years. It's often used to calculate optimal ranges, not just standard reference ranges. I wanted to show you some of what I found and get your take."

Walk through 3-4 examples where optimal ranges differ meaningfully from standard reference ranges. Good candidates:

- Vitamin D (standard: 30-100 ng/mL vs. optimal: 40-60)
- Ferritin (wide standard range vs. narrower optimal)
- Fasting glucose (standard "normal" vs. optimal for longevity)
- TSH (standard vs. functional medicine range)

**Questions to ask:**

- Do you use optimal ranges in your practice, or stick to standard reference ranges?
- Does BDMS use standard reference ranges only? Is there flexibility?
- How do you handle the gap between "normal" and "optimal" with patients?
- When a patient's result is technically "normal" but not optimal — what do you tell them?
- Do you think patients would benefit from seeing where they fall on an optimal range vs. just pass/fail?
- What's your reaction to using population data like this to define targets?

> **Listen for:** Does he light up at the data, or does he seem skeptical? Does he already think in terms of optimal vs. normal? Is he constrained by BDMS protocols or does he have room to practice differently?
> 

### Product Interpretation Demos (25 min)

**Transition:** "So if we agree that optimal ranges matter, the question becomes — how do you actually communicate all of this to someone who isn't a doctor? Let me show you what some companies are building."

Pull up 2-3 examples on your phone/laptop:

- **Overall health scores** (e.g., Function Health's dashboard, [[superpower|Superpower]] Score)
- **Organ-specific metabolic scores** (e.g., liver health score, metabolic health score)
- **Structured action plans** (dietary recommendations, supplement suggestions, lifestyle changes)
- **Per-marker education** (click a marker → learn what it means, why it matters, how to improve)

**Questions to ask:**

- As a doctor, would you find something like this useful in your practice?
- Would you trust AI-generated interpretation if a doctor reviewed it before the patient saw it?
- Do you think your patients would engage more with this format than a verbal consultation?
- What would you add or change about what you're seeing?
- Is there anything here that feels misleading or oversimplified from a clinical perspective?
- Would you personally want something like this for your own health tracking?

> **Listen for:** Enthusiasm vs. skepticism. Does he see himself using this as a tool, or does he think it undermines the doctor's role? Does he instinctively start suggesting improvements — that's a great sign of engagement. If he dismisses it as "gimmicky," that's important to know now.
> 

---

## Wrap-up (~10-15 min)

Don't push for commitment. Let him process.

- What stood out to you today? Anything that surprised you?
- What are you most skeptical about?
- Is this something you'd want to explore further — even just as a conversation?
- Would you be open to reviewing a prototype action plan if I put one together?

> **Strategic note:** You're not asking "do you want to join BodyCypher?" You're asking "are you intellectually curious about this problem?" If he is, the partnership conversation happens naturally. If he isn't, you've learned something valuable.
> 

---

## What You're Assessing

| Signal | Strong Fit | Weak Fit |
| --- | --- | --- |
| Personal health practice | Actively optimizes, tracks trends, frustrated by tools | Annual checkup, doesn't track, satisfied with status quo |
| Patient follow-through | Recognizes the "forgotten advice" problem | Thinks patients just need to listen better |
| Optimal ranges | Already thinks beyond reference ranges | Sticks strictly to standard ranges |
| Product demos | Suggests improvements, sees clinical value | Dismisses as gimmicky or unnecessary |
| Overall energy | Asks questions, wants to see more | Polite but passive |

---

## Prep Checklist

- [ ]  NHANES data ready to show on laptop (3-4 biomarker examples with optimal vs. standard ranges)
- [ ]  Product screenshots/demos ready (Function Health, Superpower, or similar — health scores, action plans)
- [ ]  Panel builder prototype — have it available but don't force it. If conversation goes there naturally, show it briefly
- [ ]  Note-taking setup (phone or notebook — capture his exact words on key reactions)

---

## Post-Meeting

- Write up notes within 2 hours while fresh
- Key decisions: Is he a potential partner, advisor, investor, or just a friendly doctor?
- Compare engagement level to Dr. C meeting
- Identify follow-up action items and timeline

Transcript

Yeah, so what I'm interested, so two parts. So first of all, I wanna ask you about your health and how you approach longevity and checkup for yourself. So that should take about an hour. And then the second hour will be just showing the Showing you the product, what I have, what I want to do, just to get your feedback. So yeah, it should be basically an hour, an hour and then That's it. So yeah, do you do, when was your last checkup?

Hmm.

My last breakup is quite good. Everything is... Everything is okay except the text Detection scan. Why was it not good?

Oh, because...

I was expecting because I do all year training with the trainer. Last two years. for the whole year and then Uh... I found that my muscle mass because I did once in like One DEXA in my prime age, maybe like six seven years ago Okay, like 28 is the prime And then after that I compare now to there. And then... My muscle mass is a little bit increased. Okay. But the fat mass is a little bit more also.

Right. But maybe because at that time I run a lot. Right. I do a marathon, I do like-Oh really? Okay. Yeah, do badminton and other things. Okay. Yeah. And that time for the diet, I... eat the same diet like not not too much of the fatty or the sugar i already cut that And now the result is quite For the blood marker, everything is normal. My cholesterol, my other thing is, everything is normal. That's good.

Yeah. Blood, but the body composition, Maybe I found that my hormone is a little bit dropped from the stress from work. I have a lot of things to focus, so that's why everything is dropped. Ciao.

So you're saying you gain Hormone you mean like testosterone a bit lower than you want and body fat percentage will be higher than you want?

Yeah, so I think that this year I'm gonna focus mainly on gaining the muscle. Yeah, so I don't know if I talked to you or not, I'm planning to gain the muscle and then...

That's great, that's hard, I'm trying for years to gain muscle and... Yeah, yeah.

And also for the so hopefully the hormone yeah gonna get better also but you know like my when we talk about the growth hormone the IGF-1 I got like 200. Which is pretty good, yeah. It's like 20 years old. Yeah. So... But when we look at, when I talk to a lot of people in the longevity field, now they don't want growth hormone to be too much. Oh, they think it's too much already? Yeah, actually it should be in the age range, plus or minus 10%, so that should be the optimal range for you to be more healthy.

So for your age, is it 150, 140?

Yep, 120 to 140. I got 200 so I thought that it's gonna be great.

I thought it's great, like a high growth formula. Before that I also believed that.

It means you can train a lot. Yeah, I can train and then I can easily gain. Yeah. Yeah. But yeah. Yeah. Maybe because I have good sleep also. My sleep is quite good. It's good sleeping like a baby.

I see you.

One of the other things, if I tell you more about my health condition, actually my dad and my mom has everything. Diabetic, high blood pressure, the cholesterol, yes everything and my dad also have stroke Oh wow, so easy to get that. Yeah, so I come from So I know that I have to make myself healthy, otherwise I'm gonna be like them.

Oh wow, so you're checking all of this closely? Yes. When was your checkup, sorry? How many months ago?

Last year. Maybe beginning of last year, January, February. Okay. Maybe I'm gonna do it again. About a year ago. And... I also check my genetics. For the wrist, like the upper ear jean, You know typing for the risk of Alzheimer's? Do they carry any risk? Okay. Of Alzheimer's?

What service did you use to do that? Which service do you remember? Like Genius or there's a few in Thailand.

Actually I sent to him help.

Okay. Oh, it's a circle.

No, the circle DNA, I did the whole thing. Yeah. Inside, because circle DNA, you need to understand this, the circle DNA is fast read. So sometimes they can miss some small gene.

Oh, because it's hexome sequencing. Yeah, hexome. So you did the whole genome sequencing.

Oh, no, the whole exome. Okay. The whole exome. But sometimes when it's fast read,Oh, I see what you mean. Yeah, Nick and Paul. Nick and he, something like that. So yes, I did a Specific gene test for the APOGE gene and MTHMR gene. MTHMR gene is, I don't know, do you know, like it's for the risk for Hyperhomocytingin for the heart disease and brain disease also. How accurate is this?

It's accurate. You think it's very accurate?

Yeah, it's accurate. Because I have a few also. So you know that, okay, are you more risk to having this or not in the future? Right. So after the test, the test came out good, so I'm happy.

No one's having it for you.

Yeah, I'm 0.6 times... Develop the risk of Alzheimer's 0.6, not one. If you get one--So you're 40% below?

Yeah, 40% below. Something like that, okay, that's great. Do you remember the price for your checkup? Hmm. Like a rough range, you know, 30k, 20k. A year, right? Like that one, yeah. Last year.

Yeah, because the genetic test only do one So you don't need to repeat again?

Yeah, I guess that was the case. I mean, more like the actual checkup, like with the blood draw.

Maybe because I know the players, it's not going to cost $13,000. Yeah, it's gonna cost around, I believe that the 10 to 20 thousand is It's the range for that.

10 to 20k that's what you paid?

Yeah, for all the hormones, all the biomarkers.

Did they also do like x-ray, CT scan, ECG?

I didn't do because Because I know that this is like not the age to do Yeah.

Great, love this.

For the x-ray and for other things, I believe that now the model is going to be more like a You do the bleh. Most people are going to feel more comfortable if they do only the blood first and if they found something wrong they could do the radiology study for that later, yes.

That's great. I don't have to convince you of a blood test. You don't have to. No, because some doctor... Um... Actually, even Dr. Chawap was a bit skeptical at first because he was saying that, you know, like, People like to do the x-ray, they want to do x-ray every year, but it's like, "Yeah, but is it really important? Do you do it every year?" And it seems like, "No, actually, Blood is something you want to do often because it's easy.

Yeah, it changes. And it's actually most of, like 90% of the data is from the blood, right? Yeah. Like the x-rays, like, yeah, whatever, no cancer.

I know that from the one patient. Before I did the wellness, like the checkup, routine checkup, and there's a company, something like some foreign company like this, and there is one lady from European country, she asked me that why she has to do the shared x-ray every year. I got like Oh, yeah, you don't need to do every year because she afraid of the exposure to the radiation.

Yeah.

So that's why I asked my senior doctor. Yeah. So that she said that Does she know that in Thailand and in Bangkok we have more risk of tuberculosis?

Okay, yes, yes. Tuberculosis is... Why not an infectious disease? And it's on the skin or lungs? Lungs. Lungs.

Yes. So that's why we do every year. Okay. But I think that reason is not that strong.

Is there a way to detect tuberculosis from the blood? Spew them mostly.

From the spit? Yeah.

Yeah. Like you would know, no? If you have tuberculosis, what are the symptoms?

The same thing, like if you found X-ray that you have some spot in your lung. Then, and with the symptom, then you do the sputum test. So sputum is the main thing to diagnose.

So even the x-ray cannot tell for sure. It's just like maybe.

And the ultrasound, all those things is for to add on some like The risk that you have, you know like the software and the hardware, blockchain is like software. Radiology is like hardware. Right. So you want to see sometimes the structure is there, but you cannot change the structure the hardware. Right. Yes, I tend to think like that.

Okay. Software and hardware you mean?

Yeah. You know, like another thing. A lot of patients come to me and ask for their brain health. And we usually recommend the blood marker and MRI to see the vascular, the artery.

So you can estimate what the brain function?

Yeah, the size of the hippocampus, hypothalamus. Because if you still have normal or good, healthy hippo thalamus, Hippocampus, this is a good thing. But if you hit hypotermia, it becomes smaller. then the volume is not good.

But that's like for old people, right? For old people. For our age, we wouldn't see anything.

No. And... The thing is that we cannot change the hardware. Yes.

Yeah, we just know.

We just know and then we add something else. Oh, I see what you mean.

Do you remember, so I want to talk specifically about the checkup you did? Mm-hmm. So you said no x-ray? Only blood?

I didn't do any x-ray since... Maybe more than three years now.

And so that checkup from last year, did you have to go to the hospital or you had somebody... So they just took your blood? Yeah. Okay. When did you come to your place?

I go to N Health, so they have this space, it's called N Space.

Ah, you went to N Health directly, N Space, yeah, I've been there. It's really convenient, yeah. On the Ramaphore, right?

Yeah. Yeah. Yeah, pet bully, pet bully. And space.

And space.

Yeah, I wanted to try, what is it, mystery shopping? Yeah, yeah, so I tried all the labs.

Path lab, and health.

Yes, this one.

Yeah, it was really nice. Very fast. Yeah and super cheap right because it's the lab directly so you get the best price. Yeah, okay I took a picture. You see, that's how I do my research. I took a picture of the event.

The downside, if you don't know about that, but I... I think now more like we can interpret the result with yourself, right?

I mean, I still want a doctor. I do both. So actually my last result, So you interpret them and then I went to see [[kojchakorn|Dr. Kocha-Kon]] to interpret. And then I went to Dr. Chavapon as well. And then I went to Chagipiti. Oh my God, everybody saw my result. Yeah. Because for me it's more like, learning right so I want to see okay what what different doctor how they interpret What they focus on? Different style.

Different style, yeah. So that was pretty interesting.

Yeah, sometimes I also want to know what other doctors like in the video.

Yeah, right. It's very close. Honestly, I was surprised. by like 80% the same. I think I don't remember now, but maybe you focus a little bit on this thing and maybe Kotakon a little bit on this one, but 80% is the same. Same comment. So no big difference. So you interpret yourself, I guess, you didn't see a doctor? No. Yeah, it's funny because actually this is one of the big pain point I see when I talk to people who do checkups.

The doctor interpretation is very Not actionable. I would say. I think you're doing a good job. I think you're doing a good job at BDMS, but I think you're the exception, right? For most people, it's like, oh, you're okay, you don't have cancer, you can go home. It's like, okay, but I... Yeah. You know, I want to do better. Yeah. And so now, Now more and more people actually ask for GPT because they're not happy with, it's like okay, no cancer but it's a bit boring, I wanna know more.

So now they ask for GPT and I was surprised because So I've been doing this for a few years. I thought I was like the only one but I've been chatting with some friends because now I'm doing this, I'm trying to get information. Actually so many people now use ChagGPT to interpret but even to go to the lab like in health. Just in this office I met three people that, as CHPT, which test to do and then they go to PathLab.

PathLab is really close. You know PathLab?

Yeah, yeah.

So they go to PathLab and then they put back in ChagiPT. ChagiPT is their longevity doctor. They don't need. I was like, wow. Not just one, like a few.

Yeah.

So I was like wow really curious so That's when you know like inhale Last... At the end of last year, I have like a... BDMS also like the inhale arms And medium is for one doctor to talk about the product that they're going to do. which is the telemedicine to--And health. Yeah, yeah. And I did that one session for them. Okay. But, and then after that... The director of the N-Hill Uh... I'm really surprised that the approach for the wellness is different from the disease.

So that's why he said that if anything or any other opportunity he would like me to be to talk into like some other things and that's when I saw the opportunity that if I work with N Health more maybe we can get something like What you want to do in the future? For example, because in here is the lab, right? Yeah. And also they have all the data. Yeah. But except they don't have the variable device that you can link in and other things.

Yeah. So... I believe that the interpretation and AI, maybe they don't need any doctors anymore.

I think it's... So that's a debate. Yeah. I think... There's also trust, I think, that Um... People want, I think it's okay to have the AI generate the findings. But I think people still want, and even myself, I still want, because health is important, right? I still want a doctor just to check.

It's like, yes, it makes sense. Because maybe AI is like, oh, you need 50,000 IU vitamin D. You know, like, no, that's going to kill me. So just make sure that AI is not saying anything crazy.

But having the report made by AI, I think most people are okay with this now. But they still want somebody to check at least. But I think, yeah, the role of the doctor would be I mean, I think it's similar to software engineering, right? Yeah. Maybe less work per patient, but you still need a doctor I think. And maybe because the costs go down, maybe there's more patients. So at the end of the day, you need the same amount of doctor.

Because like the project I'm doing, I think is gonna make the price go down a lot. But then I think a lot of people that wouldn't do checkup every year, now they're going to do checkup every year. So actually we still need the same amount of doctors because, you know, more patients. That's the hope.

It's a good concept that you... Yeah, because it's concerning become more and more in younger generation, right? Yeah. 50, 40, 50 then you do the checkup. Just don't care, yeah. Yeah, don't care. But now if you can choose to check yourself every year, then it's a good thing, yeah. Twice a year even?

Yeah, two, three times a year is also possible.

And have you went over to the Paya Thai package that they do, like the--Yeah, you send me, yeah.

I haven't tried no.

At first, the beginning, It's good, it's a good idea that they do that.

But all you can check is what, is for the blood mostly or what?

Blood mostly.

So you can do like a crazy amount of tests? What is it that we can check?

But another thing is that They limit with the doctors. Every time that you go to the test or the lab, you have to rely on or you have to pay the consultation for the lab. Okay. Yeah, that's one of the limitations. Right. But you can do it like the normal metabolic panel. You can do it. And one CTR, one MRI, you can do once a year for this package.

Yeah, I feel like Yeah, it's focused on blood, but yeah, the things like MRI, I would really like to try, but I think it's still... Expensive and I don't see the...

I did one in China. Yeah. It's really cheap. And you thought it was useful or... For me, I... I can understand myself more because I usually have consistency headache. Yeah. And then one of the neuro doctors. Yeah. She, she measure my intracranial pressure. The pressure inside the head is too high, too much high.

Really? Okay. Yeah.

So she, she, she advised me to do an MRA.

So is it because of the high blood pressure in your family? Yeah. Yeah.

Wow. But at the end, like, Mostly from stress and maybe I don't sleep that good at that time.

Yeah, it's funny actually I have to say I have freaking frequent headaches and my dad has high blood pressure so maybe But it's sleep, yeah. For me, sleep. If I don't sleep or if I drink too much coffee, I have like crazy headaches. So you can manage.

Yeah. MIA is good and it's called like 3000 something, but in China.

Yeah, but in China, not here. Here it's more. In China, try to make everything cheap. Because the thing is, I want to do it for, I told you, this shoulder, my back, both ankle and the head, ideally. So like every part of the body where I have some kind of chronic pain, I just want to do MRI, just out of curiosity. Um... Or like past injury. Yeah. It's more like my ankles are fine, but I had past injury on both.

I just wanted to see what's up.

What if like If someone Can't tweet you without doing the MI.

It's more like out of curiosity. Like for example, the ankle, I always wonder'Cause you know sometimes you can tear a ligament and it doesn't reconnect.

But the buddy kind of adjusts, so you...

But it doesn't adjust? So you would know? Yeah.

You can tell it from how strong is the ligament. Okay. Yeah. As you know, like the elastic band. Yeah. If it's overstretched? Yeah. It loses elasticity. Okay. Okay, it's too loose. The same thing with the tendon.

So you can know without MRI?

Yeah. Maybe you should check that. So that's why sometimes the first thing you have to build the muscle so that it's become more closely and tight the joint but other thing other the orthopedic maybe they do the surgery to try to make the Elastic, the tension more closely.

Yeah, just cut a piece and put it back together.

But the re-sign is not that good. Yeah, that's what I'm thinking.

Maybe I will know but I cannot do anything about it. Yeah. So it's like, okay, good information, but I just pay 40k for that.

Yeah, I think that was good. Let me review this.

I still, I think I've done the Applebee myself. And it's okay.

Applebee is cholesterol?

Yeah, apple, apple, putti. The platforming cholesterol, the subtitle of LDL.

This one, yeah, I didn't do. It's like a special test, right? Yeah, yeah. Yes. Spencer? It's no it's not expensive define like 2000 and 2000. No, no one thousand. Oh, okay. Sorry Right then.

Maybe if you do inhale it's a little bit cheaper.

And healthy dough. Actually, Pest Lab is also really cheap out. Oh, really? People...

The hospital that I work, the public hospital, they use PetLab for special lab. But there's a lot of problems so I have bad impression about them.

Yeah, they seem not as professional at health. I can guarantee that. But I think for longevity, you know, if it's not super, super accurate, probably okay. Yeah, yeah. Do you track over time? No. Your... your test.

Yeah, if... yeah. I will see if my lifestyle changes, then I will track.

Do you use any third party tool to analyze the result or? So, Chargpt, you must be putting your PDF in Chargpt, right? No. No? No. How about your patients? Do you sometimes... Yeah, I think you told me, right?

Yeah, I put all the patient details because I want them to summarize. Okay. I need to do a summary report for everyone. I want to do this this year. So I put all the labs and patient details. without a name. Confidential. That's alright, don't worry. Yeah, into the chat GPT for the summer lives and set the priority. So because every time that you check, you want to know one or two things what is the most important for you.

Okay. So that's I make the prompt. Like the main finding. Yeah, the priority what is the main thing now. So after that, like I... Yeah, it's make I can do a lot of medical summary report really fast now. Which AI do you use? Chagivity. Because I tried Gemini, it's still not that good. Yeah, use the same prompt actually, like same prompt and ChatGPT gives me more... Better interpretation. Yeah. Maybe you should try other things but now Chativity is the main thing.

Yeah, Chativity is pretty good. I mean, just asking. Um... Do you do written... Interpretation? Oh usually it's oral Uh...

In summary report It's written, right? But you don't send that to the patient, right? I keep them. Okay. When they come to the interpretation, I'm going to tell them, okay, this is a summary. This is what we're going to talk, the main thing. Okay.

I don't think I got it when I came.

No. Because that time I still haven't done it. Oh, it's new.

It's new. Okay, okay.

The only people, the only doctor that do this, maybe I'm now, I'm starting to do. Actually, I want to code the API of the the hospital document To the chance of it. I want to do like the workflow Yes. I want to do, I asked you about, I told you that I want to do the workflow for that.

Hospital API, do they give you access to that? No.

Not not now. Yeah, I think is that they they The IT guy told me that they got an update on another program. It's called eClinical. I asked them, "Can I use this API?" For the AI? He said that, yes. Bye. I don't know.

I can show you some tricks. What you can do is you can ask So you can work with the clinic PDF actually. What I do is like I put first in charge GPT and I say, hey, can you extractExtract the blood test results. as a list so it would just say like hemoglobin and this much by nanograms, so just like a text list, and then you copy paste that into another window, and then you can ask your question.

So it's not API, but it's--The thing is that, Now the lab behind the law lab It's not that. good in arrangement so I believe that I cannot pull that PDF or the data out. Yet.

We're gone. You mean it's in the system but you cannot download?

In the system, I cannot download. So now I just like, Screenshot.

Scoring down and then copy. Yeah, I see what you mean.

I was screenshotting, yeah, that's not. That's super nice. Cool. Yeah, I think that's enough for your own experience.

Yeah. I think it's great. Okay, now I'm gonna show you on the monitor.

The first thing I want to show is I don't know if you heard of the US National Health Survey Database.

And hey? And hens.

And hens. Oh, you know this? Yeah.

And so this is used, a lot of people use that for optimal range. 'Cause you know the blood test, they have like the reference range, which is like medical, but not the optimal range. So how do you do optimal range? Like do you just have a feeling or in BDMS do you have like an internal document? We're going to do that. BMS. BMS.

Oh, Renegade, they don't.

Right now the user in him Okay Right now they use Enhance and optimal andNormal range.

Okay.

and for the hormone there is no optimal rangeIt's all because the hormone is not widely.

They use enhance, yeah so I've actually done the work. Do you know how they've done it? Because the enhance database is 50,000 people, but almost half is like sick people. So you need to remove the sick people. So they've done this already? And a BDMS masking.

Not yet. For the special lab. But for the normal lab, like, metabolic... Pano?

Yeah.

They use in hand. For like optimal range? For optimal range. Let me show you.

Wait, don't wait, I didn't say anything. But... Another thing Yep. It's not BDMS. isInhale. Oh, doing this.

Doing this. Because I see in my report they have a Display settings, let me do screen mirroring. Um...

明? Beer. Okay.

What did I want to show?

Yes, so I'm asking because it's a bit difficult like so in here so there that was my report and So for example, we can look at What's interesting and not too boring? Creatinine?

No, I think it would be too difficult.

I think the LDR that they do, the Optimal I don't know if I did it.

You did. Are you sweet?

Yeah, this one. LDL Direct? Yeah, you see down here the normal range and then the optimal range. Less than 100 I live in town. Sorry.

Normal range.

Yeah. And the lower one is optimal range, you see? Less than 100 is considered optimal.

So that's normal range LDL, that's LDL direct.

So they say reference range is 130, but optimal is 100. Yeah. Okay, that is LDL correct. Well, let's see. So I've done the work.

So LDL cholesterol, that's the one, right? Yeah. So we can do for mail. So this is...

I haven't saw thisOh, so this is mine.

Oh, okay.

This is my own website. Okay, okay. So this I work with AI to make this. So I've downloaded the enhanced and HINTS or whatever you call that. So it's six gigabytes. It's like hundreds of thousands of markers.

And I use AI to kind of like compile the data.

So here you see the raw data and this is like an estimate.

So male only compared per age.

So this is the distribution, don't care. So 32, 39, so reference range is 100 actually.

That's why sometimes it's not exactly the same.

So they say the reference is less than 100. And the optimal is less than 150. Does it sound a bit too high to you? Yeah.

For me, I'm not that...

I mean, this still needs some work. This is like a draft I finished yesterday.

I want to see the labor candidates. Or maybe a home IThey're fasting, below their fasting.

Metabolic? Fasting glucose. This one. Home I am the Who am I? Sorry. This is distribution so we remove, yeah. Clinical range is supposed to use, I don't know which data he's using.

It's 2 or 2.5 Yeah, 2.5.

So that's for male only. Forbidden. Is there a difference? No.

And then optimal range is almost the same, maybe a bit higher, less than 3. Do you agree with this or do you think it's too high? You think it should be lower than that? Yeah. Home AR should be as low as possible.

Because when we talk about optimal, it should be in the healthy zone. So the healthy zone should be 2. For me, I use 2. We tend to find that if you have higher insulin Then you are more fun.

Let me take a picture of this. So this is a draft. So that's why I wanted to show you because I wanted to see if you agree or not with those results. Because I'm not a doctor, it's difficult for me to interpret. And you're saying the LDL is also too high? Was it gonna take it? I'm gonna so this is The first draft. I finished this yesterday, okay? It's working. I'm already happy it's working. But the data needs some more work.

Is there another one you want to see? Creatinine. So he seems to be saying a bit lower than the clinical range.

I believe that there is no optimal range for the Great. Great evening. Oh, wow. Yeah. That's better than... Maybe you can try them. There's no almond in it, right? That's how I'm on the tower.

Oh. Uh...

I don't agree too much either. I think it's pretty low. Sorry, because this one you have to separate. It's important. But you see male, 20s, 700.

And you see why 60 to 65 is a little bit higher, like to 700. Why 30, 40, 50 not higher?

Let me check, maybe few patients, only 73 patients.

So maybe that's why.

Because, you know, like... I wouldn't say it's optimal. I would say it's normal range, I think. Yeah, this is normal.

Because it's a survey of healthy individuals, right? So it's not... It's not the best, it's more like what the normal population looks like.

When So how do you do optimal?

If not the NH or maybe I should use different filters?

Yeah, you should use different filters. This is just like the data that you collect from the NHANES.

So I took this data, I removed sick people and then I just do the average.

I think this is good for the normal range. Right. Okay. But for the optimal range, for the hormone, especially when we talk about hormone. As you know the hormone is dropping every year, 1% after 35-40 days. My mentor, a lot of doctors in the conference, they tend to treat that 30 to 35 years old is theOkay Consider that 100%.

30 to 35. 30 to 35.

So when you use the hormone or when you want to target the hormone, you want to be at 100%, which is 30 to 35.

Okay, as close as possible. Yes.

So you can use that range. For everything? For everything. For only the hormone?

For the hormone, sir. But things like... I need some work.

TSH is more like a disease.

Oh, okay.

Yeah, it cannot set the optimal range that much.

This one is funny, you see the free T4 is always below the recommended clinical range. Yeah.

And you know like for the free C4, the optimal is 1. So you see it's below 1. Everything is below 1.

I mean above one is good or bad?

Above one is going to be a little bit more high Hypo.

Okay, and below is good? Below is hypo. This is not good. So it has to be around one. You cannot be a... Yes, so it's a bit low. I mean... Yeah.

Yeah, I believe that this is the data. Also, like in the DEXA scan, ThatYeah. When you see like the range that I put it in on that table I put The data in here and that data is usually from the Mexico and US data and European country. So when you compare them, the result is actually the population of the European, not Asian. Not Asian. Yes.

This is American as well.

And your European is Scandinavian, not... Not England, not French, not something like that.

So, you know Scandinavian have more muscular and more larger body, right?

So, down here is smaller. Difficult. Yeah. So, when I interfere with the result, I have to be, know that.

Is there a good data set for Asian? Not yet.

Not yet.

Yeah. As I see now, there's no data. I cannot find any data from Asia.

So optimal range, it's actually difficult to just get optimal range?

We have to collect a lot of data, a lot of in. Subject, the sample from the normal healthy. Yeah. If we can do that, then we get the optimal. Is there a...

Some kind of ministry in Asia that release a lot of data that you guys follow or... Like maybe Singapore Institute or something or maybe in Thailand is there like a Thai The data mostly come from Japan.

Yeah, Japan. Singapore is not that much actually because they have like very small country. They don't have that much population.

And their population is getting older.

So maybe China, maybe the Philippines. They're starting to collect this.

That would be great, yeah.

Yeah, but now every, every Panel for the blood test and also the body composition they try to find in Asian but they cannot find.

It's hard, okay. That's great. Okay, so it means if I can find something, then it would be a--It's the same with Germany.

In Germany they use other things like body composition and they use leanMass index. I also tried to find it and it's all in German.

Right. Yeah, I noticed.

Not easy, yeah. No. So, yes. What you do is that it's good for the range of for normal. Yeah, I would say it's normal. Yeah Oh, the average? Yeah. For the data that you have? Yeah. But for the optimal?

It's not optimal, yeah. No, not optimal. Okay. Great, I mean that's great.

And you know like the range that you use is too much or too low. I mean like you use 5% you cut out the middle of 5 and above 95% because you try to cut out lighter.

This is not good. Are you says good?

For the optimal is too much? For the normal is okay?

So you mean you need to cut out the outliers, right? For optimal? For optimal. For normal, you kind of ally it. But for Optimal you don't want to cut them out?

For Optimal you want to be like... Close to the middle at pointRight.

Maybe you can use like, 25.

75 maybe.

Yeah, so this is the Optimo at layer, yeah I mean Optimo is using the standard range, so Optimo is using the middle using the middle. I think optimal so is using the middle and then doing two standard deviations or one standard deviation.

Yeah, and maybe you see the The head range. Yeah, which one is more... But it's good that you do the subgroup into different age group every 10 years.

Yeah, I think it's just for simplicity, right? Yeah. I think I need to... Yeah, I get maybe more that I said.

Yeah, one side of the equation can be the optimal range.

Right.

Yeah, because one standard deviation above and below is like, what, 70%?

Hm Maybe 25-50. No, that's too close. Let's see.

Okay, I'll look at them. Cool.

So that's for the range.

The actual blood panel, we're not going to review because I think it's kind of boring. I also have a website for... Okay, I just want to show you, but we're not gonna review, because I think it's too time consuming. So I've made another website to So these are the main competitors overseas. And I want to know how much They pay in US, so they're using Quest. I want to know how much they pay and I want to know if I do the same test with any health, how much I would pay.

And so I have some Nhealth estimation to compare. Actually, Nhealth is more expensive than Quest. Did you know? Yeah. Uh...

Maybe because they already done that. Yeah, I think there's just more scale.

And then I have the panel builder so this will be like later I guess. Like I can add for example vitamin D with the hydroxy So you can make your own panel? Test, free test. I think you can compare the price. Oh good, that's good.

So you get all the data from PenHail, right? How did you get like as a Inhale is really expensive at TF1. IGF.

Why is it showing the... Yeah, there's still some bugs. It's showing in dollar. I think it's converting IGF. 23, so it should be... Where's the X-35? That's actually pretty cheap. 800 baht.

Yeah, it sounds cheaper than...

I found this one thousand.

I thought there was one more in there. I have a Yeah, yeah, everything.

My key research ThailandCan you find any health? I'm so confused. Sandwiches, any health?

No. No, maybe I don't have it here.

There's another place that The body builder will go to the for the lactase but in the public hospital, Julano-Cord Hospital.

Oh, this one, look. So this is how I get the pricing data from InHealth. You know this? This is their pricing Wow, look at all. So, you can see this is the price. This is the test product name, code.

Ah. I can zoom in a little bit.

Wow, how can you get it?

I'm very good at AI, yeah, yeah. I have AI agents crawling the internet, you know. So I basically used that to create the panel build I show you. This is 100 page. It's gigantic, 200 pages of this. And so I extracted all of them and then I asked her because this is Everything they do, so some of them is not wellness. So then I ask AI to filter only the wellness biomarker. I think it was about 200. And this is what I put on the website I'll show you.

So here we get, I just want to check here to make sure my AI didn't do a mistake. IGF-1.

800, yes.

800, okay.

That's actually cheap. Yeah, I thought it was more.

I think I pay more than that. Passable. Ah. They use boom and go actually.

I think it's you told me I don't have the... Because you said I don't have... Free testosterone and IGF. You have IGF?

But you don't have free?

On BDMS in December. IGF is there? IGF is there. Maybe I'm confusing. Anyway, so I just added out of curiosity and they...

admin patient game I have so many Yeah, so...

Past that they just so they send me everything I asked for except IGF Which is... They don't have it? No, they use Woongred, look. So only that one is coming from Woongred. Okay.

Must be pretty heavy, too.

So it's good? That's the one you said you had 200, right? Yeah. 160c, so I'm also high actually.

Yeah, you're so high. You're like 30 years old. Okay.

That's great. Internal age.

35 to 30, 25. Great.

See you next time.

But my test I think when I test with you my testosterone was crazy high it's low it's it's It was 900. No, but it's not so... I've done more tests since and now it went down. Now it's more... Oh shit. I think it was too high.

I mean, it doesn't matter so much, but... Hormone test.

Oh yeah testosterone here.

Oh they use another Free test. Yeah, he's lower. Do you know how to convert this to the other... Yeah, it's... Because I think... Uh... Where did you use enamel to...

So 19 more to... Nanogram. Nanogram. 550, wow that varies a lot. Mm. It's funny, I had another test. So in December I got 900 at BDMS. Path Lab is showing me 550. And I use in health and health was like 700. And there is so much. Yeah. Quack, swing. What? What timing is it then? Roughly, it's okay, I'm not worrying too much about my health, don't worry. I'm just curious to see, Because actually, in Health and PathLab, I went the same day.

So it was the same day, like one hour apart. And some of these are different. Where's Batista's doing here?

Seven.

See, it's 200 more. Yeah. The Path Lab was, in health I went at nine, nine a.m. Path Lab I went at 11 a.m., so two hours. Wow. Is it possible? Yeah. You think it's like equipment malfunction or? or just testosterone varies this much.

It shouldn't be this much. It shouldn't be like 200. Yeah, it's 200 difference. Yeah, it shouldn't be like this. I believe that is from the labs. Yogurt is... Petlab is wrong. Nothing else. Maybe I'm biased. I would believe so as well. Because in VDMS we also use the handheld. So...

She's curious. Yeah, I guess we need to try more.

What about the Another thing that can happen is a technical error. It can be from like if you're drinking You do some other thing you have some stirWhat is? It can be coming down also like for example like heat stress or traffic stressBecause the stress hormone is bringing down the tetrasalone also.

If you move--Oh yeah, yeah, that morning was pretty busy.

If you move from inhale to palate, maybe all the way like you--Yes, I had a lot of stress actually.

No, I had to go home, And there was too much traffic, so I was late for the nurse, and I was really stressed about that. Yeah, yeah. And then I went to BathLab, so maybe that's why. It can be from there. Because he went 200 down. Yeah, so cortisol, you mean, cortisol is lowering testosterone. Yeah. Really? Yeah. Wow.

Learning so much.

Yeah, I think that's the explanation.

It's more like a functional thing. Sometimes like Uh... In medical school, a lot of time my My teacher told me that like You not only tweet the numbers Everyone wants a number. They want the number to be high.

Certainty.

But you have to know, like, or other aspects of life.

Okay, I'll show you my panel builder. This is working progress, so we cannot review now.

Still some pricing issue.

I think this is good. Looks good. Do you have to do a competition for the prize? I mean, you do this program just to see it? What's the difference? Do you want to...

Because I want to copy Function Health in Thailand. And so I want to match the test they do with N Health to see how much it would cost. And some of them actually we cannot do because and health So for example, I forgot which one. This one test is like 12,000 bats. It's very exotic. I think it's this one. Yeah, MMA. You know this? Yeah.

We don't do too much, but we do.

But so, Function Health, they claim to be doing it as part of their normal level, normal program. But in N Health, it's super expensive. It's $12,000. So this cannot, it's just too expensive in Thailand.

Maybe the Jewish that they do the lab is... They get imported from other country. So that's why the price is going up?

Okay. So for example, if we copy function help, we would need to remove this one, I think it's too expensive.

It's also non-e-impact to me. Right. It's one of the anti-inflammation. No, no, the anti-oxidants. Right.

Yeah, so think like this. I think right now, But the algorithm is broken so I still need to work on this. But I think it was estimating that it would cost like 60,000 baht. per year? Per one test. So... 50,000? Yeah, so I think it's too much. But because things like this, you know, like this one is 12,000.

I went into the functional lab. And they usually the origin of high is 20,000 something USD, right? Yeah, so it's closely to 60,000 Thai Baht.

Yeah.

Yeah, so But they can do it like 300.

Yeah.

$65. But I think that the first year I don't know, second year.

Yeah, I think the...

I mean, there is negotiation with the lab. I think we need to adapt as well, but... No, but it's great because, so, The goal of this product is direct to consumer lab tests. So it's a new industry that doesn't exist right now. Like instead of going to the hospital or the clinic and then they go to the lab, Like we send the customer straight to the lab. So we skip the hospital completely. And because of that we can make much cheaper.

And so the last Yeah.

Maybe you can... Maybe I will talk with the NL guy. And let's see if they want to do something with it. And this year, BDMS, the big chain, the head of BDMS, they want to, this year they want to invest in NHELP. To the wet? To do like the lab test and...

More lab, cheaper. Yeah.

and promote more to maybe their It used to be a day at brunch, into summer.

Oh, outside of Bangkok. Outside of Bangkok. Okay, that'd be great, yeah? Yeah.

From what I heard, this year they invest more in clean health.

I hope he's gonna make the price go down. Maybe, yeah.

Yeah, that's great. I mean, what I would really like to hear from NLT is like those prices, like how--You can't negotiate, yes. Yes, but how much? Like if we have volume, like ideally, how many tests do they, like, How to negotiate? Is it like amount of tests or amount of... How many tests per year do we need to give them before they give 10%, 20%, 30%? You know, kind of have an idea of Where the price are possible to go.

Because I know Quest apparently... They give to function health 60% discount. I guess a lot. So I don't know if here is the same or here is like, oh no, only 10%. Because this will affect the business as well.

10-20% is the earlier one. I believe.

You think it can go more? So the documents are always confused here.

Lab research and health.

Yeah, because this is the public pricing. So this is, I'm guessing, no discount. Yeah.

So yeah, if you can go down like IGF, for 400 baht? That'd be great.

It's possible. Because... This product, the core is really like Like the margin is how much we make the customer pay minus the lab. Because the AI interpretation all of this is very cheap. So the lab is the main cost. So we really need to negotiate.

And so we need the water Yes.

Yeah.

This is, yeah, do. And then the last thing I want to show you is like some, This is a panel builder.

Have you heard of ornament? No.

That is great. So it's an app to do interpretation. So they have things like this like Ultimo range.

You're gonna do the UAQ on yourself? Yeah.

Well... Okay. No, but I will hire a designer.

Yeah. Because now I'm doing a prototype. I think... Yeah. I mean, look at my UI. It looks fine, no? No. No.

No. No, but did I show you my app, right? I have another app. This one looks alright. This happens in December, yeah. Oh, okay, okay. This is my BDMS result.

You see, you also have a GF1 from... That's right. 147. In range.

Up to 160 something, right? You did the last one. Oh, you remember?

Yeah.

I don't remember.

No, maybe--You did, in this January, you go to Pat, and then you send to--Oh, maybe, yeah, yeah, so many, yeah.

No, this is not in there.

Good.

So this is the customer app and then you have the AI. They already have all my result. Well actually, what do you ask usually? For the main finding Would you be able to type something? Like find me the most important, just to see if it works. This is using, I think it's called... You can only type one message, so only one message.

Okay. It doesn't have to be sent to us on Sunday. Hi all the Ties. Okay.

Error. Why does it work? Hi. Technical difficulty happens. Hey. Nope. Okay, I need to work on this. And then here we have some prepared I think I showed you this, no? No. It's the same so... This is a recommendation right?

Yeah, recommendation for diet, supplements... Mm, lifestyle. Hmm. Like, yeah, zone 2, I have a... recommend zone 2 because I forgot cholesterol or whatever. So I think this is what a lot of people are asking. So you doctor, you don't need this, but a lot of people feel like they would rather have written an action plan.

What? Have you ever...

Do you think like a... My name is Paul. A little bit. But for me,Maybe I'm one of the lazy guy that don't want, like, try to take a photo.

Oh yeah, yeah, there's too much, yeah.

So this app, I like how they show the metabolic score. So they do per organ, and it's kind of like a bubble. This is good.

Yeah.

This is using the data. Yes. So this is a good way to show people, okay, like, why you good, why you not good. Ornament is a Swiss company so... Yeah, so they're showing, but the action plan is not great. Yeah, they also have action plan for, sorry. Yeah, so they're just two girls. It doesn't look like screenshots. Health report, sorry, vitamin, yeah, so here they show the Very mean recommendation It's similar to what I showed you.

Oh they have like extra tests I want to see the action plan.

What is this? You patient? Survey.

This is how they do the scoring. For diabetes, they look at glucose and then they give a score. That's pretty nice. So it's not on MS. I think Syphox is the one that do-yeah, yeah, yeah. So, CypherX, there is something like this, similar to what I showed you. So they give us coal per organ. And then you can see a dashboard Um... Well actually if you see something on my computer you can just open it Where is the news?

Yeah, that's a lot of information.

Yeah, that's why I wanted your opinion on this. I think it's... Nice to have an action plan but it needs to be not too much. So that's my dashboard. December, no they don't want, for some reason they prefer Path Lab. Biological age, so they give me one year younger, oh yeah great. It's not great, but it's all right. Yeah, and then for example, heart, and then they give you some... Organ per organ recommendation.

Um...

I guess you know and then you can click and then you can have you know the range What I like about this one is the action plan. I think this is also, this is, so, Can I tell you what the...

Yeah.

This is the overview and the result is like if you really want to see everything yourself which is like every single organ, every single test. What's interesting is the action plan. So they say okayCategory restriction for liver health.

And then you can do... And then they ask you more.

I think this is what people want, you know? Yeah. Because there's so much data. I think it's good to have... I don't know why it's always broken here. Okay, it should be like this. I think even this is not good enough. They should do just one score. I think I asked you out of 100.

I still don't get what 72%, 80% is what the data that they use and also like Yeah. Maybe, maybe... If I have to advise them, maybe like... Just doing like one column for each. Each of games are is systemic, is systemic. So then And the result shouldn't be like 62 or 72 is They just want to know that. How? Are they in the optimal or in the normal here? 62% and 72%, is it optimal?

Oh, normal, yeah. So that's the first question, yeah, optimal versus normal. Um... Let me check for... actually function health is pretty good, yes. Uh...

Function Health Apple Store Data, but here I think it's only the amount of marker.

I don't think they actually show.

Did they show? Nutritional plan.

The nutritional plan is easy to do. I put it in AI and then everything somehow. But the more thing is about the lab interpretation. If you can get more scores,Like the whoop, the whoop can get like stress and strain, scar, right?

Yeah.

When Yitang was got involved and Pa He Xiaomi Only who using Vogue will know. But other people... Not knowing. What does it mean by straining? You've got like... How am I supposed to like...

Yeah, I think Whoopi is doing great. I think they're... I mean you see I even put it on my... So recovery... Today is not good. Usually it's higher. Strain, so I haven't exercised yet. Sleep, yesterday I went to bed a bit too late. I'm usually above 90. I like the F3E. So we should find something a bit similar. I'm trying to find here is that yeah, okay, so That's function health, so they have action plan.

So that's how they do it, right? Top five food to focus on. And then they have the limit Ds, which is top 550 of ROID. Simple supplements. You know, it's like... People that don't have time, they just go to the action plan. And people that are just really curious, they can get access to the data one by one, you know, like this one. And then you just one by one, okay, bam, bam, bam. And then you click and then you see the history, maybe some explanation, why, blah, blah, blah.

Why is it important, you know?

I don't think normal people would like to go too much data. They just want... Three things Maybe the machine that is... to focus on.

But for yourself, if you see A product like this with an action plan like this, what would convince you to use a product like this? Is it the action plan? The interpretation has to be good or the action plan or you just want cheap as cheap as possible?

I just want something easy that I can follow and then no like to focus on right yeah Like the top five from Function, you think is good?

What was it?

Yeah, because I used to do like a lot of Yeah. Testing and a lot of like... Measurement. Here. And I found that it's too stressful for me. Too many data.

Yeah, yeah, yeah.

I cannot focus. Yeah. I cannot focus. So if I can get like one overall and then like divine to like five action time. Yeah, that's finished Better. Sounds like a... Yeah, easy for me.

So what do you think of the concept of the product? If we do like blood test like this and then into action plan like this, you know, streamline. and ideally low friction so We send the nurse to your home? The reason why I wanted to go to Pathlab and Enhealth because I want to see the clinic I think it's a bit crappy. I would rather if people don't go there. Because I think especially if it's a premium product, you know, it's like rich people.

I think if you send somebody with money to Pathlab, they're going to be like, what the fuck is this? It's so dirty.

Some other patients, last month I have one million patients. He doesn't want to come to the caning. Even medium-ass, the clinic is like big, right?

But...

He want to stay at his hotel.

Yeah.

And then we bring the dust today. We did two samples, blood samples. He always stay at the hotel.

I think it's okay because In this case, everything is in the app. Yeah. So... I know, so I tried Vitalab. I don't know if you know. Do you know Vitalab? Yeah. Dr. Ploylaida. I don't know. The owner is, she's very funny.

What was that, product research?

Mystery shopping vitalab. Yeah, so they send a nurse. YeahMm. So they do custom supplements? Yeah. So they sent an address to my place. Yeah, I try all the clinic I can tell you. It was actually nice. I was surprised. It was very fast. She just came, took my blood. Actually, that nurse was really good. Painless. They have the machine for the pressure. I'll see you.

And then a month later...

So this one, their specialty is to do custom supplements. So months later they give me supplements and then they give me this Which is funny, so I asked the IGPT Because I have the blood test, right? I say, look at those blood tests and tell me if the supplement recommendation makes sense.

I actually say, no, it doesn't make sense.

You say, actually, my... What do you say? My zinc is high, yet she recommend extra zinc. Or what were you saying? I don't know. It doesn't make sense. He said this looks, ChatGPT said it looks like she's giving the same to everybody. Like... Not personalized. There's no personalized. You see, A, what is it? Vitamin D? Wheezy. This way, 800, are you? What is this? I don't know what I'm talking about.

So... Doesn't make sense.

Absolutely scam. You know how much I paid for this? So the blood test is 15,000. For the vitamins. For the blood test. I mean for the vitamin panel. And the vitamin is 7,000 per month.

Is it subscription every month?

Yeah, but I will not be renewing, I tell you that. I just wanted to try. Packaging is pretty good though. Yeah, they give boxes like this morning breakfast dinner I'm looking at this because this would be a good upsell strategy for some people, you know, like after you do the blood test, you want to do this. But I think the way they do it is really bad.

How, like... You have to wait how many days before you get the supplement? And weThe result was really slow.

They took almost two weeks. After the blow-draw, I don't know what happened. Two weeks and they say, "Okay, now we have the blood. Now you need to book an appointment with the doctor." Another week. And then she called me on my phone. "Hello, let's review your result." And then she's like so fast, she's like, "Oh, this one okay, this one okay, this one will be high, this one will be low." Like five minutes.

to review. It was almost as many tests as BDMS by the way. Um... So really, 5 minutes to review all of this And she's like, "Okay, you're gonna receive your supplement." next week The call was like 5 minutes, it was really bad. Yeah.

Um...

Anyway, that's the competition you see, very easy to beat.

Yeah, I can see it here. 21,000 for a blood test and...

Would you use this product if we manage to do what we're talking about? Would you do it for yourself? Like every six months Send a nurse, get your blood, and then you get your result in the app with the action plan. And the pricing would be the same as the lab, honestly. We...

The casting is the nurse. But Denae is not... Message Everybody is nervous One of the contract, maybe not contract like that.

She's working, yeah, I asked her. She's working for a public hospital. She's not working for Vitalab. They just pay her for that day. So she told me she had night shift. She just finished the night shift and then she comes to my place. She was so tired. Poor girl. She just gives a blood test and then she goes to sleep. And how do you do this?

I would do this.

Because I'm thinking, you know, like... If you do the test with Anyhealth directly, maybe you pay like... 10,000? But because we have volume, maybe any health, they give us discount 30%. So we can still sell 10,000. So it would be the same if you use our app or if you use Enhel, they'd be the same price for the customer. And our margin would be hidden. And then we have the AI interpretation, so obviously...

Yeah. People keep renewing.

30 to 60% margin, is it going to cover enough? If it more volume then yeah, it's good.

Yeah, I think the cost, So I've done some calculation. We think in Bangkok we can get So the market size is around 100,000 potential customer. Um... So that's a pretty good number, 100,000, you do it easy. But that's like after many years, you know, when we are successful. And let's say per year, 30,000. That's 3 billion baht. Divided by 35. That's $85 million. But that's the total market size, let's say you get 10%, so that's eight million per year.

300 million bats per year. That's why I say it's like for a startup 300 million baht is good. That's great. But for a big company or even a hospital it's too small. They don't want to, you know what I mean? Yeah. Cannot justify the investment.

The passing power is not that high. You don't own the...

I don't own anything, it's all digital.

So that's why I'm saying, I think, so right now, as you can see, I'm working on all the pieces just to have the full picture. And then I'm gonna make a prototype. So I think next month should have a prototype and then I'm gonna start testing my friends and you know whoever want to try. And then if we see the feedback is good, people want to pay, then we raise money full time, let's go.

I believe the concept of personal lifeThe first one is this. Something. I think that drive more people to do the lab. And also you can get like someHow did you know? Other than the lab?

Yeah, more revenue. Yeah.

More revenue because the...

And the supplement is 1-100% margin. You can do it yourself, like, I mean, like... As long as you have some French cleaning Mejia desuThe supplement need to under the medical license?

Yeah, they need it, yeah.

This is something we're seeing like actually Dr. Chabapan has a lot of good advice on this like So apparently one of the biggest in Thailand is called Max Max Life. And But same as BDMS, they mix the powder themselves. Which I think is very expensive.

Yeah, and they don't do this, Carl.

Yeah, so I think What I would prefer to do is repackaging. So we buy the multivitamin and we just make the sachet, right? We just make the pack like Vitalab, but we It just repackaged. So you see like maybe some of these pills they make themselves with Max Max Life.

We can use other on the miasma.

Not that have to use the macadamia.

Right, I mean, ideally just repackage because it's less cost, right? You just buy multivitamin from iHerb and then you just open the box and then you put them in the sachet. You know, it's a lot cheaper. Because mixing powder I think is very expensive. It's too labor intensive and you need the bunny suit and it's too complicated.

But anyway, this is for later.

But it's not going to be personalized.

For the vitamin, no. You would get a multivitamin.

But I understand that for something like finished product, like omega 3, you're not going to mix any of them. So the omega 3 and some other things you can repackage.

Even the vitamin, if you use a multivitamin, is it really a big deal? I think it's fine, no. But...

Another thing is that We don't have the pharmacist Ourself? So to buy The supplement from iHerb and then mix it. We have to have the...

Yeah.

The other lab that do the supplement, they already provide something like this. Right. When I... When I meet the subordinates by myself with an outside company, It's cheaper. and it doesn't cost that much.

Okay.

You know, like if you have to pay 7,000 Thai baht every month, Instead of like getting that little supplement that you get it's a little i think this is a ripoff this is 7 000 per month yeah so expensive yeah yeah look what i'm getting like six p.m seven p.m yeah It's not about the feels, but when you say the ingredient, it's... Very small.

Yeah, 5 mg of zinc, thank you.

But for male, if you want to maintain 10, 15, 20 milligrams of zinc, but the thing is that what Max Life is superior than other companies, maybe they have more premium. raw ingredient and then put it in That's why they cost him more. Same with BDMS. Yeah.

You mean like the, yeah, like...

Yeah, we call it from here. Pan-X, Ginseng, things like this, right?

You may have mixed this. in BMS maybe two tablet for the customer and another four tablet for No. Two tablets for customize? What? Oh, okay. She gives you the arginine 2000mg so that's already 4 tablets Why she give you fuck? Sorry, where's the Ajin?

Oh, yeah, yeah. No, one capsule. It's not possible. One capsule, one capsule, one capsule. I mean, I think this is... It's not possible. 2 grams.

Yeah, 2 grams cannot fit in 500 grams.

Oh yeah, you're right.

Yeah, so it should be maybe this one, this one.

And these two or somethingIs it hard to, like, the package, is it hard toTo take it out, or is it easy?

It's alright. I think it's pretty good. The packaging itself is pretty good.

I believe that this 4,000 is costing the Yeah. Price, if you do it, maybe $2,000 to $3,000.

But is this Max Life?

I mean, there's no way to know, right? No. It's not Max Life? No.

I guess we can find out. Yeah, because it's VitaBoost and also they changed the company name, it's so confusing. You see, because it used to be Covita Boost and now they named it Vitalab.

Which one is it, you know?

But anyway. I'm going to leave the baby here. He's always curious, "Papa, what are you doing?"-Cool. It's a good idea.

I think that's it actually. Not even an hour and a half. Other than business, what is your outer plan? How did I do this? What do you mean? Do you have any other focus right now?

No, I'm full time on this. I really like the medical field. I think it's pretty Because I think with AI,'Cause originally I was just doing blood tests and everything. For me it's more like a hobby, like biohacking hobby. But I feel like now with AI, it's really It opens new possibilities, right? Yeah. Like now people ask... which test should I do and then they go to PathLab themselves you know like Before, it wouldn't be possible.

People would never go to the lab because it's just too complicated. But now with AI, I think it's a whole new... Like the industry is changing. I think the wellness now people do it themselves. Yeah, and they also want to use a for interpretation and And so I think there is an opportunity to package that together. So, I mean, I want this for myself.

I honestly, I just want to do it for myself.

Yeah. I mean I'm open to, I also have a friend who has a clinic called Manscape. I'm also talking with him to maybe do something together. But for him it's different because he already has a business so he's not looking to do something too... Too new, he just wants to improve a little bit. The way they manage the patient data, for example, right now is a bit messy, so they want to do an internal system to manage patient data and stuff like that.

That now?

You want to do it now? Yeah.

But yeah, anyway, it will still be medical. I really want to do it.

The wellness in Thailand is going to change into more retreat. Yeah, other than this Yeah, but other things something like ice bath sauna, yeah, then some other thing is more hot way Yeah, you can't like using the fitness.

Yes I use a, I'm a very big fan of So now I used to have an iPad at my place. Have you tried before? Yeah. So I used to have a alice bice in my homeWhat do you want to do every day? Um, I think it was a bit difficult to maintain because the water gets bad so you need to put the chlorine in. I was like, it's too much work. Yeah.

But so now do often Mm-hmm.

You guys are outside at home? Yeah.

And now I'm about to start Paddle. You do tennis, do you do padel? Not yet. Because it's getting very popular. I think so too, yeah.

My friend also, like last week, he He told me to join him for a party. Yeah, but it's too late, like 9pm. And the body of the corn is like...

everywhere in Bangkok now so many yeah so many and they're opening more and more there's one I mean there are multiple around here Have you tried it? Not yet. But I have a group of friends we used to do badminton together. And now a few of them switch to paddle So I feel like Padel, I don't know how to pronounce Padel.

It's from Mexico Right.

So if you switch to pedal And so now I have two, I guess. No choice.

So you can get something other than the gym.

Yeah, Mocah Joe. I need Mocah Joe. I was raining for a while, but I think the sun is too strong. 'Cause I don't like running indoor. So I go running at the park. I got very tired then, yeah. I got really nervous, I was like "ok, that's too much sun, I'm gonna get cancer" So I was like "ok, I need something less outdoor" so padel, you know what I mean?

If this product You asked me if I really want to use? Yeah. If I'm not part of this, also maybe using it? Yeah. Part of what? I mean like if somebody else doing this, maybe I will subscribe. Still use it, yeah. That's good, that's good. Because like you can compare for the fitness. Every year you have to pay like 20 or 30 thousand. For the gym, yeah. For the gym. Yeah. And now like if you have like 20,000 let's say.

20,000. then it still makes sense to do the lab.

Would you do the blood test, would you prefer once a year or twice a year?

If you have more information and if you want to do Twice? Ah, twice? Like every four months.

Yeah, I think function is smart the way they do it is they do one major one one minor andSo they have two, but the first one is more test, and then the second one is less. I think it's good to at least get the ball rolling. I keep people, yeah, so they show like cholesterol 2x, so they do every six months. This one only one time. CRP also, yeah. Applebee.

Hmm. This one I cannot find actually within hell. That is, I saw.

Oh, you saw on my website, right? Panel builder ApplebeeOn the quest.

I know, that's it's own quest. I can have them.

Let me check on there. No, but my app is also not... I don't know if it's a bug or not.

Let me check, library search. Oh yeah, here hereYeah.

What's the difference? There's a boy A1 is a good guy. B is a bad guy.

Is it...

So the one... Oh, it's only $200, but... Thank you. Where is it? Not working. What? Oh, okay, he's here. Yeah.

So the top one maybe they do both in a package So it's only 800. But if you do it separately, it's almost also like... And how does something?

In lab, out lab, yeah this is...

Okay, so it's pretty cheap. It's not that expensive.

Yeah, so things like this, you know.

A lot of people have high cholesterol and a boobie is gonna I'm going to tell them the difference that they should take medicine They should be concerned about their platforming, right?

This is also something that's not available in Asia, Grail cancer test. Oh no. So in Asia, I think it was a Singapore company Let's do something similar cancer Why so many?

cancer test What did they do for the crab?

So, Grail is a separate product. 55 It's um...

FD approved, where is it?

Yeah, the gallery, the big gallery Okay, 50 type of cancer. So, three? Yeah.

Um... We do sell free, but we do only 10 times.

Yes. Do you remember the name of the brand?

I saw something in Thailand. I think it's a Singapore company, right? Spot mess.

Something, okay.

Yeah, we do spot maps, yes. How do you spell that? S-P-O-T. Spot. M-A-S.

Is he CP? No no no Cancer...

Early detection, yes.

Screening, ah, here are you. Stool DNA, cancer screening, no. Stool, I don't know, please.

Prostate cancer screening? No.

Room temperature But this test is...

Oh yeah, yeah, yeah. Spot mask here.

Spitmas is 16,000. Wow. Yeah, crazy.

and you know this thing gonna make Ready? What'd you say, like... Some people will go even like curious and maybe like I have some bad impression because one of my friend The accuracy of this one is 60%.

Oh yeah, that's not good. 60, 63%.

That's not good at all. Yeah, so a lot of false positives, what are you saying? Yeah. Yeah, that's not good.

Stress you out for no reason.

Yeah. And Gateri? Wow, this one has very low full space. Yeah, so gallery is great. Very low force but yeah so we don't have this in there's no Asian equivalent so we cannot do it I think.

There's no need as of now. If you later maybe even have better taste you can do that.

Yeah. What do you think I should do?

But yeah, just finding... Bringing functional health to Asia is not easy because a lot of things are not available here. So we need to adapt a little bit.

But I think we can still make good product.

Yeah, that's the basic one. The basic and real estate.

It's okay, we're not competing with functional health, we're competing with... Ourself first.

Yeah, B&H, BMS, you know.

Yeah. Yeah. That's already big market. Yeah. But the main... But too bad that the main... The main people that using From BDMS it's still foreigner like Middle E? That's the main climb. The US when they comeBecome more and more because the--You mean the cancer or just BDMS in general?

No.

Checkup. BDMS in general.

Okay.

And also, Bam Lam Lad is also a foreigner based. [[bnh-hospital|B&H]] is more Thai based. But that's not still the number cannot compare to BDMN.

I think a big concern for Ty is the value, right? Because Thai people, they can go to a clinic outside of Bangkok. Yeah. Where it's very cheap. It's like, okay, it's just one day, you know? I can drive an hour if I get half price, you know?

And they still have belief? That going to the hospital is more reliable than going to the clinic and do the blood test. So I think You can say from election.

Too bad. 500 baht is only tax, yeah? Only 500 baht and you can just get the vote. Yeah, that seems pretty crazy. Do you believe this, that they pay people?

You have to grow up.

Love, Klaus. Yes.

I saw the It's like Bangkok orange, like it seems like Bangkok majority and also Chiang Mai orange and then rest of Thailand is... Not orange.

Yeah. Too bad.

Yeah. All right. Ta-da! This one has a... Benefit, because the blue Yeah. If they still can, they also... They cheat a lot, but they... Make the company. To grow also.

Business good.

Good business you mean. Yeah.

Yeah, let's see. Maybe...

Anyway, I can't, you know, it's not my country, so I don't have a say in this.

But as for Thai patients, I got more Thai agent more and more now. And some of theTime. When I told them that we have nurse Delivery to do the blood test at your appointment. They're starting to, oh, okay, if you have that, then...

Oh, they prefer not to come.

Yeah, because it's very time-consuming to go to the clinic. Yeah, yeah, yeah.

And they don't want to, like, wake up in the morning and drive to the hospital and then...

And fasted because you're so hungry, right? Yeah. So hungry, I have to drive.

Yeah, yeah.

-Yes, I was also skeptical. So usually I go to the clinic and with Vitalab is the first time the nurse come. So I was a bit skeptical. I was like, oh, what if I faint? And you know, it's only me and her.

Actually it was great.

Now I'm like, oh I never want to go to the clinic again. It was really good. Just come, take my blood, take you, go home. It's so fast.

If you have to come, have you been met technically? My technical is... Better in blood draw than the death.

What is the, the medtechnical?

Yeah. What's that? Medico, technical. It's another view People that do the lab Yeah.

Is...matic.

So when I go to Path Lab, the person taking the blood is a med tech? Med tech.

When you go to inhale, The person that took the lab is med tech also. Okay, but what... Not the nurse.

And so the better you think, the better. And at BDMS he was a nurse as well.

BDMS.

For the IV, we use NERSC. For blood draw, we use methane.

The lady that took my blood when I passed out.

No, that didn't happen.

That was Nociano, because she missed the vein, yeah. It's okay, she was nice. I'm not going to blame her. She missed it. Yeah. The nurse it depends right sometimes is really good sometimes is not so good like the one that came to my place She was really good. Yeah I couldn't feel anything. She was really very straight, got the vein right away. Good idea, good idea. And so you believe, yeah, so... Because I think if I'm leaving, it's not just Thai, I would say it's like people living in Thailand.

Yeah, because I think foreigner, Like medical tourists or whatever.

They don't know the price. You can also plug in. with the service.

with the hospital with the hotel with those yeah because they don't know they don't live in Thailand they don't know the price so I think it's easy to cheat them and I think a lot of hospitals do that but I think for people who live here they know the cost they know the real cost and I think that they want something that's like good value you know so if you like look and health It's gonna cost 10,000 and we do it with the app for like 11,000, you know, it's good value.

I think it would be easy to convince people.

I proposed the hotel Proposition for decline. Uh... A lot of hotels now, they want to do the wellness industry. They want to get into the wellness industry. They start with sound, spas and other things.

SoOkay, I saw BDMS is doing a mega complex, BDMS complex or whatever. Yeah.

I don't understand, what does that mean, hotel wellness?

They're not doing the hotel, they're doing the Leslie Danes. Okay.

And why is BDMS has to do with this?

They want to expand into the ultra luxury again in the wellness.

Yeah, in longevity.

Even the hotel?

Yeah. Downstairs, it will be like complex, like malls and other things. Upstairs, there will be residency.

Okay. Yeah, maybe some hotel, maybe 20%. But down here, they... They want to, they do the hospitality now. They want to expand into more hotel or maybe like...

But how does BDMS make money with hotel? So they sell what? They sell the IV drip or they sell the... Doctor consultation.

I believe it's gonna be the same concept with those who come to Bangkok, to Thailand for retreat.

Because Movempic right now, BDMS Wellness is working with Movempic. Yeah, it's actually the same company. So do you have people who stay at Movempic only to come to BDMS Wellness? Not that much. But we have. And so the package, what does it look like if they have like hotel plus wellness, like what does that mean?

Three days, four, five days, or maybe one month, two month. To like the wellness plan episode so they do like their time flying.

Yeah, they maybe like have their meal prepOh, so the meal is made for them? Yeah. So they come with a goal of weight loss or something like that? Yeah, yeah. And so do you also give them like maybe they have already some other things?

Yeah, right. So they come to say for a week, okay and then just walk to the clinic to do something. We have some activity that they can do.

What do they want from the clinic usually? What's a common package they take?

The last time, it's not that wide open. It's also not that much client. But the last time there's one client, Stay in Moen Peak and Venice for two months He come to do the... Weight management. So five days he come for the gym and some some massage and stretching and other things for his condition like the muscle and the... Good. Other day like some facials Aesthetic some other things Yeah. Spas. Yeah, he's a--Leap is like a...

Between The concept is good, but the thing is that it's pricey. It's like you buy other applications from the hotel. When you go to the hotel, some hotel offer executive lounge that you can use every day. Yeah, and all day.

Have you seen BDMS has like some phuket? Yeah, C-Pangolin, yes. And so what's also I'm curious about this. So is it a normal hotel or is it only for BDS customers?

It's used to be the hotel. And now we plug in with them Right. So the client that come to C-Pen Wall And if they want some more medical or some Some blood test, they can add in like plus the service. I'll be there, mate. At the hotel. People do that?

So you see for them it's just a normal hotel right? It's just a normal hotel and the clinic is trying to upsell them medical Yeah. What's up?

You know, you know, Equinox.

Yes, in the US, right? It's like a luxury gym.

I heard they're gonna bring the Equinox to that project.

I would love you to do it in Bangkok already.

I love the luxury gym in Mecklenburg.

But it's... Improves still. I think it is good, but it still can do better. Yeah, yeah. I think the food especially, in US, a lot of the gym do meal prep. Yeah. And here it's very difficult to find. No.

In the US, those who exercise, they got paid. Yeah, to the exercise, to the athlete, right? But in Thailand, the athletes got very little pay.

Oh, you mean there's so many rich athletes. Those are the customers for Equinox. In Thailand, athletes don't have money, so...

In Equinox, they also have like Mario Clinic. Yes. In Equinox. So there's Autopilot out there, Assembly have that there.

Yeah, so as an entity you just spend the whole day there. Yeah, yeah. I see what you mean.

So I believe that's what they're aiming for in for the BDMS and The Latin residency.

To bring some kind of athlete over.

Because like, we now like uh... old population now. Maybe some people want They have money but they don't have someone to take care of them. So they can plug in the medical into the...

I see. It's more like a luxury... Retirement house.

I get it, yeah.

I get it. I mean... I want the same when I'm older. I'd rather be in a luxury BDMS condo than a retirement home, right? That was great. Do you know the name of the event you're going with Dr. Chawaphan?

You can search NUSOh I see it.

And longevity.

Oh I heard about that one. And you're going with him? Yeah. So like, you're gonna take your,Playing ticket together and everything?

No, we booked separately and then yesterday I talked to him. He said that the last week he not gonna be in So I asked him, are you going to Singapore? Yes, so we accidentally booked the same event.

Yeah, he seemed to be... There was also an event this week. There was an event at the Empire Garden. But I look at it, it doesn't seem...

Not this one. Yes, sorry, I just... What did I tap? Brake acid test And yes, longevity in Singapore, I've seen it. Yeah, that one.

Yeah, and then academic for healthy longevity. Yes.

Oh yeah, save the date.

That's the whole event for that. I only went 26 and 27.

Yeah, I'm considering. I want to go to some event, but I think I'm a bit early. In my project? Like what are you looking for, for yourself?

Like where are you going there? Every year, we find Yep. At the same period, in Thailand we also have the event for anti-aging. Yeah. Yeah. But I went to many times already and I think it's the same, same, same. I want to keep updated on something and I want to know what Singapore is doing. So that's why I'm I want to go to see myself. What are they doing now?

Like the new technologies or what they're talking about?

Yeah, what they're talking about and because Singapore is also the hub for foreigners, so I want to get what they do and the NUS is one of the top universities in the world. From the expert I want to see but they're quite conservative actually they're quite conservative they don't do much of the other alternative things maybe we do more than them yeah yeah Last year my friend told me that they're still talking about NAD Plus.

It's already old now. Nobody does that anymore. It's past. Yeah.

I'm not going to say it. What did you say?

Yeah I was curious but it seems that there are already so many events in In Thailand You should go to a steakhouse. Um... So let me see the health tech event in Asia. I have AI doing research for me. It says so many in A-so yeah, this is Texas. Texas. Texas Baseball Tech. International Healthcare. Um...

Another thing that you should do is You want to see the product and what to do in China?

I'm thinking about this eventually, I get to X.

Yeah, I'll take that. I'll take X. LSA, I'm just Global Wellness, Phuket.

I also have a lot of Singaporean, Korean patients. They come to Bangkok because they say it's a lot cheaper. Even though you say the BDM is not that cheap compared to others, but Singaporeans say BDM is still cheaper than in Singapore.

Yeah, there's a lot of regulation. There, makes things expensive. But yeah, basically the... There is Already like a few good events in Bangkok so I was like okay, you know for this because I'm so early stage and I think it's pointless Another I want to go to LA.

At the end of this year. LA? LA, like Los Angeles. Oh, Los Angeles, right.

Yeah, they saw the best anti-aging conference over there.

Yeah, I want to go, but let's see. I have some plans. This year I... I'm gonna see if I can expand My work feel to other things. And then... Like what? I'm gonna do something else other than effort I'm gonna do some plan to do some training right but now maybe I'm gonna focus more on investing in some other things.

Because now you're still working five days a week for BDMS, right?

Yeah, like only five days in a year, they have a lot of time.

That's good. No kids, you know. For me, five days is all I need.

And the Bangkok hospital in Lai Yong, do you know Lai Yong in the east part? They offer me like if I want to do maybe my salary comes down but I can work four days. I have a Rayong.

You have to get your Rayong every day.

Yeah, but my hotel already.

So you would just move out of Bangkok?

If this year Yeah. Everything is good? Yeah. Then if I don't need to go to the clinic or working in Bangkok anymore, then I move back maybe one or two years later. Okay. And I want to... My parents had an idea of maybe gonna do something like live with them and yeah Just bring them to Bangkok.

Easy, right? Yeah, I can see.

Hopefully, because you know, when we talk about politics, the government now, They have some project in my hometown. The new protein.

So you think there's going to be job opportunities? Maybe. International Healthcare Week, this one looks pretty good. in July.

This is next to my home. Yeah, a quick Quincy rickety, very easy. Yeah, let's see.

I think Because for me going to this event I think is mostly for a fundraiser. So I think when I fundraise I will go, especially Singapore, Hong Kong. But, uh, we can wait.

So what do you think ofDrive-up protocol is gonna come up. I mean, I'm going as fast as I can, right? Yeah, you're one person working. This is already fast. Thank you. But if you want some more information about InHeal, I can ask for you.

Yeah, that'd be great.

Just, I mean, I mean, you can be the connection point, right? Just ask them what... I mean the discount is number one right like how does it work to get discount I mean obviously they don't want to tell you because they don't want people to know I think but no I can't find someone to talk to about it yeah so just like how the pricing works I think because for this business pricing with the lab is key I believe that they have their Yeah.

Right. I believe that they're going to talk about the late for the clinic first.

Right. That's okay for clinic. I mean, Dr. Chiawaponi is Probably okay to use this clinic. He has a clinic already. And I also have another friend that also has a clinic. So we can use their facility for the legal stuff. And then it's about, yeah, so costing and maybe ask if they have, do they have API to get the result? Because right now I extract the data from the PDF, but it's not great if they have their own API that can give me access that would be better.

So again, ask, "Do you have an API?" "Yes." And they're probably going to say, "Okay, we only give API if you can guarantee us one million baht per month or something like that." They probably have some condition, so it would be nice to know. I can send you a resume. what I would really like to see from Enhelf. Just like a few bullet points.

Yeah, because I quite... I... last year I don't know why, but I'm working a lot with the inhale.

That's great. Yeah, and then...

And then some other things For the sub-feminine it's already easy.

I think what's blocking right now is legal. I'm working with a lawyer but he's quite I'm a bit frustrated, so I'm thinking to hire a second lawyer. Mm. Just so I have like more bandwidth. Um... So I don't know if you know any lawyerThey know anything. They get that.

Yeah, lawyer with expertise in medical.

That'd be great. Um... I can hire them tomorrow if they're available. So that'd be great because we need to know all the legal implication because I cannot take people's blood right now, you know? without knowing what I'm getting into. And then after this, so this is what I'm waiting, right? After this is done, Because I told you I've already committed 3 million baht so... We have funds to do all the development, it's no problem.

It's more like, you know, step by step making sure everything works.

The detail is that the lens cannot do The medical procedure outside hospital or clinic. Yeah. Yeah. But the mid-type. So I believe that the weather lab They use minting.

Sorry, so you mean... Nurse, so you have to come to the hospital if it's a nurse. She cannot come to your home. Only a medic can. And I'm guessing they're more expensive. No. What's the difference between a Metacanonist? Just the title difference.

Last, when I did the When I hired Medtech to do it, Is casting a little bit more than nursing? Yeah, but... For one day, $500 or $800, depending on...

And so you say, you know Dr. Chawapat, so what's your opinion? Yeah, you say he's like pretty good in functional health. He seem passionate about it. Yeah. But he seems to be really focused on Wait, Luz.

I don't know, maybe... Everyone can do weight loss. Yes, I think. Even you.

Calorie restriction.

Yeah. Even you. Everyone knows about weight loss.

Pretty simple.

Yeah, but the main thing is that he, like if you want to talk more about like the approach. Yeah. You have to see the mindset that is it the old or the new approach that you know and It's like you have all the weapons that what you should to do.

But what would be the difference between a doctor that you think is like old fashion versus new fashion?

The old-fashioned is... You're gonna see the same man, Tom. and But the good thing is that you have to see that are they good to handle the expectation. Right. Yeah, that's the main thing.

I would say like old fashioned they would not do functional health or longevity Maybe not too much. More like, you know, like, okay, only disease prevention. Only, uh... One, two, three. Yeah, like, how do you say, conventional medicine?

But I still believe that he is so flexible, but not as flexible as me. Flexible what? Flexible on the treatment, on the approach. Kid. Why is that even happening?

A little white. Great, yeah that was great, thank you.

What other things that you need?

I think it's slowly. I think right now I'm just making progress and so I like to have like doctor's opinion on some things, you know, kind of like guiding me through.

I also have a friend in the software engineer actually. Yeah, he used to work in Akrona.

Oh, that's great. Is it Thai? Thai.

Oh, that's great Maybe get off, maybe like, blah. Almost five years already. I wish I was that good.

Now you're freelance. What does he do? Like when?

I don't know now. Like what? Maybe he only worked for the project like one year One by one. Not in the main. Comedy now.

How old is he?

Same.

We are the same. Do you think he's into like Blood check? Does he do a check up recently? Yeah, good question. No. No.

I think it's good like If you have someone to say my side, so it's more easy to talk.

I think it's I mean obviously I don't want him to be an expert but at least he sees the interest in the product now. Because sometimes I talk to people and they're like "Never done check-up" so they're like "Okay, I don't care about this product" you know. But yeah, I can talk. Ask him. I mean, if you think he would be interested, then I'm happy to talk to him. I'm also talking to one other... So I'm talking with two software engineers, but one of them never done bot tests.

Doesn't care, so I was like, okay, you know. One of them does and he's very interested so... I keep talking with that one. But that one is very difficult. He's very smart. And right now he has... Very high paid job. So it's been, I think it's going to be difficult, yes. I'm trying to get him but asking for too much. He asked you to watch No, he didn't ask me, but his current job is pay the 700,000 baht.

I was like, okay, that's a lot.

So we'll see. I think already doctor is How many doctors do you contact now? Just you two. You and Dr. Chalapon.

Yeah, I say let's just meet, you know, we can just talk.

Because it's not just... I mean we're just talking now right so yeah yeah Maybe some doctors are interested to join as co-founder. Maybe some inductors just want to be advisors. Like for Tocco Chacondo, you can be just advisor. Just meeting, like maybe we have a video call once a month, you know, you just give us some opinion. You can also be investor. Which one? I think maybe she misunderstands. She thinks I want to join.

I don't know. It's okay, I will ask you again in a few months. Because I think yeah, I think it's a medical project so it's good to have.

Another thing is that for especially for question card maybe like you do first And then... Maybe if she interesting later then she come to you. It's better.

Do you think maybe she wanted to play it a bit more advanced? Yeah Maybe it's too early.

Yeah.

Yeah, I think so. But, let's see. No, because also I mean she she helped me so much actually she introduced me to you she introduced me to Dr. Charles. So I also I'm like, okay, you know, like you helped me so much already, you know, I want to have I want to have you as advisor or something.

Yeah. She I think she wants to Help?

Help. Yeah, that's great. And even, yeah. Cool. Okay How do I stop the...
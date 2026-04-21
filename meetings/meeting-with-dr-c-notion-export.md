---
type: meeting-notes
date: 2026-02-01
source: transcript
tags:
  - biomarkers
  - lab-testing
  - product-design
  - blood-panel
people:
  - art-chawapon-kidhirunkul
  - nick-warot
companies:
  - bodycypher
  - bnh-hospital
  - vitallife-by-bumrungrad
  - bdms-wellness
status: raw
---

# Meeting with Dr. C

Date: February 17, 2026
Created by: Guillaume William
Summary: Guillaume is tasked with researching optimal ranges for CRP, triglycerides, and vitamin D, modifying dataset visualizations, and finalizing blood test panels with InHealth. The meeting discussed lab selection in Thailand, focusing on pricing strategies and the reliability of labs. Key points included the importance of distinguishing between reference and optimal ranges for biomarkers, product design considerations, and competitor analysis. Collaboration with Dr. C was explored, emphasizing flexible scheduling and access to a clinic network for patient referrals.

Summary

### Action Items

- [ ]  Guillaume to use AI agent to research optimal and clinical ranges for CRP, Triglycerides, and Vitamin D
- [ ]  Guillaume to modify NHANES dataset visualization to show age/gender-specific ranges and rename "optimal range" to "observed range"
- [ ]  Guillaume to finalize blood test panel selection with InHealth and get clinic pricing
- [ ]  Guillaume to review micronutrient package options from InHealth

### Lab Selection and Pricing Strategy

Discussion focused on selecting reliable lab partners in Thailand for blood testing. Key labs discussed included InHealth, Bria, and [[vitallife-by-bumrungrad|Vitalife]] (Bumrungrad Hospital's lab).  Important considerations included:

- Price comparison across multiple labs to optimize costs while maintaining reliability
- Concerns about some smaller labs potentially manipulating results
- Clinic pricing typically offers 20-25% discount compared to retail
- InHealth was identified as the primary lab partner, though Bria offers better discounts but is farther away

### Reference Ranges vs Optimal Ranges

Extensive discussion on how to display biomarker ranges to users, a critical product design decision:

- Reference ranges from labs are based on statistical distributions from mixed populations and may not account well for age, gender, or ethnicity
- NHANES dataset can be used to calculate age and gender-specific "observed ranges" from healthy populations
- Optimal ranges should be defined separately for each biomarker through medical research, not just statistical analysis
- Both normal range and optimal range should be shown to users so they understand if they have health issues versus optimization opportunities

Key examples discussed:

- **CRP**: Optimal <1, Normal 1-3, High >5, Critical >10 (indicates infection rather than inflammation)
- **Fasting Glucose**: Optimal range remains constant across all ages (75-85), even though normal range widens with age
- **Kidney Function (GFR)**: Must be age-adjusted as it naturally declines with age
- **Vitamin B12**: High levels don't always mean optimal health—can indicate stomach or immune problems

### Product Design and Competitor Analysis

Reviewed multiple competitor products including Kiro, Ornament Health, Health Matters, and others: 

- Health Matters identified as having well-validated reference ranges and reliable reporting
- Best practice is to show both normal range and optimal range with clear visual distinction
- Product should include organ-level health scores in addition to individual biomarker results
- AI-generated recommendations should include citations to research
- Four-value system recommended: Normal Low, Normal High, Optimal Low, Optimal High
- Some markers also need "Critical" thresholds for dangerous levels

### Blood Test Panel Design

Worked through designing a comprehensive test panel using InHealth's catalog:

- Started with Function Health's panel as reference baseline
- Included: hormones (testosterone, thyroid panel), metabolic markers (A1C, glucose, insulin), inflammation (CRP), lipids, liver function, kidney function, electrolytes, vitamins, heavy metals, omega fatty acids
- Estimated retail price around 30,000 THB, which would be ~20,000 THB at clinic pricing
- Micronutrient package from InHealth costs ~5,000 THB and is comprehensive
- Final panel considered very comprehensive—includes tests rarely done in Thailand clinics

### Collaboration Discussion

Discussed potential working arrangement for the [[bodycypher|BodyCypher]] project:

- Dr. C currently works 3 days per week at [[bnh-hospital|B&H]] (InHealth lab partner)
- Schedule is flexible and could accommodate BodyCypher work without requiring full-time commitment
- Access to clinic and hospital network (Bumrungrad) provides referral pathways for patients
- Both parties agreed to start collaboratively and determine formal arrangements once product gains traction

Notes

###

Transcript

When you check for sale count, like complete sale, red sale, white sale, was some small lab companyAh, beep. Don't use your own lab, don't use your own result, they just random the result. Really? That's like scam.

That's the dark side.

Like, would Bria do that? I'm not sure at the moment, but in the last couple of years, there's still some small company doing that. We cannot prove but we know it's what's happening. So in terms of price, we have to make sure it's not too cheap. Because if it's not too cheap, it's like it's a sign that it's not a good company. So in health,It's Trusted Lab, B-R-I-A. Bria Lab you think is the bigger, and Bria is cheaper than Enhel.

cheaper cheaper and they have their own maps too so it's reliable Anything else?

Which one should I look at? Because right now we are about to look at N Health. Uh...

I think just two is enough. Do you want to compare all of them or you want to just try one? Because it can be like this if you want toLower the price as much as you can. You don't have to send out to only one lab. You can send out to a different lab. You can compare the price and choose either this one you send to a rare lab.

You mean for part of the test, right?

Some part of the test? Yeah, you don't have to send it to only one center.

Yeah.

So if you want a little bit more convenience, maybe you have to select only one partner and then use only one lab.

Because I guess also the lab if you give them more volume they also give you a discount maybe?

Yeah, yeah, yeah.

But not always the case because... How does it work to get a discount at a lab? Is it like in terms of how much money you give them or how many tests or negotiation?

I think it depends. For any health, it depends on your money. And then you have to ask them too. Because if you don't ask them, maybe they give you the same price.

But did you ask them for your lab? Do you know?

I didn't send a lot of tests to another company.

So you never asked for a discount? Never asked for a discount. So you just paid the normal price? Yeah, normal clinic price.

Not the sheep, but she did not.

So clinic price is below the... is already discount or no? Already discount.

Clinic price is lower than retail price, but not that low.

But like what? How much are we talking? 10%? 20%? 20%.

Okay, it's 25%. For me it's not bad because I don't care about price that much. Like, my guitar post. Yeah. I, I, I, I focus more on reliability. Yeah. I have to be like very happy that's most important and another company actually Bamrura Hospital also have their own lab. It's called Vitalife. You know Vitalife? Oh yeah, yeah. They have their own lab company. Okay. So you can contact them to compare the price.

Are they good? Yeah, they're good. Because it's the part of for Bambula's hospital, right? So that lab is reliable. So maybe you can compare like two to three companies. I would recommend VRapp. VRapp is good.

I mean right now I just need one to start. Yeah maybe I should have asked you before because I'm going to show you I've already done a lot of work on Enhealth so I think I'm going to use it.

I don't use them very often because it's difficult to deal and they don't give us a lot of discount on that. Obria gives better discount. Yeah but I don't use them also because it's far away from my clinic. It's too far. our lapel area.

Yeah, quite fine. Do they have a delivery service or you need to send to them?

They have delivery service too, but it takes time.

Yeah, because I guess it's fine.

They give but they give very like concise range. They don't give you unnecessary detail.

And so right now, I think I sent you an email, I don't know if you saw. For what? Just ask you some questions.

Oh, really? Which email? Your email?

My email? dr.chauabon If you want, we can just go through already. I think it's okay.

Okay. Oh, a lot of questions. Sorry about that.

It's okay. Actually, I'm not good at looking at emails. It's just for me to not forget, so we can go over now. Yes, so I was asking about the range. So B&H, I think is a better case study for you. So B&H use which lab? InHealth. InHealth as well. And so the reference range, are you using the lab or the hospital has its own? You mean I, personally?

Yeah. I use my own reference range? So when you see the report, I don't care it's the reference which is from my own is from my work I see for example, they may say 10 to 20.

I would say no But that's only Sorry, I just want to make sure so B&H doesn't care doesn't have internal reference range or anything So it's only the lab and health All doctors know that it depends on the context.

We don't need two doctors, we don't need to use the same reference range. It depends on patient context. So that makes it difficult when it comes to reference range in the lab. Of course, you can stick to the reference range. from like in health.

But how does in health get their own reference range? It depends on the labs too. But is there like a Thai standard or worldwide standard or anybody?

I think worldwide standard. But for me, I don't think they work that much on that reference rate. They just pick up like textbook or reference rate that they have been using for 20 years and they stick to that. And then when there is a minor update, they change the reference rate. For me, I think it's kind of like not perfect. different brand even from Intel. They might get it updated more frequently when you compare with other companies but it's still not Not only one reference that you can rely on.

Have you heard of the NHANES dataset?

And Heng Jiao, yeah, it is a big database. Yes.

For me, So some people use that for reference range.

Yeah, the problem of reference range is Let me tell you about how RuffinRange It's rubbish. Once they do the test, they get the big data. Maybe mainly from Europe and in the US. And then they use the standard deviation and see if it's in the middle, that's a different range. In detail, we don't know yet if it's a reference that can be applied to everyone. because they're like that pool together. from different age, not different, different ethnicity.

That's right.

Yeah, sometime. If we use one particular reference brand, it might not be the Perfectly for us. Okay, that's why in functional medicine some people talk about optimal range.

When you say for us, you mean the... You mean Asian or just optimal versus?

Asian like I and you might have the different reference range. But in general it's not that big difference. That's why we still can use the same range.

Because usually the range is so it's the gender and then the age right? Like 10 year gap or something. Yes, gender, ethnicity.

Ethnicity is important. Yeah, I don't know.

Does the enhanced dataset include ethnicity?

I believe they include, but you know it's complicated. They cannot use differentCool. Actually, it depends. Most different range can be applied for everyone. like blood count, sugar, you know right, sugar is safe for everyone. It doesn't matter where you go. But kidney function, for example. Kidney function, we use different Grinch, when you calculateYeah, they're number. So, okay, this might sound very complex, right?

But in practical, when you get one particular lab. You have to know what your reference range that you would like to use And then you have to know what optimal level you would like to use. That's all. Because you want to focus on two things, right? Yeah. Okay, normal range and half-node range.

Sorry, I'm fighting with this TV. It's okay. I think I'm going to unplug the TV. There's something wrong with this TV. Oh no, this is why I need to get pregnant, see? Misty What's good about working in IT is you can debug.

Yeah, so thatThank you. The different renders you like to use, you may have to do some more research on that for each one, which one you want to use. You don't need to use the rain form in health actually.

You can use your own electric rain.

Well, I really want to show you It's crazy why it doesn't work Actually, it's the same. It's the same... Yeah but this one doesn't...

It's the same TV, right? Same brand.

It's like when it shows the number it doesn't show the pop-up and when it shows the pop-up the number doesn't appear. I cannot... I cannot do anything. I didn't mean to do this. Okay. Okay. That I set on my computer actually. I did some work with it last week. part of the thing I was doing for two weeks. So I wanted to show you some of the work I've done with this. But I didn't know there was ethnicity, so maybe it's something I should add.

Um... So if I manage to connect to this TV at some point... Okay, oh my wait see always reboot Oh my god, yes. And I work in IT. Imagine people who don't.

I have no idea what you've been doing.

So Um... And hence that said let's goMm-hmm. Okay. Uh... Yes, so the range, I don't know if there is like, so this is, these are all of the biomarkers. Um... But then the question is how to Is there one biomarker where the reference range and the optimal range are very different that you want to look at?

Let's look at... Okay, start for... A1C. The second one.

Okay, so P5, P90, this is the middle. So we remove the bottom 5% and upper 5%. And then for example, we can do per age. Okay. So it would seem that compared to Is it different for gender? So this is male, male and then the age.

Not big difference, but a little bit different.

Oh, but you see, the color is really bad actually. So yeah. So it's supposed to be finished here. So optimal range. So it's not really optimal. This is more like the...

Okay, let's look at the A65.

I think it's better we look at my computer actually. The colors are really bad on the TV.

Oh, okay. I don't see the camera.

So the clinical range, I think those are the standard range from the hospital. And the optimal range, so it's not really optimal. I would say it's more like normal range.

Okay, you can... This is the optimal range here, right? And this is the range.

Yeah, but let me explain how I calculated the optimal range. So I took the data set and then I removed the... Patient with some condition. So sick patient. Because they tell you in the data set which one is sick. So then we have like, I think it's 25,000 people. Or maybe 15,000. Not sick. And then you can slice like per age, gender. And so this is more like Healthy patients Normal range. This is more of an observed range.

I think optimal is maybe not the right word for this becauseYeah, then the question is how do we calculate optimal, you know? So, actually [[nick-warot|Dr. Warren]] was like, okay, maybe we take When people are 30, because 30 is kind of like the peak.

Maybe let's look at it as like... Let's see something else so we see more details I believe I saw... Oh, CRP, yep. This is the one. That's the one that we have.

Yeah, so I want you to pin because I want to keep refining this. So this is like the first draft.

Okay, let's see the range. So optimal range is the same right? Okay Okay, you will see that actually my optimal rent, I normally use less than one. So I can say that this might not be at the really optimal range. It's the normal range. Yeah. It's the normal range.

But how do you know it's one? Like you do some research or?

It's for many, many, many knowledge, right? Some we use In our field that this we use as an optimal range. Some we have It's a bit strange from the research show that this is optimal. You know, not every lab we have optimal range and not Optimal range is valid. I think this is a good start because this is the problem in my field too. Sometimes we use optimal range in the way that too tight, too strict, it's not necessary.

But sometimes we use the reference range that too wide.

So you mean, what I calculated in red could be a replacement for the reference range? I don't think it's optimal. I think I want to change the word. This is more observed.

Observed range, right. Optimal range is not the way we use optimal range. I think this is normal range. Healthy range, something like that. Healthy range. But you can refine it a bit more. Like, okay, this is the range, the healthy range. Move back to one side is optimal you can use that kind of thing So for some marker as low as possible is best Yeah for some marker for some marker as high as possible some marker need to be in the middle So optimal range is very individual.

It's different.

Okay, so so the way we would do it So I'm trying to I think normal range from in hand.

I think it's pretty good so you can extract normal range and update it if needed. Normal range is very easy to get because you can get the dataset. But for optimal range, you have to work maybe like God. Separately, okay, we cannot extract one data set from one. It has to be one by one. Yeah, it has to be one by one. Maybe we need to do some more research on that too.

So what do you think we could do with this enhanced data set?

I think enhanced is a good database. Okay, how did you extract that information? Which is data science. Okay, just extract the data and then you You analyze by your own.

So I used to do some data science before, so I know how to use the tool.

Okay, good. Yeah, it looks pretty good. I think this one, when you put it in your apps, it would be a good thing because the reference rate is very validated. I think it's good.

But the question I have right now is, What, how to...

What is PS? I didn't know. P5... Oh, you cut. This is the distribution.

Distribution, okay, okay. So it's... Cut the top five and bottom five. And then what you do is like you kind of calculate the median and then you do one standard deviation. That's how you get the optimal range. But so... I'm trying to figure out if we're going to use this data set or not.

Normally, normally. Let me check.

Maybe we have to... So basically, because the clinical range you see here, so in gray, this is like the... From the Mayo Clinic, this is like the... Like the common reference range like in health use almost the same.

Yeah, I think in health use the same method that you do.

So for ourPredic, would you use enhanced dataset or would you use the Mayo Clinic normal range? Uh. Which you see sometimes is tighter. I think they are comparable. Because this is statistical, so the blue one is statistical from the NN to the Z. Whereas this is like, from the Mayo Clinic they just say, "Okay, the orange is this." Oh, okay.

Uh... Do you have any information for myokinic? We can use another one. It's the same, right?

The gray is like... Like, Ed Health would give that. Oh, okay. Because they wouldn't give per age or per gender, right?

If you can use the age and gender, it would be more refined. I believe it's better.

So, yeah, because right now, so we would cut per, for example, this one, the fasting glucose, we would cut per age, at least.

Yeah. And, yeah, I think each test, we can use different, like, Uh... Not the data set, same data set, but different interpretation method. For fast link code, actually you can use only one. One range for any age. You don't have to worry about the age.

But you see as people get older, the normal range get wider.

If you use normal range, not optimal range, You can use that to see, okay, when you get older, your sugar might be increasing a little bit, but optimal range still remains the same. You know, the cut point for optimal range to remain the same.

So for the fasting glucose, for example, If I was a user, would you rather show the ranges like this and then the goal is to be as low as possible? Or close to 80? What's the...

My optimal range for sugar is 75 to 85. Something like that. So it's not Uh, uh... Not depend on age, okay? Any age, I use the same range.

Yeah, but when you're older, realistically it's going to be...

When you have high sugar, that means you don't have optimal sugar, right? That confirms that it's not optimal.

Is it possible when you are like 60 to be at 75? Yeah, possible.

That's why we have optimal range. But if you don't worry too much about your health 90, 95, 100 is acceptable. That can be still in normal range. But for sugar, actually in medical field we don't talk about age. We just talk about range. It doesn't matter how old are you. It's the same range. This is the example. For fasting glucose, for A1c, you don't have to worry. age. Any age we use the same range.

But for creatinine like kidney function, I mean GFR. This we need to refine the edge because it's different.

So let's do all. So both male and female.

Yeah.

So the clinical range, they say it's 90 to 120. Yeah. But the observed range, let's call it observed, As people get older it seems to be getting a lot lower.

Yeah, so this is something you want high this is the Situation that we accept when we get older we have lower kidney function that unavoidable, you know, right so that why we use different H group, right?

Yeah that we we have to keep it right different a cool for kidney function, but it's a okay Let's say somebody used my app and they are 50 to say they are in this group. Mm-hmmAnd for that marker, what do you think we should show the user of like the range and the optimal value? Should we use the--Both, both. Should we use the 90 to 120 or should we use the 70? Too sure you know what's normal for them?

Depends on their age. So if they have 50? If they have 50, you show. You show the result on their 50. The blue one you mean? Yeah, yeah. The blue. Actually, I recommend you show both.

From NL, NL would only show this. They will only show 90 to 120.

I recommend you show both. So, what I mean by both is like... Standard range, healthy range and optimal range. You show both. So when they see the result, they know they don't have health issues because it's still in healthy range. But it's not optimal yet. If it's still not in optimal range, so they can work on it. You know what I mean? Like when you have good kidney function, not very severe, but it's still not optimal, you may be able to do something to help.

So usually I've seen some app what they do is like they have four okay.

Let me let me show you some functional report.

Yeah, I was gonna say I think we should look at the product I think it'd be easier.

Okay, let me show you some report. Yeah. Okay, this is a good one. This is from functional BX. In functional medicine field, it's very popular. When they show you kidney function here you see they show normal range Yeah. like this is normal range and this is optimal range this is the way they report so when you look at this if you have the problem like here you know that okay you're still in normal range but it's up not optimal yet okay this is the example of okay how to how how to show the the yeah let's see so what what did they show uh they saw something like this they show in the same uh Yeah, bureau standard, that means it's not normal.

But I believe they use this word because they don't want to focus on diagnosis.

Oh, they're not giving the real number?

Sample report. This is a sample report. You don't have to worry about numbers. So I think the reason they use the gradient color like this, not very different color, like red, blue, because they don't want to give the diagnosis. I think it's like playing safe for their interpretation. But this is the way they report. They report normal range and they report optimal range. And I'll show you some other things in...

Okay, let's see some example here. There are another way they report the result like this. So this is number range. Uh, This is normal range. Oh, the colors, yeah. Yeah, this is the color to say it's already out of range. But that would be something like, oh, this one. Okay, you see it's like a sentence, right? Yeah. So... You use percentage to see if it's in normal range, but actually This one and they just get updated.

They show the median right? Yeah median of that case to see what what the median number so you so so you would know from the report that how much deviation You we have from from the healthy or from from the average people, right? Okay, and that tip it's another way to compare optimal and not optimal range you So it depends, but if you ask me what should be reported, Optimal range and normal range should be reported over the kit.

Yeah, like this I think is good. Team XA.

Another one.

Optimal rate would be more important, more... Like useful for hormone test when you use right for normal taste like kidney function liver function Normally we use the same range. Yeah, okay Only kidney function that we used to use different age, but most of them we can use the same way Okay, but when it's come to hormone you have to make sure you use the age.

Okay, the age group very important Okay, let me instruct the A, sorry.

Not just the edge group, actually it's the day of testing also matter.

Alright, okay, one minute, I just want to instruct my AI to change some stuff. Hey, can you help me increase the contrast on the website? We use a video projector where the gray and the white kind of look the same, so maybe Just make it a color for the clinical range. I also want you to remove the P5 P95 from the graphics. I think they're not useful or make it hidden by default and I can click to show it.

I also want you to rename the current blue optimal range. Can you rename it to observe range? I think Yeah, right now it's not really optimal. It's more like observed from the healthy people and clinical range. Um... Yeah, call it reference range. And then... Yeah, just do that and I think you should be okay for now. Oh! Well, what's going on? Bypass permission, okay Okay, masking the... Let me see if I can restore.

you Of course. 10-113-1119 Yeah, it's all right. Anyway, we just do so just like my computer. It's fine. Can't choose your health.

Still updating, right? Yeah.

So we can show Okay, let's look at some Blood analysis is fun. Lab research, no, no product research. So this is still work in progress, I haven't finished all of them. So which one do I like? Now this one that was for the heroOh yeah, I've used some. Yeah, yeah, so Kira, I think this one you're gonna like. So, just to finish on the range. So Health Matters seems to be really popular for ranges, right?

Apparently they have Rang on everything. Yeah.

They use very well-validated reference range, so you can rely on their result. But in terms of optimal range, of course, it's not well-attracted, so sometimes we don't know yet. But normally, if you ask me, when we get the result, what interpretation should we have? First, we have to focus on more conventional. interpretation so the range would be the cut point for Uh... Deceit or not having disease, you know what I mean?

Yes. Yeah, so that's very important. But you give an option of optimal range for one who really keen to Like health optimization. That's why we have two different range.

So I've analyzed health matter and the conclusion I got with AI is thatWe can actually, actually with AI we can easily replicate them. The way it would work is I can use an AI agent for just one marker and to be like, okay, so you are a medical expert and you need to find all of the research paper for reference range and optimal range for that single marker. And they have the AI engine just getting it off source.

And then giving a conclusion. Obviously we need to say, okay, So that's why those are pretty good. So what's what? What some do is they have four values. So they have the clinical range, low and high, and then the optimal range, low and high. And so we can ask the ASL, okay, so for example, I don't know, LDL. I think that should be enough. And then we can have a doctor inside our team to just review, make sure there's no mistake, and they'll be like, yes.

And then we approve those. That's it. That's what we do in the app. So that would be... So the doctor will only need to review the EIA report for all of our marks, so like 100 marker. I think, you know,Within a few weeks, it's probably doable. And we would be basically as good as Health Matters for those markers. Yeah.

I think that's a good way to do that. Because health matters, actually, only one person, am I right, Junior? One person, what do you mean? Full time.

I don't know. It's just one person but apparently they've been doing this for 10 years.

Oh, you do some research on that, right? Yeah. But I think they know pretty well about what they're doing because the report is very good and very easy to understand. For me as a doctor, I I like the report that look reliable. We know what reference range, we know what dataset they use, and the way they report is not too fancy. It's kind of like a standard medical report, things like that. But one thing that's very important in this AI healer, I believe when we can use the range with some recommendation, with some reference range, with some references, that would be pretty good.

For example, like--Can you give me one or two biomarker?

I give you an example that if we don't know, we don't know. For B12. When we test for B12, Uh... Looking straight forward, if we have low B12, it's not good right? We need to increase B12. If we have high B12, Okay, it's optimal. But it's not that simple. If you have low, okay, you don't have enough B12. But in case you have high B12, Sometimes you can have problem Because it's too high.

Oh, sorry. I forgot my driver. Easy. Yeah, it's been downstairs for half an hour. I forgot anything. Oh, okay. So wait here Yes please Okay, right. Yeah, okay, he get them. No. You don't have to go down? No, no, it's okay. So you said B12? Yeah, so...

For example, like when you have high B12, it doesn't mean, okay, perfect, we have good vitamin B12. There's only one concern that if you have some stomach issue or immune problem, you can have... Uh... For positive level. Really high B12, but it's not a good condition. If your interpretation can flag that, that is okay. It's a running sign that even if high, it's inoptimal. But if you have some particular issues, Maybe you have to consult with your doctor to see if it's really good, something like that.

I think I can pick it up very easily because it's the common condition that even most doctors misinterpret the result. Okay. You know, it's like, there are some, one red flag, one sign that, Telling us about that report. It doesn't mean it's perfect. It means it's too good.

And it's not good.

And so can you give me one or two biomarker? Yeah, you mean sometimes the B12 so higher is better, but if it's too high it could actually mean disease. Yeah. And so Can you give me an example of biomarker? where the reference range and the optimal range is not like, I want to try my AI agent to do research to find what I say, like optimal range, and then clinical range. So can you give me one or two interesting marker and then I will send AI agent just to see the report, see if we think it's useful or not.

That normal and-the optimal range totally different, right? Yeah, I think so. I think it would be an interesting one. Let's take a look at CRQ. So CRP is a good candidate for that. How about another one? Um, I know.

Just try two.

Okay, let's make it very simple like try this right Traglycerides.

Traglycerides. You think optimal and clinical are very different?

Optimal and normal range. Okay.

And is there one marker whereOptimol is very, debatable like we don't know Actually, one of them is vitamin D.

Vitamin D, you know the range is Very wide right? Some doctors use this ring, some other doctors use another ring.

So this is a hot topic. Yeah, even I myself cannot answer you accurately. Great, so I'm going to use AI for that.

I think that if Your report can can pinpoint what the the optimal vitamin D level that that we should So what would you want to see?

So, okay, another one I'm showing you. This one, this they have seven, so they have...

This is your mock-up right? No, it's not mine. It's an example. Oh, okay.

Of a product, so like, How many values do we need so let's say value d? Like, do we need clinical and then optimal, so full value, or do you also want the mean, or?

As a doctor, what would--I think vitamin D, the way we report it, it should be a little bit more in detail. Like, if you focus on deficiency, this is the cut point for deficiency. If we focus more optimal, like optimal immune function or mood or sugar metabolism, we should use another So what I was saying earlier was... So make it very simple. It's like normal range. Normal range. Oh, sorry. So we have the normal range low.

Normal range. Yeah, like low normal. And then normal range high. And so if you're outside of this, it means you need to do something. Yeah, yeah, yeah. And then same with optimal.

Optimal, yeah. Normal low sometimes we can say like insufficient. Not low, but insufficient. You know what I mean? Right. Yeah, something like that.

So for So you also you give me tracklist right and CRP. So you think for all three of them, we can use those four value? Yeah. And it would give like a good--Yeah, yeah. Like as a doctor, that's what you want to see.

Yeah, yeah. But in more detail, like when you have critically low or critically high, some lab tests might for some serious problems, for example, like vitamin B12. So when it's too high, maybe there's someSo you mean you would even have like critical?

Critical, right. Like critical high? Too high, it's like too high, it's dangerous.

For nutrition, sometimes we say it's like toxicity, the toxicity level.

And I guess you will have a critical low. Critical low.

Critical low nothing much but critically high sometimes we can say toxicity. Okay. For nutrition, basically for nutrition. And for CRP? For CRP it's very simple. Like low, high, optimal.

Well the CRP is basically zero, right? Like low and optimal is just zero.

Actually CRP also have critically high. For example, if your CRP higher than 10, is not information, it's infection. Wow, okay. So if it's 10, you don't have to worry about heart disease or chronic inflammation. It's something else. It's a cure problem.

Yeah. Okay. So if we see that somebody has CRP more than 10, we will tell them you should go to hospital. Yeah, yeah.

So for me in this era, the perfect scenario is like the client when they look at the report, they can understand their report. As close to doctor They know when it's too high, it's like too high information, but it's flag something dangerous, then they need to go for further investigation.

CRP, so okay, just Just to make it real. Let's try CRP. So yourself, what value would you put there?

Less than 1 is optimal. So optimal is less than 1. So optimal high is less than 1, right? So 1 would be here and if you lower it, that's great.

Yeah, optimal is less than 1. And then normal range is 1 to 3. normal range like normal high is 3 Yeah, 3. And high is 5, something like that.

For example, you can do something like that.

Oh, so actually the normal low would be... Because this test, the lower the better.

So you don't have to worry about low. So when it's low, it means it's good.

So the report would be if you look at CRP.

Wait, let me check CRP from myIf you look at most of the test, it would be like this, you see?

Most of the test would be like this, but CRP would be like this. The lower the better.

So on my, on my, so the database, so reference range is actually zero. Mmm.

No, no one has zero level. I mean, it's less than one. I think the database is not very like Uh, I never seen in my life People with zero level of CRP.

No, I mean I mean the sorry dear.

Yeah, it's not it's not I believe they put the number like when the level lower than point for like 0.4 They say see this is the sorry.

This is reference range reference range.

Yeah. Yeah. Yeah, it can be like that But no one has zero level. You know what I mean? Right?

I Lab research, let's look at, actually, I think let's look at, in health I think it would be easier. CREP. How do they call it? Do you know?

C, that reactive protein.

reactive Creactive yes Sensitivity? No. Yeah, yeah, yeah.

Yeah, this is the one. High sensitivity. 200 baht.

And the range, now storage condition,Oh, they don't give the range.

I think it's just price risk right? Oh sometimes they give you the range right? Yeah I remember I test it every day They use 0 to 1, 1 to 3, 3 to 5 That's the cat point. I think I might have it here.

Inhale, CRP. I forgot if I tested CRP. Is that a common one?

Hmm. We can move. Move.

Actually, you can take that. reactive. It's reacting. No. Oh, nothing. It's PLPDF, right?

It's PLPDF. Because this was a... It's scan file, right? That was a chip. I don't know. I think I just don't... I didn't do it. Oh, it's...

Yes, you have moved on, David. This is something I've done myself.

So it was announced, only five page. This is cheap, I only pay 4,000 for this. There is no CRP or I believe it.

It's here. It's normally is In the immune part, Where is that? Okay.

Repeat, no. Yeah, no. Nice note, see? Okay.

But so for CRP, so what you say, optimal, so that would be 0, 0. That would be 0, yeah. So for CRP, that would be right, 0, 0. And then optimal high as 1, so less than 1 is better. Clinical, this says 3, and then if it's above 5, Maybe a raisin alone? Yeah, yeah. Okay.

Yep, this is an example.

Okay, so I'm gonna try to have AI agent do research and then come up and then try to give some quotation because actually this is good also for content as well that we can publish.

And then in this case, remember I told you if the number is two digits, like 10, we're not gonna use it for chronic information anymore. We use it for screening for infection, CRP. So it means like it's out of chart. When it's out of chart, you have to interpret it you differently.

He's like... And...

I think this is very simple, easy to replicate. But when it comes to hormones, it will be like this. You see? The range, very good. H1 is narrow, it depends on your age. So you have to understand some of the lab tests be like this. When you plot your reference range, for every test actually, it would be like this. If you plot it like this, like, for, sorry. For most of the tests, like CBC, it would be like this.

Like, reference is the same. for the whole life. But some of the tests, the gap of the range, it can be wider or narrower, it depends on your test.

Yeah, so actually, if we want to show optimal, it's better to show this, right?

I think this is the best way to demonstrate the report.

So is there a way you can share this? Can I take a picture, maybe?

Sure, sure, sure. Actually, I just Google it, it's CRT lab.

Can you forward this to me, this PDF? Yeah, sure, sure. to modify my enhanced um just url yeah yeah online okay in terms of nutrition i'll show you like So I can modify my enhanced data set to show this I think. I think it's better. Think is better.

This is in Thailand report.

But B&H doesn't have it. But actually it works, I think it's pretty clear. But at the light, yes.

In this era, the intubation is very old school.

Yeah, we're gonna see some products.

So I think next time we meet, I'll show you more because actually there are many interpretation products.

I didn't look at all of them But today we're going to see a few. I think you will like it.

I'll show you this one Ladies and gentlemen For me, I think you egg you out.

It's one of the most important Factor main for left result. So, we use or we don't use it, it depends on that. Which one? I mean UX/UI. Oh, yeah.

By the way we integrate the result.

Yeah. Okay. Look at this. Okay. It might look very old style but it's more like research view. But when you look at like vitamin B, Okay, this is the optimal client.

That's amazing. How did you get this?

You know it's like they use their own dataset and then they put their own information.

No, because I have the enhanced dataset so I can recreate this.

Yeah, you can use enhanced dataset to recreate something like that. So we know where we're at.

Yeah, and I can filter for Asian. Yeah. Let's try.

Yeah, this is the way they report the results. So we know, okay, this is the normal range, this is our range, something like that. It's higher than Everest, it's lower than Everest. So you see that she's in interpretation. Actually it's the same like you show in the range, but this is more complicated and like fancy way to interpret the result. I'm not sure this is the most updated. I think it's already all.

But you can look at this. A spacer cell of labradori. They do nutrient micronutrient test I believe they are. updated is already this it looks very old Okay. You know that why I don't like micronutrients for fire in Thailand. You see the way they report. How do they know this is the range? It's not, it's nothing.

I think they keep it vague because they know they, even they are not confident of the data. So they don't say exactly what they do. Yeah.

Like I mentioned first time about the reference range. You can use big data set to plot the graph. But in the future, when you have more clients have more data like at least like 1000 yeah you can not not use it as a reference but use it as a crew yeah for example like crp for most people that you already tethered what is the median number yeah or what is the range that you see start from one to three So you know that where you ask when you compare with most people.

Also, I think we have to keep in mind that I think people using our product will be Most likely we'd be already very healthy. I think. Like if I have to guess within the Thai population, it's probably like the top 20%. It's true, it's true. It's kind of like bias a little bit. Yeah, super bias, yeah.

That's why we don't use it for resident range. We use it as a magic number. Yeah. Something like that. Okay, that's the part and what next? Okay, let's just review some product I think.

So This is Kiro. So Kiro, they seem to be... So it's kind of similar to health matter but in Europe. Cute. Chiro, yeah. K-I-R-O. Actually... You think?

I can show you my computer if you want.

Oh, okay.

They do the same, right?

Very similar to Health Matters and they are B2B, so they work with hospitals, so it's very similar to Health Matters.

So it's very... This is the way they interpret the result, right?

Yeah, so it's a bit old-fashioned the way they display, but they are very serious because they work with a proper hospital. And they raise a lot of money, so they're very well-founded. Starting by the cleanup.

There is the range that shows this is optimal.

This is the way the input feedback is going down. Actually, some of my tests I did my time in love. Okay, actually this is my style. to beat them in town.

This is very, very detailed, right? If you look at my report, it would be quite, it's pretty much the same. Okay, now let's look at some more, I would say, customer-friendlySo ornaments that we like. It's a Swiss company. Okay. So they only have an app. So that's how they report. Let's see if we can. Yeah, so they have the rent. Yeah. Hi, this is a global view. So they give Oh, yeah. I don't know why they use 55.

To NN is a street number. This is not a movie, you should use the video. It's not too low, it's good, but maybe they use their own analysis. I'm not. Optimal range that I chose is 40 to 50. So for me, I think they use a lot of their time. I think it's good because if they use this number, that means they're not made up. They have the information from sound. 40 to 60, what are you saying?

It seems to be pretty high. From DNA, that seems to be in the mind. -Oh, no, sorry. This is not, it's different parameter. It's calculated. Yeah, okay. Forget that. This is my problem. Thank you. Please mind your head, T. Lewis. You have time to ask a question. or you will stand up because they use different So you tell me which one is the tight end. This is European standards. Actually, you didn't do that.

Because it's Swiss company, so. Swiss, you know, it's in Europe, but it's part of the European Union. Yeah, but, you know, like, for example, like, for example, yeah, uh,We follow.

One The thing before What would you say about metric, right?

But all medical Yeah, imperative, yeah. -Everything else we follow. Okay, so they seem to be using similar to this, right? They have the normal, high, normal, low, and then optimal, high, optimal, low. This is the recommendation. Bye. Yes, so So this is supposed to be the global view of your health? Why they show you So they compare for gender and they compare your age. and particularly for our community.

This is a global view. Sorry, I'm showing a little screenshot. Amen. -Yeah, so what they do is they give a score to the organ. You need to do that. What do you think? Do you like that? The way that he's played, easy to understand? Not really, mate. I mean, I'm not mad, Ian.

I think the way they interpret it is good, but the way it looks is not good. I did.

And look. -Yeah, I've been fine. You see,The picture is like, maybe about 20 years ago. Yeah, yeah, yeah. Like Windows 95 3D, yeah. And the way they interpret this is like,As it's big, right? If it's good, it's big. If it's not good, it's small.

Or if it's not good, it's big, you see, there is no consistency.

Yeah, I think it's just maybe the part of the organ, maybe how many test you want to admit?

It's easier to understand.

One more can do. It's more about-Yeah. It's about like two inches. Yeah, so what I've seen competitors do is like they have... -Usually, so you have like the, so you have like one score. So the score is like, so ideally, So, you know, Wood, for example, they have-They have the recovery percentage and strength. So often it's I know the age. Metabolic age or metabolic score. So score could be, I don't know,And age could be like, the And my real age is 36, so I'm like two years older.

Yeah. I actually don't have score because I think it's hard to interpret. because let's say 50 out of 100 Is it good? Is it not good? I think, so you don't know if it's, is it, does it consider by age or is it 50% of the general population anyway? I think it is easier Because let's say I'm 36, so I know I'm lying to you. He is younger. My friend, my friend, he's younger, so he's more healthy than me, even though we have to stay very young.

Metabolic age is good, so? I don't know how much you know about this, but there are actually some scientific studies here. Do you have a metabolic rate? Like a final, final eight? Yeah. You can use that to another. When you get the test,Okay, yeah.

You don't have to, but it's not for the 10. When you take for 110, You use all these sound data to compare.

-But I have enough that it's for a while, maybe I, when I have more,And then you can tell me.

Now we have a lot of data. There you can do it. You can use that database to campaign involvement.

Yeah, actually, NH would be great for that. I can compare my own biomarker with the NH to find the machine learning. Yeah, yeah. So what do you think of it? Do you think as a doctor, as a patient, something you want to see? As a patient, as a doctor, I still need to take a look at the individual lab.

The In general, I think you got it.

Actually,Okay, the next one. You know, only by test they can-Can you hear me, Bob? Oh, no, I heard of it, but I haven't checked. Can you send me this as well? Yeah, yeah, yeah. I will be able to again--It doesn't matter if it's a one-point pen, right? When you test, you can calculate and get a compare with your age, okay?

How many years?

I didn't talk to you. It's a lot. Yeah. It's a lot. And then you see it's not the best idea. Okay. And if you look at the...

Okay, you see, in life, they calculate in this order.

Your age is lower than 80% of people at the same age. So they use that to to compensate and not just comparing the age on your own. You're gonna have to figure out that, okay, So at this point for me, it's not-It's not really fancy, but it's easy to understand. Yes, yes. So that is one, I think is. So that was something I wanted to talk, so like, because, so, Score is like, that's just one number. And then another thing would be that the organ-It's kind of like a pyramid, right?

Yeah. So here you have like--Only one number. And here you have like every single biomarker. And you kind of want something in the middle, right? Yeah, exactly. As a person, you-this is intimidating. Yeah, yeah. If it needs to be copycatted,--We don't mean to understand, but if it's very simple, we have to try to make it as simple as possible. And so for the organ, So for the other night, how do you try to do this?

They left us now. How would they, what data set they use to integrate your age? Would you like, do they use the same volume? So with this, it doesn't matter how hard they integrate. If you want to know more, for example, like when you look in detail, you have to know what blood test you have done. Matt. -I did. So that's very important. So, simple report like this, For easy understanding and detailed education.

I mean detailedRight.

So you would have, for example, all of the single biomarker. And then this would be like hard. And it would be a good case for heart. Another one would be like liver. That would be a kidney. So you kind of aggregate them like this, right? Aggregate again. From the user point of view, obviously we always use the. Yeah, but in practical,When we calculate for n. We use different data sets. and the tablet or OK.

So it might not be the same class. When you are, when you report it. Please stop. can be integrated all together and some. One thing about is we can different-our organ can different. So if you ask me which one better, One number about your total case. I wonder where you are going. I have a separate number. I will keep it for this call. And so for the audience, how do you... I'll give you a good case number.

'Cause here they use out of five, here they use like, Yeah, you'll have to do some more research on that.

Okay, so then you have the first core and then you will have the organs.

And then I guess if you click on the onion, then you go to like individualYeah, yeah. And then when you think of my work as a biblical explanation, Like what is this? What is that? I think this is very... Clinically helpful because you know which organ is the weakest, right? So when you want to improve yourself, it is not like... doing everything so for now okay because we can't forget our homework Okay.

Yeah. Hi, Ben, actually. Yeah. Hi. Yeah. So, so, so he's, Inapplication. Now we don't care much about is known. What does it mean? We don't know. What does it mean? Oh, this is better. But it's still like in the I think when you want to calculate for number, you can start from here. And in August, that'd be my problem. -Immunity, you know what I guess? Okay. And you can use the call one, two. Yeah, you see there is a scandal that we have.

But this, can you get from the blood? Yeah, please hold on to that. Yeah, I guess the-And also metabolic health. I guess this is something we can, that we're gonna talk about. This is the bread. Let's just quickly review what they have. So the app will show you the technical. I don't know. They have the same number of operations. I guess like this is a bit more modern. --So this is just screenshot of the app.

They have AI integrated.

-Actually this one is pretty good.

But in terms of detail, And we saw the few end runs.

-Oh yeah, I know you like Kiro. Yeah, Kiro.

So, let's look at the report. I'm not sure aboutThere's no report, just so you know. Yeah. When you look at the email, Sorry, can you grab it? You see that it's here. This is the way I like. Oh yeah, I think that might be something. Actually this one, I have an account. Actually, it's my idea. No, no, you're right. It's my idea. I forgot the English. Which one I use, I forgot which one. What are the minimum or minimum?

Yeah, I think minimal like this is better. Yeah, this is nice. I love being involved, but for me, that's very important. You think it's too much? It's too minimal. Yeah. Yeah, I mean, you need to--I need to, I, I, I, I.

Hi, hi, no radio record.

That's good, butWe have to take out that. Okay, they're live to drill down. Here by your command. I love writing, but not this color. I think that is one of the design is bigger than that. Yeah, this one sounds really bad because it's a B2B product. But I'm used to be always terrible UI. I don't have to worry about you.

Okay, we got it. Oh yes, yes, yes, this mic too.

--Everything good? Just like that, let's take a look. I know, right? Pretty bad. Not bad. I believe this is the goal. People them toFor me, I think it's good because you cannot rely on your--Not terrible, it was just. Yeah, thank you.

information.

For me, I think it's--some information that Happy Catholic Week. -I think it's pretty good. Everything is. -I think I used the PetsLab report. Okay, okay, I'm doing it. I think. -You already got it? Yeah, I eat a lot at night.

Yeah, I eat a lot of...

This company is recently raised money so,Things are gonna change a lot. This is a pretty recent company. Even though it looks old, Actually, I think the way they use it is good. I didn't like this shadow. I developed mine. Try to replicate this kind of And I highly develop that idea. Good morning. You cannot do anything if you don't like this language. And I know they can, but they have to pay more.

That's very important. So this one, even it's very simple, but I... I mean, it's cute. It's easy, right? It's easy to make a shadow, right? I know. It's not fancy, but it works, right? When you look at the report, We don't worry too much aboutNow the way it's from where I want to look and IHe needs to understand. He needs to understand and he need to be fast. I think it out. I don't want to wait like long time.

-Okay, so we do the last one and then we're done with the project. And then we do the test. I can take a little break. I really wanted to go.

Yeah. In the US, it's very hot in China. So we need to be the first in the room. Bye bye. Okay. Uh, a very busy industry. Good night. I like it. Besides Shadow, If you use light gradient, back out. I love it.

Because it look, it look-I think it's all right.

So they added recently AI, so that's why they put it everywhere now. where you can ask stuff. So it's, they're replicating this anyway. That's why it looks really bad. So I'm just going to hide the AI.

So I like this. So this is how they show the organs, but they use a percentage.

I think it's more clear. Yeah. Yeah. and in range, so it's easy to understand as well. Okay. So of my marker, how many he read? I think this, This is good because they're very, very fair. Yeah, they're very good. You need to tell how and how, we don't have that. So you can't decide.

Yeah. If it's good enough for you. Exactly.

I'd say 70. I'm happy. Happy, yeah. So I think it's good. This page is-so the website, I think, is too confused. But anyway, this also recent product. Yeah. So this is-They also do aIt's also a head right?

complete They do value collage, I like that. They don't do the...

Point, so they only show so many.

That's why I think it's a bit confusing because they should show this first.

I don't know why they chose him. It should be. So this is all my test actually uploaded. All I want to like emphasize So this is-Oh, OK. Apple test on 2022 BDMS. And I have another one. I think it's to go to the next town. Any other might be adopted. It's not working. Now, I know also it's very buggy, so I recommend you use it. So actually, the most test is this one, but it's very buggy, so I should use that one.

Okay.

And what's interesting, and then for organ,

Difficult to understand. I think the design could be improved. Like it should be shaded instead of just light.

--This one I use for a physical screen.

Actually, I should stop using because then I'm like, OK, what do you-It's all scary, right? No, no, no, it's not very high. You don't have to worry that much. but it's still high in the database. I do agree with some of the ideas. I think they use pretty standard range. So they have optimal low, optimal high, and then they have normal low and normal high.

and use the lower half grade. Right, but here, ALT is like the lower, the better, so So, is that new present left? And then they have one.

Oh, I know you're gonna like this. I'm going to go back to him and let you play with him.

Okay, I like the way it is.

The interface is a bit noisy, I will simplify it a bit, but...

All right, you go. I'm good, I'm good. Look at this. ----It's a nation. What do you think is the idea-I mean, like, they probably would do. I'm sure it's AI generated and then somebody revealed, you know. And you see there's some reference, You might not read it, right? But okay. When they give this information, so you can't read it. Yep. Yep.

That's great. Yeah. Yeah.

I believe in AI.

I think it went good.

Is this accurate, calorie restriction?

Yeah. Yeah, they also have an action planSo that's what they, based on my test, what they're recommending to them.

it's not like you know they are generated but they may give their eyes to the end And then with the intervention would be.

Let's say it's automatic for sure. Yeah, yeah, automatic. Actually, so I don't like the I think I would-I think it doesn't look good, but it's very comprehensive though. Yeah.

I guess, I think we have to rest between competitiveness and--Yeah. -I think it's more like many common calls. This one, too big, too big. Okay. Call me anything. Too much emphasis on your. Maybe they want to give it to the camera.

It's marketing too, right?

This is good, you see? Oh, you see, what? I think it's pretty cool because Yes.

So, yes, so I like the You can do multiple times. Okay, great. Like this?

I think this is. --------Okay, it's good.

-Yeah, as you can see, it's really simple.

Even if you can share with your doctor,That would be,-Okay.

Because if I'm not a doctor, I don't wanna see I think any of these views too much. Yeah, I saw it. Then I kicked on the organ and then I kicked the music.

-Thank you. Can I have a light block? Yeah, I think any kind of rodent, if I'm not in lockdown. I think this is not.

Cool. And then you actually met someone. Okay, let's see. But the action plan is very, actually not AI.

Could you see it?

It does automatically pick up. Yeah, it's like action. Okay, do this, do that, do that. And it's not very Thanks. Okay, I guess I'll give you theThe action plan I think is just okay. But I think the results are pretty good. I'm not talking in timeline, right?

It's not really action-packed. the action of using the normal open app, right? So for me, this is... Thank you. We can start from this and then summarize off here. Level one. And. I got that. Yeah. That's that. Light bulb.

This one isYes, for the air review. I guess we got it. Today, let's do the blood after. So we can review. Next time we can, I can show you some more.

If you can. I did. Yeah, yeah, yeah, yeah.

Some part of AI.

Not organ part.

Yeah, the--What about the company?

Oldament. Order. of automating. I don't know what to ask you then. --Hello. ---All right.

They're all actually... So they started a long time ago as aAnd that's his company. I think now those companies, they don't, they're not making money. Okay. I think blood test is much more lucrative. I think they might try to do both at some point. Yeah, but that website not good. Thank you. It's decent, not that great. It's before COVID, right? So I think for the time it was okay. That's why I'm. That's why you see it.

Why, the reason you have For information side. I think it's very important. Okay, this one. Actually, I----The sick full body in my life. they partner with cooking company.

But this internet is nothing.

I can't even tell youI think they would be happy to. I do. We have a business now. Yeah. I think because am I very.

You have to like, Sit like this for an hour? Yeah, that's fine. The client.

-Yeah, yeah.

And it's expensive too. Yep. I did it.

I did it. I did it, right? I don't like it. Down, hit it. NothingBecause I cannot vote. Now what about the,Tanya?

Yeah, so let's take a break and then we do the panel. Finish what time you need to do? -I mean, actually, that was the onlyToday, I only wanna talk about the. We haven't started. In the morning, where is...

Very tough for me. I have two months in a day today. Yeah. Talk to me. Thank you.

Same I also don't know So first of all, please hold on, JDMS, right? Yeah, about his path.

So yeah, maybe we'll leave the part of it alone.

He said that if the head is cut off, We're just sharing. I think I mean, right now, I just talk to many people, honestly. I don't make any decisions. Not just a doctor, but also I talk with a lawyer, I talk with some marketing people, I talk with some... Oh,. But the thing right now,Until the product is not started, I think it's difficult to see I was going to do what? I also need to see like, you know, some people, Some people want to be co-founder with shares.

Some people just want a salary. Some people want to do hot time. So I think it's easier to start. Like this and thenAll right. Yeah, then when they'll eat, you know. When the demand starts, then we see, OK, who wants to do what? And then-because it's also-Yeah, the problem is I don't want to spend too much money. I can kill a higher food than I'm going to. I know. It's too much, all right, okay. Let's do slowly and then we see, okay, who's interested and who's doing what.

I think it's too easy. A lot of work, a lot of work. How much are you getting paid in VNH per time?

--My hobby is playing football. -So DNA should do two days, three days?

Three days. What you getting paid for that?

---I'm really happy. --Thank you. Hi. It's very, very easy to follow. The can.

But you say you like that job because it gives you access to the edge.

Yeah, for me, it's not my advantage. You might be concerned about that, right? When I look at my text, And boom. I don't get that much from this topic of the day, but I have some of the heartache of the transformation of the art.

It's not even working. So if we, let's say if the project was a bit better, what do you think would be the next step for us? So, working for BuddyCycle would replace VNH, pretty much? Oh, we did, I'm asking you like, wow.

-property be happy to talk. Not that far. Thank you. Yeah. And what does it mean that I can work? Actually, I can. And Because it's at the time they can't-Do you want to keep your German Danish or are you willing to--Yes, he finds himself. I think hospital that in case I need referral is more convenient for my patient. to refer to another contact about it. Because I on this next slide orSo if let's say we agreed for you to work on the like one day per week or two days per week.

How would that work for you? Work less on Sandwich or work less on VH?

This Okay. It's all going fine, but I don't have to spend that much time. It's very disturbing. -Is that three days at the age?

Yeah, three days at the age. What do you do the rest of the week? And I had to do that.

I want to add another one. And one and anotherOkay. but one in two.

So you want to... So if you need more time, you would probably quit telecaring first.

Yeah, I like it because the environment there is good. PeopleThank you. Uh, Also with your project. So you don't have to worry about my schedule. I can manage it very easily. Another positive thought that they asked me to leave everything.

That's not good.

That's the problem with [[nick-warot|Nick Warren]] actually because he's full time for [[bdms-wellness|BDMS]] so if he leaves they have to give him everything.

I think it's just the But he has a choice. He can leave anytime.

He had the shot, he had. Two and a half. enough resources.

I think it's kind of like...

that we have to make the decision.

I think it's very good, Pete. So he's very new.

For me, working as part of my company, Most of your money is from some business. Thank you. Thank you. Not from crypto, but I think if I'm working too much on crypto, I would have to work more. Now, it is quite well balanced for me. I knew. I feel big bad walking in the hot is paying me a lot of money. Yeah, maybe I'll go with my. It's OK. --with my I think is very relaxing for me. in the filter for-I think that's difficult for me to read.

Bye. Okay.

Great, well thank you for the info. I think it's good. Like I said, I don't want to promise anything because I think it's just too early. It's okay, let's start with this. We need the... I just want to see some traction. Yeah, just get any prototype working. And I think the fact also, I don't mean to lie, the fact that you have your own cake is also very valuable as a, you know, I think a doctor found that guy.

I don't have to do it. I can just use you. Okay.

But if you go there at the hospital, I work 100%. In my, I mean, in my, In my doctor part, I'm pretty sure I work more than 100%. So you don't have to worry. You can go to the hospital and consult with me.

It's anything.

Okay.

So, um,And another website I made. So I'm trying to compare I'm trying to compare competitors. Yeah, function helped me to have super power to see what test they do. Um which is a lot, particularly difficult to compare. Are you seeing this before? All right.

Yeah. I do it.

Okay, how are we going to do this? I would like to design a bug panel Similar to you know, one of those three competitors What you were saying is the easiest is probably like Maybe function health is the reference? The problem is a lot of them I cannot match. It is taking, We can just, you know what, we can just make a movie. Dean Loewentritt has a by-product. Goodbye.

We are now in the event.

Okay, so. Okay, so any help have a Actually, let's look at the handheld document.

Okay, what's that?

I have been very complicated. So they have, This is the master project. I showed you this before. This is all of the test. His name, code. Turn around time, blah, blah, blah, blah, blah. So I've extracted all of the data and put it in a website. So we can search as easier and we can-Yeah, we know. You know, I can say that vitamin D for example, and then this is called the vitamin D. And then we can add, we can make our own panel.

This is the panel. But some of them are a little bit complicated because for example, for cholesterol, cholesterol, They haveUm...

And get the--We look at when you take a corridor, We don't. We send for a little bit more time. Yeah, from those back then. So we cut down when they cook it. the wedding, the machima. You see? Like liver function. You have to understand that. Now, let's go. Yeah. If you want to Maybe cheaper? Yeah.

So actually I think it's easier to use your computer as well. Can you open function help? Can you tell me what to do? We just do the test and then we try to record the function help with NL and thenAgain, maybe we don't have to. This is the actual one.

I think we start from,Are you willing to remove the PNN level?

Okay. So here are the use of. Thank you. I did that. 450 bucks a minute.

And then Please do see happyC-O-T-E-No problem. reactive protein. Thank you.

-Next slide.

Rachel, one. I think we can cut this one.

Actually, there's one thing that I can It won't happen.

Never tested before. it's good to tend to. Normal. Let's try adding one.

Yeah, yeah, let's do the soluble protein. And so they also doYeah, you don't need it actually. Special one.

You know, if you want to cut cut, Oh, not in that one.

-I'll run it back. So, Apobi, you don't need it actually. You disagree?

Okay, let's try at it, but I think the part would be crazy.

Hey, Javier. I believe we're going to be out. -Can you hear me? Yeah, you will do good, you will do good. Okay. Because now I have become A1 is full 50 and theySame, right? I'm sorry.

Not too bad. What should we do? How do I send that email to each other? What happens? Elaine? It's like, if I'm looking at it, it's like,It's for security reasons. --Okay, move to thyroid.

Okay, so for 1,900, where is it? This is just for restaurant. It's probably good for five. It cost 1,500. I want 1,900. It's crazy. Right? I mean, this is retail price. But it's already crazy, right? You know? I mean, this is there, but this is retail price. Okay.

Do you think they might have a package?

No. Bye. Sorry, sometime. Sometimes the packaging is better to check in. Tyroid. Tyroid. Tyroid.

Yeah, that would be what, in 1,000-I can equal that withYou may have a problem with the rain. I don't think they have it.

-I think that takes time out. And it's here there, 2053. I mean, you-No problem. Because I'm also, I want to make sure that my tool gets the PDF correct. On my knowledge, I believe that it will happen. Okay, so TSH added in three and three. Tweet, tweet, tweet, tweet.

What is it? I don't know. T3 is already half. What do you mean T3? And then you see 53, you see.

73 and 83. Positive. Too much details. 23, every day four. I think we did a trade. Oh, actually something,Time. people. -Something I forgot to mention. They use some kind of classification, I don't know if you heard this.

Oh yeah, but this classification is not the same as this. Because they kept it by itself. Thank you. How do you put this into your app? That would be really difficult to understand.

Because right now it's 200 pages, maybe it would help me to cut down. I don't need money.

I think that this is where it's hard to find out the enemy.

So from that, which one do you think of as completely useless? I cannot tell because sometimes I don't know.

I don't know that much about you. Are you the one who's sorry? When you say a celulity, I don't know.

What is celulity? I'm not sure.

I just know the name of the thing. Cancer? Okay, which one? What they use? Cancer. No, no, no, no, no, no need to do. So we have, so for Tywin, we have TSH-34-39.

Yeah, that's all. OK.

--Oh, no, I'm not.

And I think you like a little my beingI saw they have a package as well, like a micro-insurance package. Would that be useful to use this? Do you think it's cheaper? If you want to look at the more comprehensive But do you think it would be cheaper than selecting one by one? Yeah, of course. Because the problem is they do the. You want to input it?

You don't have to do it.

Because the value-meant deal, okay, I just want to show you, because value-meant deal, they have So the standard test is this one, right? Yes. Total vitamin D3 is normally look at by the total vitamin D3. Yes, but the problem is they want to sell you this one, D2, D3. Yes.

Okay, now.

So the prime is there, my pretty sure I could use that one. Yeah, that's fine.

But they keep the other prime. So in the total package, That's $5,000, right? That is very cheap. Yeah,.

Thank you.

If you look at the test separately, Where are you going to be?

So you have to be like, What's inside the Muggeridge? Or the intent that you can't take in parent. Okay, that's a good deal. You think it's a good deal?

If you want to add this to your package, that would be a good deal.

Yeah, yeah, let's see. Let's move to another email.

I do my own too. It is not in the packet. I think this they also have a package. What's the They're taking more regulation, but actually it's Can't be but cut. Yeah. So we have these-Go to the mail. You go to the mail?

Yeah. I think most of my personal email. Okay.

So, DSEN. -That's like it. Um,Tempo zone. control test.

-Or they say they do free. When they do fee, they do everything.

You want to do me? I don't think so. Because it's just a. Yeah. So it's not useful. And the--It can be used as a. Yeah. Okay, and then transform one. You want to add quality to it? Thank you. If you want to useyou don't do it, right? --Again.

People need to keep everything. I just put it anywhere. Go across.

They have multipleTesting free random, no, testing.

Who goes first thing?

You can type A1C. A1C? Thank you. And you can see them. One such is invited to enter.

.

Every metal you want to include them.

Sorry, sorry, which one?

Actually, that is.

I think it's pretty good.

Maybe you can tell it to any of you.

I actually agree with that. Not too much work, right? The website is very easy one day, but extracting data from that PDF was very difficult.

And don't come in.

They have a... websiteI'm right.

So you may have the name from this website. That means that PDF is going to be done, right? Yeah, perfect. Because if you have two, you cannot examine anything.

Thank you. That'd be it for me, by the way. But this way, this way, we don't want to expect that.

But because it's fixed, right? So you can extract everything.

But the problem is it's not real table. It's only aYeah, it's a little bit difficult to extract. Actually it's good because I'm very good with computers. Somebody else can do it.

Good enough, right? Good enough.

If you put this in CGPT, I will not be able to explain. You're gonna have to do it. --Yeah, we can start with this and then you start. Stay with the devil. Yeah, baby. Maybe they will like the product, maybe they'll buy the product actually. For them it's a good way to create demand. How much do you think? 500 million dollars. I have this here now, so you don't have to do anything else. Just focus on the project.

In a few years I think.

I believe they can do that, but They don't see any reason to do that.

For me, I do this becauseWhen I have this, I can compare with other applications. This is a price comparison tool.

Okay, top scene. You want to have it? Okay.

Let's just draft just a group. Very comprehensive by the way.

It's still not coming to you now, okay. Let's try it later. Black, it could be black. Another one likely.

But this is very comprehensive. I never seen any clinic in Thailand do all this.

How much would it cost to a patient?

Because this is in-house price, so it means for you if you charge it to a doctor, it will be--I did.

Thank you. Less is in the packet. In the packet is what you want.

I mean, we use the package as well, when we can, right? Yeah.

Okay, first, heavy metal. More of the metal. Try this. Heavy, heavy metal. If you want to do the---Thank you. Am I maybe in my DC one? Yeah. Maybe you can do this.

Okay, so they're all equal. Yeah, they are. .

It's pathetic. Thank you very much. Margarita, run. And let me know. Toxic metals. I think let me do it.

So what age? What kind of patient does this? Because actually the most comprehensive package And that would be it.

And I think it wasn't. Ah, I know, because it's optional. Most of them, most of my patients And now we talkThank you. So, yeah, you could do it with anyone you can, and it's well-meaning for a little time. Can you remind me to be helped by something very well? Okay, the additional part you already addedYeah, micro-insurance andYou try forming them? --You see my hair? Oh my God, no. Happy Advent.

Oh, is it with. You have to time back at her. No, no, no.

I believe it's not included. It's a black color in Canada. I'm happy to answer. Woo, you know my lap, stay there.

I have been the best. This is the price of 2024.

-Okay, maybe. Do you think the big five will be added?

Yeah, that's a lot. Very. Are there ways to make it cheaper?

Do my lab. My lab's cheaper. But you cannot buy, I can see now.

Do they have like Omega?

My lab is just--I want it.

Oh, so that's the exercise. Yeah, my mind.

You pat me. COVID had that. Like, like, like, uh, like one. Yeah, this is a big one. Why don't we be by with them?

AA, EPA. And so this will be how many markers? I don't know because it's not-I can't. It could be.

-This is my test. My app is testing. I'm here.

But I guess what we can do when we have this list is we go talk to Intel.

Or you don't have to order to Intel. You can order. So you don't agree. Yeah. You can't say cheaper price, right?

Oh, no, this one, sorry, this one got turned around 43 days. That's.

Yeah, yeah. My dad was always the one with the cheapest. I'm attending.

Is it that difficult to?

It's not difficult at all.

I had no demand.

Even I try to from 2010 is not very popular. I think it's really good test that everyone chooseOne of the best test that you can do to be doing your overall nutrition. Oh. I try to. Thank you. in the cheaper and more comprehensiveIt was not going to-And I think. Because it's very good. When compared with my phone, I think it'sI'm just going to go ahead and--Maybe that's how we make this test for today, no?

And help with my lab too. Ah, Fred?

Okay, that's already included. Liver, okay. Put liver. Thank you. So now. Yeah. Not working. I didn't cut anything, but-My task path is just not working. I don't know why.

So leave your function a test.

Yeah. And then you add this one, ttt. Not that it could do. Last we already included a head from my group, but I don't think we need to do that. ---There it is. What is that editing test? Are you tight here?

He didn't feel you had to do it. He wants to... -Well, I think I checked yesterday. I couldn't find it. What was the other name of the creatinine? BUN is... -That was the, yeah. But you're in aYeah, blow the wind out, yeah.

And you're set. Thank you. Okay.

That's so weird. At least it can be touched. Yeah.

Transgress, no need to test. Action. -I just had it. You don't need to have this. You don't have any-because the amount of time will come back on. I like when there's an intent. Okay, and did you-Uh, Ben Hill? Okay, you didn't provide You can type in Electrolyte.

But wasn't this part of the... You dream. My producer?

Oh, that's me. I already have my monitor. Right.

-Not nothing put in it. I'm happy.

You type in "electrolyte". Oh, they do it again. and the group update line. Ria, oh no. and you can do that. They're not that I just mean that. and anyone you like to like, that would include Go up there. That one is not in the diagram yet.

You already know all the plugins.

I always tell you that if you just give me the list, I don't. This almost 20 year of my practice. Actually, even you don't give me this list, I can like project. Write down all the lists. And as much as you want. So, so, uh, It's kind of lame, Rob, but... I don't need to copy them. I can start from my--Let me just take a few screenshots. -Good morning. Pretty good with this cold weather because outside very hot.

We went there early morning, very hot. electrolytesMelody? That's expensive though.

No, no, no.

We have already not attempted. I think. Combination.

Again, this will get----Why?

Why?

Maybe, I don't know what I'm going to say. I think it's too expensive, $30,000.

No, it's not that expensive. Okay. Normal on as you can. Yes, indeed.

Good afternoon.

-The combination would be food and insulation. Yeah. Actually, that is the combination. Thank you. Maybe then.

I don't think everyone did that.

Leave it.

Sorry, would this be doable if we send the nurse to my home? Everyone, but everything is okay.

I think it's optional. If you want to add it for one more. Yeah. 50 hours of high-intensity is 40 sensitivity. That's a lot of them.

I think I'm sorry, this is three years old. What is? I've been there for one or two years.

I think they use different category because having the category of the--You read. urine analysis. Urinary, sorry. You want me to stand here? Yawa. --And A-R-Y. And, uh, spares and license. Yumi. ---Now. during examination. There are many what, Even you do very comprehensive package, you cannot buy urine easily. Okay, that's all. I do read them, I do a film. I believe it's infectious. Thank you, Adam.

This is a good one, but On basic part, we don't need to add it. I don't think that one I'm un-naming is good.

Yeah, oh, this is says it's available at home, so it's not--No. Oh, but they did?

All add on, right?

Yeah, we only want to do the main vacation. AI.

It's an AI.

Got you. So 27,000.

So it means if another company has a member, the one that you told me to follow along. from Singapore.

-Victor Hill.

I used too many fronts. Too many one.

Yeah, do many of these.

40.5. Bobby I think you in terms of hormone, I think is missing the missing part of our-You want to add it? -I can see you.

Kind of like daddy told me. Oh, yeah. Right.

-No. It's very important. Vanadie. No. You can add one.

That's an extra.

then in that modified packet. How do you find women?

Hi, Jeff.

-I didn't do that. is a protein to buy. The unique cannot. 10 is definitely we have to combine together. Okay.

30K. 30K. That's a lot. No, but this is like retail price.

Not really surprised, but not. Not in topic yet, right?

So, yes, this is retail price. So, it means if we get the clinic price, then we pay 20,000. So we could actually we could sell that for 30K. That would be the Repeat to us. What do you think? You get all of these plus AI recommendation.

Pretty good.

Maybe Turkey will be too expensive.

What about Goodbye.

We need to debate, I think. I think ideally, and then you actually can check the actual traffic as well. Yeah, maybe some package can be combined. Maybe some should be added.

I think the idea for people to think, Thank you. I think we will get to all of them. --Would you be free with this? And not too inventive. is comprehensive, but I have to think twice before I have to take a look on to detail what I want to be on with this. Not expensive at all. Or like, anti-aggressive test. Take a look, okay. But you know, if you cut my code nutrient profile, it's not expensive at all, right?

My code nutrient is... And if you look at all the chips, all the scans, all the trees, and you get cheaper price, I think you can cut it out to like $2,500.

I think we also need it. We need to be like... Crazy amount of time. Because otherwise people would just go to a normal check-in. It needs to be like crazy valuable. Like, "Wow, it's like a hundred dollars, you know?"Yeah, I think it's good enough.

-Let's see.

Just take a screenshot.

But it's not that effective, I believe, when you cut-Try to minimize the cost, I think it would be much less.

Yeah, I mean this is the first pass right?

If you can get itNot true. To fight or to fornice? For the user, you mean? Yeah, for the user. Okay, I think it's easy to sell. Okay, so we'll see.

I think next step will be for me to actually get this done.

And if you want to come back, You can't wait. I think it's my phone. They might have thumbtack. Are you disabled? Yeah, and I'm disabled without knowing. Yeah, I'll try to look at this.

This is the first half, right? The first time I experienced this issue. Yeah, I have a friend who has a yoga laptop with windows. Is there a shortcut to disable the trackpad? Because apparently the trackpad is disabled and there was an icon on the screen to show that. Thank you.

I'll be coming in now.

Function f6. One, two, three. Thank you. Yeah, it's not that one. You know which one? Yeah, yeah. Yoga.

Okay, let me try. Oh. Anyone? Stephen? Yeah.

Pick the book. Pick the book for me now. Okay.

But it's true. I think it's kind of like accepting security as something thatI got nothing.

Maybe You know, if I can-And they can figure out the model.

If I can't tell you how do I log in? I do. The only way I can always meet my friends. And the time. It should not be too complicated.

Okay, it doesn't matter. Okay, I... Give up.

-The thing that can be switched on, switched off, it needs to be some shortcut, right?

I mean, the worst case is just rebooted.

I think I believe more. Nice big try. You did it.

Cool, thank you. I'm gonna send you a copy of this so you can review andOkay, if I think that--But do you think this is like extremely comprehensive?

Probably about 10, yeah. Continuity. Code on the. You already include heavy metal and lighting in the way that we interpret all the aspects of health.

I think it's important because what's important is the wow effect when the person gets the result, right? It's like... by a marker the more you've ever done in your life. And then you see action plan with like some very all we found We found heavy metal, so you should do this. Like something that never seen in their life, you know? Yeah. Like ideally, if even doctor wanna try the product because they want something I've never seen in their life,-He's working out.

Okay. Most of our neighbors that we've had come into comments and check out if the hot is on that
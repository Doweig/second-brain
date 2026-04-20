---
type: meeting-notes
date: 2026-02-24
source: transcript
tags:
  - product-strategy
  - blood-test-interpretation
  - ai-chatbot
people:
  - art-chawapon-kidhirunkul
  - guillaume-doweig
companies:
  - bodycypher
  - superpower
  - vitallife-by-bumrungrad
  - bdms-wellness
  - prewell-clinic
status: raw
---

Summary

### Action Items

- [ ] [[william-guillaume|Guillaume]] to create chatbot prototype with personality (Italian chef concept)
- [ ] Guillaume to research and finalize prompt engineering for blood test interpretation
- [ ] Guillaume to create website landing page with pre-made blood test panels to capture customer emails
- [ ] Guillaume to consult with lawyer regarding telemedicine licensing and application structure
- [ ] Doctor to share reference guide for lab interpretation and test panels
- [ ] Doctor to provide Vital Lab contact information and pricing
- [ ] Team to survey target customers on key value propositions (at-home testing vs. interpretation vs. application)
- [ ] Guillaume to compare AI research tools (ChatGPT vs. Claude vs. Perplexity) for biomarker analysis

### Product Vision: AI-Powered Blood Test Platform

The team discussed building a comprehensive blood test interpretation platform with two main versions :

**Version 1 (2-year goal)**: Full-service platform similar to Function Health, offering:

- Package selection with qualification questionnaire
- At-home nurse blood collection or lab visit option
- Results delivered via mobile application with visual graphs
- AI-assisted action plan and clinician consultation
- Upsell opportunities for supplements and coaching

**Version 2 (6-month prototype)**: Simplified approach to avoid legal complexity:

- Website offering pre-made test panel recommendations
- Email capture for potential customers
- Pre-made AI prompts for customers to use with their own results
- Partnership with doctor's existing clinic for initial testing

### AI Chatbot Concept

Extensive discussion about creating an engaging AI chatbot for ongoing customer interaction :

**Personality approach**: The team favored using a non-medical personality (Italian chef suggested) to avoid legal liability while making health guidance more approachable

**Key features proposed**:

- Daily check-ins and reminders for healthy habits
- Food picture analysis for nutritional tracking
- Gradual delivery of blood test results through conversational quiz format
- Dietary recommendations based on health goals
- Balance between chat interface and organized app backend

The doctor noted that customers respond differently to chat vs. structured apps, with some preferring organized information over conversational interfaces

### Food Tracking & Photo Analysis

The team tested real-time food photo analysis using Claude AI :

**Observations**:

- AI successfully estimated macronutrients from food photos with reasonable accuracy
- Not 100% accurate but "good enough" for tracking patterns over time
- Apps like FoodVisor already implement this feature effectively

**Implementation debate**: Chat-based upload vs. dedicated app section :

- Guillaume prefers chat interface for ease of use and engagement
- Doctor prefers structured app sections for complete dietary data
- Compromise: Chat as main gateway with automatic organization into app backend

### Business Model & Value Propositions

**Key selling points identified** :

1. At-home nurse service (never visit clinic)
2. Results in mobile app vs. PDF
3. AI-powered action plans
4. Personalized supplement recommendations

**Pricing challenges**: Initial package estimated at 17,000-18,000 baht, but In Health quote came back at 23,200 baht after multiple revisions and back-and-forth

**Alternative revenue model**: B2B subscription service for clinics at $20-50/month per clinic , though Guillaume prefers B2C for faster scaling

### Blood Test Interpretation Approach

**Doctor's methodology** :

- Focus on out-of-range markers only
- Group tests by health category (cardiovascular, diabetes, etc.)
- Provide step-by-step management recommendations
- Calculate important ratios and scores (HOMA score, QRIS score)
- Keep information concise - customers only need to know what's abnormal and what to do

**AI research comparison**: Perplexity produces too much content; ChatGPT and Claude provide better structured summaries

### Competitive Analysis

**Companies reviewed**:

- **Function Health / [[superpower|Superpower]]**: Membership-based model with immediate payment, no questionnaire upfront
- **Cyfox**: Good interpretation with action items per marker
- **Blood GPT**: Poor execution, "looks dead"
- **Docus AI**: Decent interpretation with abnormal marker filtering

The team noted many competitors raise significant funding despite basic implementations

### Technical Implementation Details

**Lab partnerships**: Currently using In Health, but doctor recommends [[vitallife-by-bumrungrad|Vital Lab]] from Bumrungrad for better pricing . Process is manual via email

**Legal considerations**:

- PDPA compliance needed for storing patient data
- Application should be separate legal entity from clinic for liability protection
- Telemedicine license may not be strictly required initially
- Using non-medical bot personality helps avoid liability for AI-generated advice

**Data history value**: Doctor emphasized importance of longitudinal health data spanning years for identifying trends and potential issues , though acknowledged immediate clinical value varies by test type

### Customer Acquisition Strategy

**Phase 1 approach** :

- Create landing page with curated blood test panels
- Capture emails without requiring payment
- Provide pre-made AI prompts for self-service interpretation
- Build email list of qualified leads for future product launch

**Marketing insight**: Many people already use ChatGPT to select blood tests and interpret results, but encounter issues with Thailand-specific pricing and test availability

### Next Steps for Development

The team agreed to focus on:

1. Creating prototype chatbot to test engagement
2. Developing simple landing page for email capture
3. Refining AI prompts for blood test interpretation
4. Testing with small group of friends before broader launch

Guillaume emphasized starting with legally simple implementations that don't require telemedicine licensing, then scaling up as regulatory framework is established

Notes

### Agenda

What are the topics to be discussed?

### Notes

Add any notes to provide additional context and details

Transcript

Um... Okay, so today, few things I wanna do. So, review the research. for vitamin D, triglycerides and Uh... I think... reactive H reactive protein something hc rep I forgot the name sensitivity yeah see you see a key CRP yes so those three Um...

And then other than that, I want to do some prompting. So Prompting is a bit of an art with AI because There are multiple ways to give your blood test results. Which I haven't dug too deep. Well, I think we can try some stuff. Um... Oh sorry, another thing I wanted to ask you actually before we begin.

So about OpenClaw You know the thing I showed you? What do you think if So having a chatbot, I was thinking, What's fun about OpenClue is like we can give him personality right so I show you the bot in my group he He's pretending to be a pirate. So he's like, you know. And so I'm thinking maybe we could give a funny personality to the bot and then When you get your blood test, maybe the bot could give them slowly, it's like...

take time to explain and then maybe ask you question is like, hey, do you know how to lower your LDL and then give you like, full answer and then you know like a quiz? And like every day you answer one or two questions so you know over time to to keep a connection and then over time, and then you can just chat, right? And then,I don't know what you think about that. Yeah, good idea, good idea. Could be fun, and so I was chatting with Claude about which personality would fit well.

And so I'm actually thinking to use a non-medical personality because I think If the bot pretends to be For example, a chef.

Which one do you recommend me?

If the bot does not pretend to be a doctor, I think it's also It's also better because the bot might make mistake when he say things and we don't want I mean if the bot if it's like AI doctor I think if you say your bot is AI doctor, you need to be very careful about what the bot says, right? Exactly. So I think it's better to say, okay, I'm not a doctor.

I'm just like a cook or like a funny personality. So whatever he says, okay, he said, oh, I'm not a doctor. Okay. I just say things. I'm not a doctor. I think for legal, I think it will help a lot.

And if you, if you want an actual opinion, then, you know, okay, you can book a consultation or whatever. Probably we made things easier. Yeah. And maybe we prompt the bot toAlways. Yeah. That's a dog time.

Not a dog time, just to cook or something like that.

And so I think the reason why Maybe, I think food might be a good angle, like the bot pretending to be an Italian chef or, you know, he can be like, "Mamma mia!" Because if it's food related, people would be asking more questions.

Because I think, okay, I think number one thing you can do about your health is food. So I think it would be nice to have... If people have a food question, it's like, because a lot of people just don't know about food, right?

They're like, oh, I don't know what to eat. My cholesterol is high. Like, what am I supposed to do, you know? I can ask the bot, it's like, hey, today I have a choice between rice and chicken or salad and blah, blah, blah, you know, which one you think. And then you would say, oh, if you want lower cholesterol, you should do the salad or something. And maybe they would send picture, maybe they take a picture like, "How about this one?" And you say, "Okay, this one is good." I think it would be good to kind of like keep a connection to the product.

So like they keep chatting with us, keep on top of Vine.

Yeah, one thing that you can use AI to That's a...

In the better way, it's like a 4:4 diet. You might have seen the app that you take a picture and then they calculate the shape, everything. In terms of macronutrient, macronutrient. If you can incorporate that into your system and then they know the pattern of diet, apply and do, that would be a good thing.

That would be great, right?

For example, like... This week, in case you're not eating a lot of greens, they might notice the client that's okay. This week, eating greens seem to be too slow. Maybe add a little bit more greens this week.

Something like that. Give some advice, right? Some advice. Or are you consuming too much?

In case the goal of the client is waste management, right?

You seem to consume too much.

Maybe we can discuss something like that. dense nutrients Void pasta most are add, you know, okay, no sauce. Yeah I have one For me I prefer complex complicated thing in a simple way right okay when it comes to diet Everyone likes to calculate, I don't like that. Because it's not accurate. Somehow it's not accurate. The simple way, but it's... Practical is taking a picture, every picture, and then we analyze for picture.

I think I have to have... Actually, I tried to replicate this app for my Oh, it's resetting. I haven't... This is the F-Core foot view. Foot view, okay. What you do is like--Hey, just take a picture and they tell you, right?

Take a picture. Yeah. This is very simple version.

You take a picture, And then They will add automatically into the date and time. How did you do this? Uh, basically the apps. Not your app? Not my app. Okay. This is the app that I downloaded. Okay. But you know, this is very good app. And I believe on technical, like technical,So the first site is very easy for you. The way they do is the first page, They let them take a picture. But you need to know the nutrients, right?

Like how do you know? Yeah, sorry. What's in there? Normally when I ask the patient to take a picture, they keep it in the album, right? Okay. In the photo album, but I think it's not good. Right. This, they keep it automatically in their system. Oh. Okay, not in my phone. So, and then if we have this information, palm, dead, picture, we can calculate. We can calculate calories, you see, for the whole day.

Let me try it with Chloe. Um...

I'm drinking, what do you want to know? How many calories, vitamins?

I just don't care. You can add anything you want. Keri, what do you mean? And my code in print, my code in print. What's the micro?

What are the micros? What are the micros? I don't know if you can do it. I have no idea.

Let's see how much you can do. Call me, right? Call me, yeah. It's open call. What a miracle. Okay, interesting.

Stay pink. Be paying now. My angry butt.

It takes too much time. Yes. Just vitamin D. It should not be that long. Because it's deep search, right? One... Is this accurate? It sounds a bit low. 190, yeah, it's a bit low. Protein 28. It's not bad. It's bad because you see it? He probably did the web search. I think he's probably from the web search. Veggie high protein activity.

I think what would be interesting, I'm sorry, I think what would be more interesting is... No, I think this one.

Okay. You better try this one.

No, I think food, not drinks, food.

Yeah, let's see what's inside. Uh. Yeah, but how can you know, you need to say it. Yeah, I want to, How good the podcast was inside. Because as a doctor, you see, I have to I have to try to understand what inside.

What's this? I think it's where we get coffee or whatever. That's right. What's this? I actually want to try So food I want to know out of the box how much does he know about food? How about my kids eating pasta, what do you think? Should we ask? Make your eating pasta. Let's try it. What is it? Ice Latte from Starbucks. No, yeah, because he saw that cup. I think it's the ice lady. Yeah. Can you guess?

Or estimate the micros. Can you estimateMicros. for each plate I think we need to use another mode, I believe it's possible.

For me, I don't think we need to. Oh my god!

Is this accurate?

That's actually pretty accurate. Let me see. Let me try to use my own knowledge. A big portion. What is that? It's his pen. It's his pen. Okay.

Oh my god, that's pretty good.

It's not perfect, but it's... Not perfect, but... Like I said, you don't have to worry about accuracy, 100% accuracy. Even when you try to count calories, it's not accurate. Okay? It's not accurate. But you can estimate. And if you do it, like, In the big picture, like more frequent, in different pictures, different meals, different days, you will get estimation of your meal. And that's good enough.

So if you think about your app and you can do something like this. Client can take a picture of their meal.

No, but how about a chat?

Like I want to project with chat. You think about the chat, right? If you don't make the separate section for uploading the picture, they will ask The bot. for the time that they want to know, right? But if you request them to do the whole day of the meal, they will get the full information. of the meal. Like color, calories. The boat can do that. Yeah, but you have to decide this kind of system. It's like MyFitnessPal, something like that.

Because the thing is like, I think to me the innovation in OpenFlow is the fact that you don't have to do design, it's a chat. You're just chatting with the bot.

Yeah, but chat is kind of like you have to input the information first, right? You have to, the client has to input the picture. Yeah. And ask, okay, what is that, what the carry? No, it doesn't have, you just dump.

I think even the bot can be like, hey, it's lunch, don't forget to send me your picture.

And then you send the picture, and then the bot gives resume and then you can send a message uh at 8 p.m it's like hey this is uh this is your resume of what you had today yeah but for me i think it's kind of like not not not well organized when you do everything in the chat form uh tech form is kind of like when you have a special question you do it in the chat but in general if you want to make sure you get the complete information of clients diet you have to to make a separate sectionThat, okay.

I think the chat is from the patient point of view. For the doctor, I can do a webpage where you have all the picture and all the macro, like I can organize that well. But I think for the user, it's easier to just send stuff to a chat.

Maybe both I think.

But the doctor can have a back-end and even the user can share.

For doctor I prefer this one because you can check all the diets. But for kind side I think thisWell organized and they can review their own diet.

The problem is if it's boring, if it's boring people are not gonna use it.

Maybe it need to be like The combination of two parts. When you do it in the bot,Automatically send to the app. You can chat with the bot and then they send it to here. Something like that, same.

Yeah. Yeah, that could work too.

Diet, exercise. sleeve, okay that's the part of input And then bread pastry, sugar, that you have to make sure on your app.

Because the problem of the app is I feel like people-It's difficult to make an app and people don't want to use them. Like I hate using apps personally. And I feel like, you know, if it's a chat, it's just so much more fun because you feel like you're chatting with someone, you know? You're just like, "Hey, do this, do that."Can try I guess.

It depends. It depends on personality. For me, I don't use... Da. I do chat to ask for information. I will go to the apps because I like to organize my things. So I do everything in my app. That's the dedicated for my needs. For example, I have the app for diet, I use that for my needs. The app for lactate, I use that for my needs. Something like that. But if it's into the chat site, then automatically upload to my app, that would be perfect.

Okay, yep, I think we can start. For me, If I look at the Yeah, I think it's good enough. The rip-off is good. but too much information.

Two.

But... Yeah, I think James and I are working better when compared with the previous, last time I used them.

Perplexity is a bit of, yeah, perplexity is a bit dying actually. The best search, so if you want to do AI research right now, the best one is Ciao GPT and Gemini. Thanks for your publicity, Slave. falling behind because of the complexity. I think they lack funding. You know, Google and OpenAI, they have unlimited-That's why they keep-Yeah, yeah, yeah. And so, okay, so... Yes, so the bots, and then...

I guess the question is, Do you want the butt? So, okay, so... It's just finished on the bot because I feel like it's a big topic right now. Bot or app, you think the use case could be really good for people to constantly upload what they eat, but that's for weight management. And then asking questions about food, I guess. Which one should I eat or something like that. I think that's more of the...

I think that's what could be fun, you know. Let's say somebody's like, oh, I'm hungry. Okay, there's two dishes in front of me. Which one should I take, you know? And the butcher's like, okay, you should take that one. Don't forget to send me a picture. They send a picture, you know. Another The idea would be for the result delivery. Instead of getting them in the app, maybe we couldYeah, but I think it's better to be visual in an application, right?

I think chat is not great for that.

Yeah, actually you're right that Many people prefer doing chat, but at this point, I think the chat is smart enough to gather all the data and put it, organize it into the app automatically. If you can do that, I think that would be a good advantage. Because people are not very organized, right? Not very organized, but they want organized information. So when they--Yeah, so the chat is like messy, you just send.

Yeah, messy and then it's summarized into the app. I think that would be good. And the app is like, okay, you should review. Actually, even the chat can say, hey, Can even send a link to the app and I think what's what's what's I mean the important aspect of the bot is that There is a daily interaction, so it's easier for building a relationship because the problem is if we do a blood test, And then that's it.

They look at the result and then they just forget about us. Well I think if they keep interacting, it's easier for the bot to say, "Hey, by the way, do you wanna buy some supplements, "or do you wanna do another test?" That's really good upsell. Really good to keep the relationship.

Maybe use, you can use a chat as a way to say, Main gateway for interaction. And then use the app as the organization book, something like that. Yeah, I think that's a good way actually.

Yeah, let's try, okay. I'm gonna do some prototype. You know what, I'm gonna do some prototype. I'm going to do some product. I'm going to make a new line.

Yeah, for example, if I do the black test, right? Okay, there are some problem. Yeah. There are, there are, there are, like, cholesterol. Okay, I know I have cholesterol problems, but if there is no one, remind me about that, I forget. I forget about my problem. And then in the next two months, three months, I forget everything.

This is the nature of us. But if you do the test, and then the AI helps to screen for the problem and then interact with us automatically. Like, for example, they might remind us this is already one month, already one week after you get the result. What did you do? What did you do in the last two weeks? Just let me know so I can help to recommend the diet, something like that. Good. In case in case the client Oh.

Answer the question from bot. That means they are interested in taking care of themselves. So it's higher potential for customer with video apps.

Are you using the bot to sell?

Yeah, using BATU, not 2-cell, to be an assist for health.

Yeah. You have to make sure it's not too full chat. The problem about chat is if it's too much. They're not gonna use it. Remind too much or give too much content, give too much information at the same time.

For example, remind every day, not good.

But maybe, for example, if you have the picture of the meal, maybe after one week, the client didn't upload any picture, they would say, okay, I didn't see any of your meal, you want to share some of your dish, something like that. As a reminder. Yeah, it'd be great. And they might have to learn if there is no reply after one to two texts. Just keep it silent for a few times and then remind again. Something like that.

You think this is possible?

I think so, yeah. Everything is possible.

It's kind of like, as an assistant, like hospital assistant, we use a hat to interact with the patient. We don't just use a stick for the fall.

Yeah, no need to reach it. So I'm actually, funny you mentioned this, I'm looking, so right now what I'm looking for is some small product that I could be doing For body cipher that do not require No medical advice because the problem is If I want to do medical, I need a clinic, I need a telemedicine license, blah, blah, blah. It's very difficult actually. So I'm talking with a lawyer now to do the research, but it's very time consuming as you know.

And so I'm thinking I would like to start To find some ideas that's like kind of fun and also do not require Not medical advice, right? So I'm thinking having a chatbot like this just remind you, you know, I can do a line account and be like, just somebody to like, eat healthy chatbot or something, you know? And just remind you, like, hey, um... Did you eat healthy today and then... Just remind people, you know, and then they send picture and then I give them the macro.

I said, this is really good for cholesterol. And then I can just ask my friend to use it, you know? Just a small group, but at least we get something, you know? It's good because then we can see the metrics, we can see how often people talk to the bot, This is like, it's good data, you know, just to get a feeling. Um... Another thing I was thinking to do is So, okay. Let's review the whole pipeline.

So the idea is like, if somebody want to do a blood test So right now we have several questions, right? It's like, okay, why do you want a blood test? What is your goal? Yeah. So what I'm thinking to do is actually So what people do right now is they go to ChargeGPT, they say, "Okay, I haven't done a checkup for a long time. "I wanna do blood test, what should I test?" Or, "I'm 40, my energy is low, what should I test?" They give things like that, then ChargeGPT give the list of tests.

And then they go to PathLab or N Health with those tests. Like this is what's happening now, more and more. Um... So that's okay. Do the test. Then they get the result and then chat GPT again, he's like, "Okay, help me interpret." So several issues here is like first of all the What ChachiPT says to test isSometimes not so great, maybe missing some stuff, maybe some stuff useless, maybe some stuff are very expensive in Thailand because you know, Chajipiti is mostly like American.

Um... So I'm thinking I could do just a page or maybe a group where We would design a few blood tests depending on different use case. Let's say, oh, you just wanna check up replacement. Okay, you should do this one. You just want to... Optimize your supplements. Somebody take a lot of supplements, so I only care about antioxidant. But for example, I don't want to do glucose, insulin, I don't care, don't do it.

So you do this one. You know what I mean? We can have three or four packages, We just give the list So people can go to Enhealth and then be like, okay. And then we can also give the price. It's gonna cost 6,000 or something.

So you mean you're not doing the test yourself, right?

We're just giving the list of markers to check, yeah.

And they can go directly to Enhealth? Yeah. Okay.

Mm-hmm. The reason for that is that Because we make a community, so I can ask people, "Oh, you want to do this? Okay, give me your email and I'll send you the list." That way I capture email. I capture email and I capture email of potential customer. So I can, yeah, you know? Because I know that tomorrow is like, hey, now the product is ready, now we can send a nurse to your home, you know?

Oh, you mean like you...

You still want to haveHome test for your service, right? Yeah.

So, with the nurse. Yes, I think it's very important.

Um...

Yeah, I think it's... I think it's the same, it's similar to I don't remember.

Like the lab? No, not the lab.

It's like middlemen for SD-Mall, something like that. You work as an SD-Mall. But the way they look at the information is different.

But SD-Mall is more like for the lab to advertise their package.

Yeah. Actually, your concept is pretty much the same. Because at the moment, if you don't want to do lab tests yourself, you already have the package. Okay. Yeah, but but they do themselves right they do themselves. Yeah getting any From them correct at this moment. It's kind of like you do it for free. Yeah, but it's the same concept Yeah, but SD mall they do it with Commission. Yeah, okay something like that.

Yeah, but the different gateway is SDMall, they do the search by themselves, and then check the packets and shoot the packets by themselves, do their own research. But for your case, you would give AI-generated information and recommendations.

Why not AI actually, your recommendation.

Oh, okay.

You tell me about the initial step, when the client comes, what is the... What is the step?

Come to your app, okay. I think it just be a website for beginning.

Okay, yeah, let's start for the website.

No, so it's more--I think, sorry, because I don't want to make it confusing for you. Yeah. So let's say version one. It's a version one, right? So version one is I stay at home. You can't actually move it huh?

Yeah, I look at it more to compare with your service. Do you have any service that can go read my web browser tab and help me organize or summarize everything.

Do you have any app recommendations? I think Cluedo. Yeah, cloud has it. You need to install the cloud plugin. Actually, I tried, but not working.

They cannot read all of them. It's too much.

They just leave 10 of them and then they stop reading it.

Only code, right? I think for this you should use another browser. You can try Comet.

Comet from Perfect City, right? I haven't used it myself.

But now I use Microsoft Edge as a main browser. Yeah, then though, So a lot of taps here.

Okay, let's try to resume, I think, let's do a little bit of product now. Yeah. I think it'd be easier. So let's decide. So version one. Version one is,ideal product and let's say we copy function health okay So it's functional health, In Thailand. Yeah. That's version one. Okay. So function healthy on tiling. Okay, so customer first of all need to Uh... SelectPackage, right? Mm-hmm. So We can have multiple package.

Maybe we will have like 10,000-BAT package, maybe you have 20,000-BAT package, and maybe some add-on, let's say cancer detection or something. So it would be select package. Plus I don't Right? And then, and then the pain. So you need to know what to test. So this is kind of like what--Do what, right? What to test? What you taste? Okay, and then the pain. Okay, you pay money. Um... Okay, and then the nurse.

Nurse at home to take the blood. Or they go to lab. Right, good to know. Maybe the nurse would be like extra 1000 baht? How much does he cost in your stakes draft?

One thousand? 1,800 to 1,000.

So, let's say we're really good at logistics, so we can do 1000, right? Good to the lab. Okay, take the blood. And then... Uh... And then you get the The raw lab results, right? And then you get the roll-up results. Bye. What we would do better is that you would do the result in the app. So I guess You will get like per organ In the app, yeah, okay, in the app. So maybe you would have like some nice graph.

Um. You know visual Maybe like 20% or whatever. This is supposed to be a graph. You know, it looks cool, pretty much. Okay. the rollout result and then The final step would be the action plan. And action Ben, right? So some of them they use AI to generate. And some of them, they call theseKlinician note, cleaning. Shen knows. So it could be AI assisted, let's say, or doctor, doesn't matter, right? But that's an action plan.

Details doesn't matter so much. Okay, and then once you have your action plan, then we have obviously all of the upsell. So Epsil would be supplements. Hmm.

Yep, supplement orHmm, of course. You think coaching is up-sells?

Yeah, anything they pay after the blood test. Yes. What kind of coaching?

Kind of like the, like coaching for a restaurant management, coaching for a diet. Will you be paying extra or like? Yeah, pay extra for consultations and things like that. Okay. Yeah, but you're, Yeah, that's a... It can be anything related with lifestyle.

Right, okay. So let's say coaching. I think coaching is more like day-to-day coaching, but I mean the big one.

Yeah, because coaching is not just about health. It can be mental health too, right? Right. Just physical health.

And then I'm going to put supplements And so supplements I think is a big one. So we can either just do e-commerce, like we sell, we have our own marketplace, or we do custom. -We want to capture that, right? We could just tell them, okay, that's where you should take. You can go to iHerb and maybe we have our own shop and we sell the prices the same as iHerb. So you can buy from iHerb or you can buy from us, doesn't matter.

That's your supplements, right? Uh... Okay, let's resume. So, V1, function health in Thailand. Well, I see it's a bit more, but that's what they're trying to do, right? Select the package. So obviously select package we should try to Maybe here there should be some questionnaire trying to qualify the person. It's like, okay, what is your goal? Okay.

What, what, What do you think about making it A little bit different, instead of using generic questionnaire, you use AI. Okay. To make it like... You show me this one, right? This one, I really like that. If you... If your first piece is like this Tell me about your health concern and what test you want to check. and then they will auto-generate the recommendation by looking at your your packet that you keep it in your database.

Something like that. So they don't have to answer all the questions and spend time for answer questionnaires. Right. You just tell that I want to do the blood test for my sugar problem. Right. And I have sleep issue. Right. But you just Let them know they can tell anything about their health as long as they want. Right. What do you think?

I can try, I think the--No one doing that. I think the survey, like, I think if it can be a survey, I think I like survey better, personally, because it's just faster. The problem with chat is, like, sometimes it's a bit slow. And if it's, like, what is your gender? There's only two answers, you know? I think it's more like, "Okay, what did you eat today?" Then this can be a survey, right? It has to be a chatbot.

What about the problem that can ask missing information automatically? Yes, this could do. For example, I might tell that, "Okay, I want to do a basic metabolic test." The information is very short, right? So the AI asks the following question automatically, "What's your age? What's your gender?" So it's kind of like interactive chat. I don't like to to do the survey because I think it's too simple and it might not care.

It has to be short. To me, I think there should be a short survey and then some And then maybe later AI take over. But it has to be a little bit at least, right? The problem is for the selecting packages is people don't know. And I think it's better to be like, okay, those are the things we can help you with. Which one do you want to help? Wait for us.

Yeah. After that, the AI would act something else, like beside your sleep, you have any problem with your body weight, something like that. And it would be more human interaction.

I believe it's not too difficult.

Yeah, I can look into this. I mean, I can show you some projects after.

And because here, I think it's the gateway that you have to... to like Hmm. how to say it, make the client interested in continuing.

Yeah. Yeah. So I'm gonna call this a qualifying goal. Yeah. So it's usually I will survey your chat.

Let me look at S O for functional health Yeah, you can see the...

They ask you to pay right away. Actually, you can try. Better with your Steve. I think functional health, look at super power.

Oh, they copy each other, right?

No, but functional health, I think a little bit old-fashioned. I think super power is more high-tech. Okay, super power. Yeah. I shouldn't have, it's really too old school. Super spot. Is that getting?

It's a common website I go. Let's say I'll try, right? Yeah.

Oh wow, right away, bing.

Question, if I want to go to question then?

Oh, Trey, Poo Poo Dreamer, Trey. They're gonna send you some, uh... So they said right away, okay, 200, that's it. That's the membership.

Oh, that too. What about questionnaire? I have to... I think you have to, yeah. Oh, not good.

Actually, if you want...

Wait, wait, sorry, can you put it back to... Did they ask you to pay right away? Yeah.

Not good, not good. Too much.

It's father to...

to give the information before getting anything else. Yeah, I believe.

Yeah, sorry, can you put again your email? Yeah, they have more. They have more. With zip code, phone, payment. I saw you pay right away.

Yeah, yeah. So this one is like they cut... They want to very focused on the potential client. If for me I'm not sure about the package, I just stop scoring.

Yeah, but because there's no custom package here. It's like the, there's one membership. Functional help. And then you do add-on. Actually like that, I think I'm gonna do the same.

Yeah, if you want, let's say like doing this thing, because we're talking about the gateway, right, questionnaire.

Oh, they do the same thing actually. Yeah. You see. And what about questionnaire?

What about questionnaire? I think it's after you pay.

That's okay. Yeah.

Okay, what do you think? Doing this thing and start the survey first.

Honestly, I would do the same, pay. Just pay right away. Pay right away, right? Because the thing is, if you have question, that's before then. You can click on what we test, scan, you can look, they have a lot of marketing content. That's okay, so you can learn for yourself.

But especially when you want to work. to personalize the test. for the client.

What do you do? So because now we So there's no pay right? You have to pay but pay for the basic membership first right?

Yeah. And then you can upgrade. And then you can have add-on but I think everybody has to get the membership first. Because it's the membership base.

Okay.

But I think actually... I was considering this, but I think it makes sense because If you want to integrate AI and stuff like that, you need margin.

Yeah.

Let me check something You have to have You have to make sure you already have the client, right? So they know your service, then they can register right away.

That's the marketing of this, yeah.

Yeah, we have to do the marketing first. Yes.

It would be cells. OK.

okay this is the first version you can continue with the second version no before that so that's why I want this because I don't want you to be confused this is the goal okay okay let me show you this this very common you've seen that before right no this is an example of the common types of website okay they are they say like online exercise program okay and the first page is they are to Something like this?

Yeah, well, everything is air generated.

Yeah. Yeah. Something like this? Oh my god, so long. 42 questions? Yeah. Oh my god.

Let's say that. I'll do it. You see, you like survey. You see, this is faster than chatting to a bot, right? Like, bang, bang, bang, bang. Not really.

Not really. For example, if we do the same thing but in only one box, and I list, okay, I'm male, I'm... Okay, it would be faster, but it's okay. It's acceptable. Okay, let's say... Like it is like. Like it. Like, like, like, like, like.

I hate this. Okay. I didn't delete it.

Okay, I get something like Quiz workout 80.

Oof! Actually, this is good. I should do this in the app.

Yeah, yeah. That's the reason I'm asking about what you want to do. You want to do this kind of thing first, either AI or P. Let's see.

Let's have a goal. Click goal. I think click goal is good to communicate to everybody. Yep. Oh my god.

Okay, 80%. Oh my god, you see? Too much, too much now, they say. Okay, wait, please wait. Be patient, be patient.

It's kind of like normal question that--Do you know this website or is it a random website?

Random website. I believe they use the same hat form because they do the same thing.

Everyone do the same thing. Yeah, I mean this is computer. Maybe they have the company doing the template. Okay, short term... Because everyone doing the same thing. I don't believe that they copy each other. Maybe they use the platform, the templates. And how many questions is depend on? You see the ants start to act mean. Okay.

Alright, it's a scam. Don't put your credit card in. People say it's a scam.

Yeah, but anyway.

Okay, just stop at this email. They asked me email. So this kind of thing. And then when we finish, right, when we finish, they would give the recommendation of the package. Yeah. Like two, three different package and then we can select either package. Right. If we want something like that. But for me, I don't like, as a customer, I don't like to put any private information like email first. If I don't touch in the service, right?

So maybe you recommend the package and I select the package. And then after that, we put the information. I think that would be much safer for the client.

Yeah. Yeah, I mean payment probably less. I would say email first and then maybe some question and then payment.

You can do email first like this but you have to to know the company, right? You put an email, you put your bio, your credit card information. You need a lot of trust to start from this. Yeah. Okay. But it's Dr. Hyman, right? I think this one is one of the most successful companies.

Number one. Number one. Okay. Yep, okay, you can continue.

Okay, so V1 supplement of cells. So this is like I would say this is like in two years. So this is like two years ago. Probably. So that's 2028. So basically a function that I don't know if you can get, right? So we qualify, select the package, Hey, let's come to your home. Then you get the robot result in the app and then after all the results came you get an action plan. Plus, Doctor, maybe... either clinician note or maybe a consulting consultation.

Actually a lot of appA lot of people ask for consultation, like when you have all of the results, they want to talk to a real doctor at least 30 minutes. This is something I see like as a video call.

That's what I've been doing in my lab.

Right. So this will probably actually do a clinician note. I'm going to say a call. Do you do video or just call? depend But I checked the review And most of the apps that don't do the doctor call, people complain. They want to talk to someone. So anyway, we can do this. That's why I think you mentioned telehealth, right? So that's the problem in Thailand is like you need a license to do a...

Can you do a call with the doctor? Do you need a license for that? A license for what?

Telemedicine. No, don't need.

I need, but... They're not very strict, so I don't need it. So I can call the patient I can video call with so with anything? Yeah. No problem.

Do you mean we need it eventually, but maybe not in the beginning?

If it's big enough, like the big hospital, we have to have the system established for telemedicine. But the first phase, I don't think we need that. It's too much work to do.

So I actually played Gleician Call, and then after that we tried some upsells, so maybe coaching, supplements, but the upsell need to be subtle, right? Like it shouldn't be like too strong. Anyway. Yeah, yeah, yeah. This is like longevity 2.0.

Okay, so which one is the The main service, I mean the key service.

What is the key service?

The key service. So... Yeah, the key selling point, right?

So I think, I mean, key service, like if people ask what do you do, okay, in one sentence, what is your service?

Oh, what do you do? We do action plan. We do action plan based on blood test.

So, interpretation, right? Yeah. Okay. I think that's the value. Okay, so lab analysis. Interpretation.

Interpretation. So the value, so I mean, What do you think would be the value of in-dev service compared to what you see currently with the medical system in Thailand for longevity?

Yeah, it would be the same. Interpretation and action plan.

Yeah, I think so.

Nurse actually, I don't know if something--Nurse I think is not the key advantage because the client might request nurse or might not, right? Because if they go to in health directly, they might not request your service.

No, but I think people don't want to go to head health is what I'm saying. I think one of the problem is currently is like you need to go to the clinic.

Okay, so this case you would order the test for the client, right?

So I think one of the saying point for some people is like everything is online. You never go to the clinic.

Yeah, but you contact with in health, right? You deal with inhale for the lab test. What do you mean? You tell me about letting the client go directly to the lab and do the test and then give the result back to you and then you analyze it.

No, this forget it. Forget about this.

Focus on V1. This V1 is the same, right? So you do everything as a clinic.

Yes. Okay.

So So V1 is the person never see a clinic, never go to a clinic.

So as a clinic, I think Nurse at Home is a good plus for this. Right. Especially for expats, they don't have much time to do the test.

Yeah, they don't want to go to the clinic. So I think one selling point is like the fact that because the problem with a lot of clinic in Thailand is that even though you can do the blood test at home, you still need to go there at least once to see the doctor.

So I would sayFodbeast? The key... The key service, I mean the main service is home test. is hold shake up.

Okay.

Not lab analysis, not lab integration. The key service is home test.

What do you mean by key service?

Key service mean like what do you do? You do home test for the client. You do lab test for the client. Is it? Because you provide lab test. Yeah. Like then you deal with the labs. Yeah. To get the lab result. So this is, for me I think for version one, your main service Let's test. Your method is not lab interpretation.

That integration is just an extra plot for that. Okay, so you think this is V2? This is what I think. I mean this we can do manually, right?

Do. I think it's not too hard. Do you think it's hard to make an action plan?

No, no, no.

You can make action plan, but the key service still left here. You can sum these up together, like leftist and the occupation. Yeah, let's, I think--But let's say, if you say v2 is like--Let's say value, I think value, because the thing is like,Okay, key value, right?

Keys, okay, maybe it's the keys.

I don't wanna pick just one because it's just you and me opinion, and I want the customer to say what's the best. So I think we can only say, I think this is good, I think this is good, I think this is good, and then we will ask people, okay, what, You know what I mean? So, Let's say main value proposition in my opinion would be nurse at home so you never have to go to the clinic and the application.

So nurse at home and application I guess. Yeah, you get a result in the app rather than email. I think people hate email PDF, really ugly. And then the action plan. Uh... Yeah, I think action plan is-Obviously the main one because action plan is both what you do as well as which supplement you take. A lot of people ask about supplements, so it's another thing. But this is something that we have to, that's why I want to talk to customers as soon as possible because I wanna know why they wanna do those tests, right?

Some people is because they take a lot of supplements. And so they want to optimizeThe dose? For some people, It is... Um What was the other one? Yeah, I guess someone's supposed to be right here. So, at home, application, action plan, supplements, recommendation. Yeah, would you agree on this? Like four setting points? Can we do better than others?

From four different points, which one do you believe you can do better than others?

I did, yeah, all of them. All of them.

The first one, how? how will you do to make it better than other people? Home test.

Home tastes better than others.

Because you use handheld, everyone use handheld. You use NERSC, everyone use NERSC. Um...

So... Okay, I mean better than others, we don't have to be like the best in Thailand, but we have to be like in the top.

Yeah, yeah. Any, Any-Anything that you think you're better than other people. On the first one. Priced?

I think price, you never want to be better on price.

So, from this case, if you cannot imagine what makes it better, so you just leave it as like,Part of the survey.

Yeah. I think the next one is the thing that need to be emphasized.

Okay, because you compare it to your own clinic, right? So because you think a lot of people do have nurse at home, Actually, not all the hospitals. Like there's a hospital, I have to go there. Like even [[bdms-wellness|BDMS]], I have to go there.

As we discussed before about comparison, I don't think you need to compare with hospital because the people who go to the hospital, happy to go to the hospital. They don't worry about home tests. Okay, different I think different customer. Okay, so People who do that the test at home either person who usually go to the clinic, right?

It's easy more convenient, but Home test is a little bit more a little bit more. Yeah, something like that, but Everyone doing that for me. I think because you don't have your own laughs. You don't have your own nurse at the moment, right?

Yeah, so this might not be the key the service that everyone do and then you can back it into your service. Right. Okay. So for me, I think we can move to the next one and make it better because lab interpretation is the one that you can do better than other people. Yes.

So, I mean, first of all, having an application, I guess, is better than PDF. Would you agree to this? Yeah, yeah, yeah. And then the action plan... So I guess, okay, if we have to rank them, the biggest would probably be this one.

Yeah, yeah.

And then second two would be what, this one maybe?

What is that? App application? The fact that we have an application instead of PDF. I think it's kind of like...

Hmm. You think it's separate, right?

It's separate, right?

Yeah, because some app I can show-I haven't show you some product. Some application, they have the-Like Health Matters, right? They have application. They have application.

But they don't have action plan. Okay, we can separate.

So maybe this one, number two. And then supplementary accumulation, I think. I guess it's part of the action plan, but still.

Yeah, but I think it's still in the future, right? Because...

I think this is actually more important. Actually, I don't think I see any of this. Application nowadays, you know, people are just not so swayed. And then I guess this is more like a requirement. Yeah. And then package add-on qualifies to a VP. Application, I guess application is also that part, I guess, would be part of the app. The fact that It's all online. Most clinics right now, you see an ad You talk online and then you have to call them and say: "Okay, can you come to the clinic?" Whereas like, We will try to do everything online, you know, like really nice package, questionnaire, you know, covert people.

Like, you know, like we, ideally people pay with never going to the clinic. I think that is a key, that's a key success. Which I guess... I guess give me another one, right? Setting point for some people is that you never go to the clinic. I guess it's the same kind of like together. Okay, so you asked me what can we do better than other clinic? It's like, yeah, so actually not only the nurse, but actually you never go to the clinic.

Okay, so like 100% online. 100% online, yeah.

I think for some people it's important. Obviously it's hard to differentiate because like you said there's many If it's online then you know there's many services but maybe some day I'll see.

In my experience in Thai clients, sometimes they don't They don't use online platform. They just call, they just text something like that and request for the test. But I'm not sure about your market, about XPath. I think this is a thing that you have to survey with the real clients to see if it's the real need. And for the tech customer, you say they... You remember I told you I had the platform for online lab tests but they don't use his dashboard.

They just call. When they see the package on the website, they just call. "Do you provide this package?" "How do they do the test?" And then everything right after that is offline. Skype Live chat confirmed with the nurse call, something like that. It's not fully online service. Still need some person to talk with the patient.

Yeah, yeah, no, but that's still online.

And most of them prefer, not prefer doing that way. So they move out from the platform to the platform.

to make a call or something.

I mean, in my opinion, the call would be here. Like, okay, sure, you can call, but it's like, okay, then you have to go on our website. Yeah, yeah, but--I mean, we can create the account for them. You can have a way, if somebody call, we will have a way, it's like, okay, what's your email? And then you kind of create the account for them, but then you kind of try to send them directly to the pipeline.

Oh yeah, yeah, it's possible.

For payment, it's like, oh, for payment, you need to, okay, I will send you the payment link, for example.

You say, oh, I'll send you the payment link. So from the phone call, they end up here directly, and then everything is automated from there, you know? Okay. Yeah. But yeah, that's how we work. And so, yeah, I guess the same point is the action plan, I guess. Action plan. The Superman recommendation, everything in the app, you know, and you never have to see us. I think this is good. Sorry, I mean, I want to try some of these things because I know that you know for you Because you're a doctor, you have a clinic, so you used to go to the hospital.

I mean, you go to the hospital every day.

No, no, I'm not thinking as a doctor. I'm thinking as a... And the typical clients that I have seen and this is the pattern that I see. I cannot say it's inside because it's not representing the whole population.

It's biased because the people you see are the people who like the good news.

So I think the only way we know is we have to go to the market to survey. You do the product and then you do the survey. That's the way we can modify. I think it's the first draft that you can start with.

So now the question is okay, so if we kind of agree on the big picture, this is like the same as a two year plan Okay, now the question is when we begin.

Okay, which one is the first year? Yes.

Which one is the first six months? Okay, that's good. So Let's remove actually what's legally difficult. So let's do six months here. We can do a full delivery. Because now I'm talking with the lawyer, it's going to take some time. So we can avoid some-so actually, Application. Cannot. I think application, I will need a company to hold the patent and to have a contract with your clinic. I think it's going to be taking some time, right?

So it could be this year, maybe like towards the end of the year. So this has to wait. This has to wait. I think it's just legally too difficult. Nurse at home, I guess same reason. Well actually... I mean, how much can we do with your clinic?

Actually, uh...

Can we do the whole project with your clinic? Yeah, actually you can do everything. If you plug in with the clinic, you can do everything. Yeah, it will. You can do it from the beginning to the end. Even supplement recommendation, but you're not gonna get like 100% Can you do the application though?

I think I asked the lawyer, I think he said for the application it needs to be separate from the clinic. Um... I think that's the only thing we're gonna do.

I'm not sure, you have to. How do you say separate from the clinic?

Two different entities, yeah.

So it cannot be the application used for the clinic? So that all the, it cannot be the application that can clinic use, right?

So, I mean, it depends. Obviously, there are many different ways, but the lawyer recommended me to separate the application from the clinic so that way the application can work with multiple clinics. Yeah And also legally Because if you're on top, then let's say if the clinic has some mistake or something happened or whatever, the application can say, you know, it's not my fault, it's the partner clinic.

I mean, it's just like a legal protection or whatever they call that. Mm-hmm, mm-hmm.

Oh yeah, it's true, it's true. Actually, it's true, but...

I mean, it's not, I'm not planning to work with you. But, but...

For me, either having application or not having application, for example, if you partner with my clinic, we have to share our responsibility, you know, right? Either with or without application. So for me, I don't think application is the thing that you need to be concerned. Because application is just a tool for clinic to use to take care of the patient, take care of the client. I'm not really sure why they say it should be separate.

If it's separate in the way that you won't take any responsibility for the interpretation, okay, it makes sense. I think that's the goal, yeah.

And also scaling if tomorrow we have 1,000 customers.

And you do the application and then you sell the application to the clinics, something like that, right?

Not really sell, it's more like, okay, it's like, hey, I have a thousand customers that just registered, I need to analyze the blood test, so I need like a big clinic that can handle the weight or I don't know.

Yeah, but okay, what is your thought if there is no application, so what is the service that you would like to start?

Okay, so what we can start, so, okay, so let me one, so, What I was saying is maybe we could recommend people somewhere here, right? So we could make a web page where you do some kind of survey or some chat and then we recommend new packages. And then the same stuff there, no payments. Like we just, so what I was saying earlier,Um.

Let's say it's a test run to see So this now is like prototype, okay?

Mm-hmm. Thank you. So what I did could be just these two. So basically we have just the website. Why is it so bad? Where you can qualify so you do maybe a survey or some questions. Or maybe not, maybe we just show different comparison, you know, blah blah blah, and this is like 5000 And this is like, we recommend this blah blah blah, and this is like, 10,000 euros. Just a comparison I mean, ideally we hide the price and we ask people to give me the email.

So that way we just get email and we get people to talk about it. Okay.

so So for your prototype, you don't worry about revenue, right? You just do it for free, let's say? Yeah, get customer. Get customer, okay. Okay. Okay, you wait for it. -No, I don't have it.

Okay, may I go to the toilet? Yes.

We have to move to 27B. Because of these nice people. What's the plan in the afternoon? Work on these more. I need to... So I'm done with the research. Yeah, let me check and show you everything today. We move now? Yeah. Yeah, anyway, for the project, it's actually, it's okay. Like, we don't need to talk too much about it. Let's focus on the blood interpretation with AI today. I think it's enough.

So in this case, you said that you want to try experiment with your interpretation. I think that makes sense. You said you don't want to-Like to the kind to pay for anything I think it's good to start to see the perception of the market right to see how And then...

Oh, you mean the idea...

Yeah, the second idea, that you just do interpretation, right?

Yeah, because the idea is like... But for the nurse, what do you think?

What do you mean?

Yeah, maybe you're right. Let's wait. Let's talk to some people how important the nurse is. Maybe you're right because I thought, yeah, maybe people don't care if they go to the lab. I actually know a lot of people who go to that lab. I think the problem is I really want to eat and health. But the problem is Any Health don't have any branch in Socovite. And that's a big issue for people because they won't close.

And so actually, Pathlab is very popular. Because they have a branch right here You know that branch, right?

Yeah.

So everybody go there. I mean everybody.

I'm not sure about the private, they give very good price now, or do they do that? I'm not sure. Very good price.

Random, they don't do the test.

They just random the results. Just random numbers. Just AI.

These are funny, but it's possible I know how do I can we check this yeah We cannot.

Lab Nisau is just a random thing.

But do you think they are reputable? Oh my god, I have no idea where the bee is Let's just walk I guess And how about bria? You think bria is...

Yeah, I mean it's a good one.

And you think Pathlab is good? Yeah, yeah.

So they will not be cheating?

No, not this one. So you mean N Health, N Health plus Labria. All three are pretty good.

It's not work because when they have a lot of customer, they can run the test. almost zero cost, so there is no reason for them to cheat.

Okay, sorry, I need to pee. Can you do it for me? Okay 35 minutes. Okay, no problem. Let's review one research. And then we do blood interruption. I mean, it's, well, okay. 27D, oh my God, is it gonna work this time?

It's gonna work the same room, no. Last time you did that. Oh, you're right.

First time, look at that. So nice when he works. Okay. Screen mirroring though. Okay. So this one. Here. Okay, what did I do? Oh no, I didn't do... Oh no, I didn't do Gemini. You're right. I think Gemini, I don't like, I think Gemini is writing too much.

Yeah, it's writing too much.

Yes. So actually, so my test... I compare Clothier GPT with BackCT.

Oh, okay.

Yeah, I removed Gemini because I think it's too much. Yeah, yeah.

Okay, great.

YesWell actually if you have it we can compare. So I think right now the internet opinion is Chagipiti is best for deep research. You ready? Let's see. Uh... Okay. Let's first look at the prompt, I think, because I did some work on the prompt. Yeah. Preview, no. That's what I said preview please, okay Okay, prompt. So this is a two-part prompt. What? Oh no, I messed up. Yeah, I messed up the prompt actually.

sorry let me fix this real quick tick tick Preview. Okay. Yes. Okay, so can you see in black like this? Yeah, yeah, yeah. So Yeah, so the way it works is research the biomarker Research the biomarker comprehensively. I need to output structured data for health product. This prompt is going to output two things. The first one is... Getting the range, because that's what we wanted, right? So, output one structure range data.

Standard range, optimal range. And for each range, you want exact value and sex specific. So, you know, kind of like data to Um, Just to get like a data table, right? So depending on sex and age. And I think, oh, maybe I forgot. There should also be guideline for race or ethnicity. Actually, I forgot that one. So this is the actual to use for the product, and then the output two is to make a blog content because I think what we can do is we use his research to do blog.

And so we can do one marker per week or something, you know? And then after like a year, maybe we have a nice blog. Um... Okay, so I only need to watch at this too much. That was basically the idea. So the actual range and then the view. So now the prompts. Is it this?

No. Yes. Oh, chattypneed, right? Okay.

Yeah, so I use multiple where people say chattypneed is best, so let's see. Let's see what you think. Vitamin D status is more commonly using serum. So this is the test. blah blah blah from an analytical standpoint vitamin DMm-hmm. Oh, sorry. Sorry, I think the output 2 is wrong. Oh, shit.

Yeah, I think it's too long.

I think he messed it up. Okay, anyway. Clinical interpretation remains different. Primarily a bone endpoint and therefore Do you want the table?

Because he has the table right away. Yeah, yeah, yeah. I think it's way too long. Hmm. You have to make it shorter?

I'm trying to find the data. Oh my god, no comparing. limits Comparative essay. Oh. LQ, I think this is comparing the tests.

Is that like research, research tool?

Measurement standard milestone, that's actually pretty interesting. 2017, 2019 is too much, bro. Okay. Consensus threshold from major guideline bodies. Finally, okay, midway. Insufficient 32% Sufficient, yeah, but again, this is too much detail. So they compare multiple body. I don't know if you have one that you think is better than the others. National Academy of Science. Uh...

This is the one for research, right? Not the one that you want to put it to the interpretation?

For me, if it's for the client, that would be two weeks. information Yeah, yeah, yeah.

So this is-This is for research, right? I mean, for the client, there will be... Slow discovery, so maybe we first of all we only show the graph and then if they click maybe we have one paragraph to explain and then if they click no more then maybe they go there.

Kind of like block post. Yeah, yeah, yeah. So you have a short version and then a long version. This one has a information. It's too much The problem with too long information is you have to verify information too. Because when it's too long, you have to... to read it and make sure it's correct.

I think it's my fault because I think I messed up the prompt. I think I gave him a wrong prompt. I will try again. Okay, forget it. What is this? Usage, I messed it up again. I give the wrong prompt. So the data might not be completely correct. Actually, Perfect City managed to do it anyway. Okay, Perfect City is pretty good. So right away, vitamin D Common lab reference. Okay, many expert guidelines.

Okay, that's it.

Yeah, that's enough, that's enough. Literally take away, okay.

Because you think about the report, right? They have to see the result and they have to know how to interpret the result, that's all. It's very easy. Actually, that's really great. So you agree, and do you agree with those range? Do they look okay to you?

Actually for vitamin D it depends. You can use either way with reference.

As long as you have the reference where you get the information from, that should be okay. You can use 30 to 50, you can use 60 to 100, it doesn't matter.

So quest diagnosis and then you give the list right and then start Standard reference and then propose optimal so apparently you want to keep this low.

Yeah For example, for me, I use 40 to 60, some doctors use 60 to 100.

But apparently, according to these, lower is better, 30 to 40, pretty tight. What is my name, and then he's like, what is my name, D. Okay, so, so far we agree, public city. And then you have all of the research.

I'll show you some. This is my writing.

I'll finalize soon, but let me show you some biomarkers.

And then this is the last one, sorry, third one. This is Claude. So Claude gave Overview, fasting required no, you need a measurement, okay. And then standard reference range, low bound 30, high bound 100, that's correct? Mm-hmm. Classification breakdown. Okay, doesn't matter. Where's the optimal, bro? Optimal range. 40, 60, so he seems to be agreeing with you more.

Maybe they use the same database like I used.

primary sources grassroots the action actually cloud is not bad I like these two I mean it's long but at least they give an overview right? Yeah.

I'll show you some in a way that is a little bit more organized and easy to understand. This is the thing that I'll do for my team to get better understanding about the result. Let's see.

So now that you have co-work, Claude also has deep research.

Yeah, yeah. But I still prefer...

I think the visit is pretty good. Perfectly because it's well organized. Something like this in the way they interpret the result. Let me see if there's any vitamin D. If you see CIP something, okay, I'll show you the example not just relatively. You give standard range, you give optimal range and then you give like the comment about this. Like I mentioned, I mentioned if it's a number higher than 10, this means infection.

This is all the information that we need.

Even doctor just need this, okay, for client also.

So if it's in the green, if it's in the range, you don't care?

Yeah, yeah.

So you actually only want flag?

and very concise information and interpretation guide. We don't have to put too much information. For example, when you do the interpretation for liver function, what you want to see is if all the liver function enzymes are in the brain. If it's out of the brain, what causes the problem? And management, how do you do that clinically? There are the red facts, for example, In ALT higher than Tx, that is the sign that urgent, you need to refer to the doctor to get more investigation.

Okay, vitamin D.

This is for your team? This is for my team. For like educational stuff. Actually I'm doing the same thing that you do, like group of longevity lab panel. It might be a little bit different than yours, but it covers almost everything. Like for vitamin D is standard range here, optimal range here and this is the recommendation if it's higher than 100 is potentially toxic.

That's all.

Sorry, okay. You gave me a big detail I completely forgot. So on pre-whale you do that? Yeah, yeah.

Pre-well, actually pre-well two main service I'll do is waste management and nutrition.

So do you have LabPanel doing similar to what I wanna do?

That's why I said this is just the gateway when the clients see my website they ask. Oh so you do custom for every customer? Yeah custom for every customer. This one is just like the mockup. I never use the package.

When they ask, I'll list and I'll give you the price.

How do you get the price? So you need to ask in health every time?

Actually, the common lab I already have price. But the special lab I have to ask in health.

Oh, but one thing about, like, you remember, I'll tell you that I haven't used, uh, inhale very often What do you use for like blood tests?

Another company. Which one?

Now we use yto live Okay.

Vital Life from Bumgrad?

Yeah, Vital Life from Bumgrad. The lab? Their lab. They give better price. Oh, can I get that? Yeah, but I'm not sure about the name.

I'll let you know. I'll let you know. It's not Vitalite Company.

It's another Vito. Okay. Vito Lab, something like that. Can you send customer data?

Pardon? Can people go to their lab directly? No.

Not sure, let me check. Only B2B?

Because yeah, now as a B2B I have opened the account with every lab.

Can I compare the price? So do they have a backend?

Back? Do they have like a website? No. So you do online?

Yeah, why told, let me see, why told textbook, why told textbook, um, um. As an owner, sometimes I forget the name. White hole.

Life. Pro. Lab.

Yeah, they don't have the website yeah I'll let you know the name.

So how do you talk to them?

Similar to handheld email.

We contact them email and live.

So you say, okay, I want to do this. Give me the price. Yeah.

Most of... Most of the time is man-manually work. It's kind of like I'll ask them the price and then get the invoice and then we confirm the test.

Can I see an example of email? Just see.

Not on my in, on my stop.

Yeah, but it's very, very simple. It's like you get the price and then when you send, you just confirm that you send the test.

Yeah. the delivery, the crab will come to pick up the--So actually I want to show you, Yeah, forget the interpretation.

OK. So the interpretation, if I try to resume, when you see the blood test, so you want to know which marker is out of range. So let's say you see 50 biomarker, You only want to know which one is out of range. And then for those who are out of range, you want to know And then what?

If it's out of range, too low or too high, you have to know what to do next. You have to have the guideline or recommendation what to do next.

And so that would be another test or...

It can be another test or like the... The key recommendation, for example, if vitamin D is too high, just stop vitamin D taking.

Or get in the sun.

If CRP is too high, maybe you're having acute infection, you have to see a doctor. That is the recommendation.

Also, that was actually what Cyfox was doing. You remember Cyfox last week? Yeah, yeah, yeah. So they had For each marker out of range, they had one action and then on the action plan they list all of the action from all of the marker. So they were already doing that work, but just they should do even take all those recommendation and then do another like full action plan.

Yeah, yeah, yeah.

The better way to do that action plan is you You don't want to focus on on Only one test at a time you focus on the group of the test.

For example, you will take for cardiovascular health, cholesterol, diabetes, right? And if everything come up positive, like there's a lot of abnormalities, there is step-by-step management that you might set that recommendation for the client to go see referral to see a doctor.

So let's say if somebody has too many out of range and they're all about cholesterol, instead of having like three item on the action plan, you should see is like, okay, this person should really focus on weight management, therefore.

And then you give more general, okay, weight management, how to do better. General recommendation and urgent recommendation. If it's urgent or emergency, you know, the client knows. I see. I'll give you some example of Yeah. This is cardiovascular. We test for And so what kind of prompt you have?

So I guess you have a prompt that just flagged. Do you have a prompt to flag an item or you just look at the lab range?

I prompt it, but my prompt is very short, not too long. But as a doctor, I know what I like to see, right? So sometimes I prompt and I make some modifications. As a researcher, when I get the data, I'll ask them to add additional data, something like that, to modify the information.

Might be a special information for cardiovascular health If it's flagged out very high that would be step by management like if it's too high like this Hmm is urgent.

We need to see a doctor. Okay, it's a failure.

Yeah, Oh five be nothing too high Okay, maybe not too urgent the diet should be Should be enough and this is sorry.

These are all the marker related like Is it possible to share this with me? Sure, sure, sure. No problem. Just to have an idea of how you work.

But I haven't verified all the information.

I'll send you the whole pack. Same. It's just to get an idea of how you do the analysis.

Yeah, for nutrition, something like this.

Nutrition.

I think it's very simple. If low, what costs the low?

If high, what is the common cost of high level?

And that kind of like they have more information and they can manage according to their condition.

And another thing that very important when you want to interpret the result, many times we calculate the score or ratio. So I'll make sure When we get the information, we calculate important score like HOMA score for insulin resistance, QIS score for insulin resistance, something like that.

So this is not AI based, it's kind of like the... Regis and flags, yeah. It's verified ratio that gives better information instead of just one particular lab test. The ratio, the score that combines different types of tests, that would be better analysis.

Yeah, that's all. You can--Yeah, I'm curious if I can, because I didn't know this when we started this project, but if I just give my blood test to the AI and I'm like, "What's up?" Need to know the range and yeah, it'd be interesting. Maybe I'll do this next time. I think AI interpretation is not due today. I also need to prepare a bit more.

For me, I think we can use AI as... Oh. AI is good at gathering data, right?

Yeah. Organizing information and make it ready to use. I think it's another part. For me, the information of the lab test, at this moment, 100 tests is not too much.

You can do something like this. And you use AI to read the information that you already have, like the guideline that you already have, and then they pick up the information. So every time they see the result, they use the same information.

So when you give a recommendation, so let's say if I use AI and I give my results, So you want to have an overview do you give like the Atari plan of what food to focus on? I mean, I guess it depends on the On the person, right? Do you do supplements recommendation?

I do but not not not too much because I'm not the one who prescribed a lot of supplements, right?

Normally my practice I'll do supplement review the patient come with different bottle, multiple bottle of supplement and I'll help them review together with blood result which one should continue, which one should stop.

I see. And is it common? You see your customer take supplements often? Often, often.

Like what? In my field, often. 70% or 100%? Not 100%, but more than 50%, not 70%. Okay. Because for obesity patients, I don't usually recommend supplements. Usually they have too much. Yeah, they have too much. But I have different group of patients, right?

Another group is the one who want to focus more on nutrition, of course. They consume a lot of supplements. I have to review all those supplements and then make up supplementation. summary for supplement that really helpful for them. So it's manual work together with AI. Actually, when I got the result, I put some of the results to the AI and get the clue of what should recommend.

So like similar to what you showed me or something else? This one is kind of like quick summary. Because the AI does not have the range, right?

Not have the range, yeah.

So if you put in the eye and then you like flag, so you kind of try and then you review right sometimes they say this is high but actually it's not so high. Yeah, yeah.

We have to know to to help have the background of this information. For me, I think AI is kind of like help me with the with with simple Not difficult work, but boring work. So I get all the information in one page and I can use my own knowledge to reveal the information and select the helpful, beneficial information to my client. So I don't get all the information from the AI.

It's too much.

So let me check. Maybe I'll share I'm old school, so I'll do what? I'll do the what, okay? And share you what for them. So the way you use AI, I think, is one by one. So you analyze the report, the general report with an AI, and then you use information as a database for interpreting the result.

Yes, so with N Health, I had a lot of issues because, so we reviewed the package. Last week. So we did a package together last week. Yeah, and I asked AI to resume You remember why we use my website builder and then I sent so after you left I do another pass and Um, to kind of get lower level so because we use one package was like antioxidant and vitamin D 2 D 3 which I think was a bit too high level just too many things So I made a smaller list like this one.

Yeah, I don't know if you can see. So... I broke down the antioxidant into lower. So they have a package called antioxidants 10 and HPLC, toxic metal profile, Antioxidant mineral, so they have like smaller package. Mm-hmm. So the version we did together is version one and then I just I just break down the big package in smaller package. Okay. So that's version 2 and I sent it to them. I was like, okay, this is what I want.

Can I do all of this in one sitting? How many vials do I need to... Okay, anyway, blah, blah, blah.

And say, hello, valid customer. Not AI channel. Yeah.

So actually it's way more expensive than the price. because The price I have, I think the estimation was 17,000. Do you have any price for me in health?

Like any price you share with me? Not yet, not yet.

I asked him, I'll share the list that you show me, but no.

I don't wanna say yet. All right.

Um... So they came back to me and they said, "Okay, this is the price. 21,000, I think the price we saw was 17 or 18, 18. So it's more expensive and they remove stuff actually they say So they have a package, a happy life, which include Some CBC and some kidney. Basically change the package and they say a whole more in for tarot they have a package actually because last time we couldn't find it separate package blah blah blah blah blah blah blah and then they say And then they say we don't haveJust to tell you how.

Just, so imagine you're a customer using ChargeGPT. That's why you have to go through. Yeah. Okay? So, negotiation, blah, blah, blah. Okay, we don't have this, we don't have that, okay. Then they ask me to fill the package. and then They remove liver function. So They say "Oh we can do this package" They removed the liver. They didn't tell me. I just forgot, I guess. So I asked AI, I said, hey, Leave a function is missing.

What's going on? They say, oh, leave a function. You want to add 500 pass, I guess. Anyway, love back and forth as you can see. So then he gave me another quotation, quotation number two.

This is the one I usually receive from them. It's similar.

Station number two, so now he's even more, 23,000. Okay, so at this point you see it's like an hour of back and forth between them and me as unbearable. Okay, so... So... Talk with them package number three.

Whoa, it's not finished. And then I go to headspace.

go to in space they're like oh actually so The person that does the line is not the person at end space. So at InSpace, So remember they said they don't have to leave a package anymore. No, they say they don't have the heavy metal. Oh. So heavy metal is unavailable. Then I go to in space, So they give me this. So... Blah blah blah, and I talk with them, they say, "Oh, actually we have the heavy metal, you wanna add it?" So then we change again, we change the package again, version four.

Which is supposedly similar to actually what we designed. 23,000, so even more. And at this point, I'm at 23.2. I was like, okay, let's do it. I want to get through this. Please take my blood. I see.

It's not uncommon, you know. Every day. It's everyday problem.

I know, but just, you know, like as a... So I'm like, for me it's fun, you know, right now I don't have a job right now, and I think it's my hobby, but for a real person, this is unbearable. Impossible.

Sometimes you might have to I see some duplicates.

The two packets have the duplication.

The same test. Different packets.

So I think mercury or one of them, copper, no. Magnesium was being tested twice.

Yeah, yeah.

And then they cannot cut it out. They have to do the same test twice.

Oh, so it's common. It's common. Okay, yeah.

But they would insist that even you cut it out, the price would not change.

Yeah, because they have packages or whatever. Heck yes. Okay, so that's coming. Yeah. Yeah, so I did. So in the end, So the hotline actually removes some tests and then when we get back there, they put it back. So actually the package I did at the end was pretty much the one we decided to get. So anyway, all of this for nothing. Yes, so. Okay. We're not gonna review the... Anyway, now I have everything so I can use AI too.

Okay. And then next time you would have your interpretation, right?

Right, you tried to make your interpretation? Yes, I haven't.

So I've done it. It was Friday.

So I got all the results pretty much yesterday. Have you tried any interpretation? Not yet. Oh, yeah, yeah, yeah.

It's pretty good, actually.

Like one in report? Yeah. Do you have any like the example of your style report.

No, I haven't.

Not yet, right? You mean my own product? Yeah, yeah, yeah. Your own product. Not yet, right?

No, I'm still finishing the, I can show you. some more products because I first want to do research before I do my own. Now we can talk about what makes sense. Um... This I can show you. 15 minutes left. Parallel research, interpretation landscape. So we review Ornament together, Psyfox, Kiro... Inside tracker, I show you? Yeah. Uh, New one doc use and blood GPT But GPT. But GP, good name, huh?

Everything GPT. Yeah.

This one is okay, I think. I think they just do like simple interpretation. Well, actually... Can't just go on the website, actually. Yeah, I mean it's kind of crappy. You want to see the range, right? Oh, I can see. So it's like this, I upload a test From Any Health last year, last month. May I go to you in your soul, friend? And then you can see I guess what you're going to like is they are able to show only the out of range marker.

I forgot how you do it. Anyway, no action plan. They just show you the report and then you see it's yellow. I mean, this one is out of range. Then you can click. I cannot even click. But this project seems dead actually. Blood GPT, I think they're dead.

It looks nice in the green way, but not much information.

Yeah. And then the other one I looked at is called... Um... Docu's AI, this one is actually pretty good. Um.

Okay, I've seen that before.

Yeah, well you bet you see it so... Health report, I guess, health report is the action plan pretty much. Check-up plan, I guess this is recommended test because right now they only do interpretation. Actually maybe we should do it like this, right? We recommend the package. This is the action plan. This is the AI. And this is the upload your own test. AI is crap. We can try it. I'll skip it. How are you doing?

Ah, come on. Yeah, that's bullshit. They haven't, they ain't. That's really bad. That trace is very slow. Um, And you can tell it's Chad GPT. The way he writes, the way the AI writes, I can tell it's Chad GPT. And it's very long, and it was bad. I think a lot of these companies, maybe it's just one young guy that was like, oh, I'm going to do a... And they just don't know what they're doing technically, I think.

You can tell the result is not good.

Anyway. Or when you look at the website, you know, right? It's not--I know he's a beginner. It's not well designed, right? He's a beginner software engineer, yeah.

Because I'm experienced, so... Okay. This one, yeah, one thing. So this is, I uploaded my... PDF. and then this is the extraction, is okay. You can filter only abnormal, so I guess this is what you like. So you have an overview on only what's abnormal. and then you can click and you have a little bit of an overview but I think it's also very simple there's no no more That's it. This is a raise money actually.

Honestly, seeing some of these websites, I'm thinking maybe I'm overthinking.

Yeah, there are many companies doing the same thing. It's kind of like third party? No, but they raise...

Third party company doing lab interpretation? They raise more than a million dollars. Oh, okay. I can do this in a week.

Maybe you can start with that. Yeah, that's what I'm thinking.

Okay, one thing.

This is like business opportunity.

I think you can separate your service in different parts. If you think about B2B business, If you do the interpretation in a good way, very simple, very reliable, you can sell the service to clinics.

But you think leading with pay, I think it's cheaper. um he's kind of like subscription based how much would you pay for this Like a hundred bet? He's like... Something like that.

$20 up to $50 per month.

Yeah, but how many clinic in Bangkok, you know? That's the problem. Like if 10 clinic, that's too much.

Because it's not just in Bangkok, right? Because it's in this bed, right? It can be everywhere in ASEAN. You mean full clinics, yeah? Yeah, full clinic and even hospital, but hospital difficult because they already have their own system, right?

Difficult to plug it in. But if you... If you can do black-in interpretation, that would be another level.

But I would say the clinic.

You think clinic would pay per customer? Let's say if I charge like 100 baht per customer.

It's possible. It's possible. But for me, I would pay if there is a quota.

from this subscription I can do 50 patients maximum more than that I have to pay extra yeah we'll see it's a part of service that you can sell separately yeah you can try I think I don't like B2B I think it's too difficult oh really?

it's too much work Because B2C, you know, if it's successful, it's a million dollars right away.

It's kind of like going slowly is a potential, right?

Yes. I think B2B is kind of like... B2B is stable, but very slow. Yeah. So... It's easy, right? Because you can talk to people, get customer, you can make custom made software.

Okay.

For me to see this service can be the main thing. It's like we discussed about... aboutDad, Dad. Todd. the way hospital report, right? And how and how disconnected it is from different hospitals. If you can centralize all information, that would be good. For me, I would use your service. If I can centralize all of my health checkup history, I think it would be good.

Why do you need the history actually? That's something I struggle with. Is it important to have, let's say, checkup you did three years ago? Yeah. What's the point?

We have history to compare.

Like what data do you want to see about yourself? Anything, anything. I mean anything.

If you can, if you have the service that I can, I gave you a lot of documents of my checkup from the beginning. from 20 years ago and then you can centralize all the data and make it connected, I would buy that service.

But let's say, for example, okay.

You would say that, oh, three years, it's too long.

Yeah, it's too long, but it's worth knowing, right?

Yeah, I mean, as a doctor, I understand you want, but so for example, let's look at this. So those are, let's say, okay, you're my doctor. So these are my results. Which of these markers do you want to know like five years ago? Which one is like really good or is it more like EKG?

For this, it's very...

how to say, like, it's very common lab, so I don't worry about the previous history. Yeah. It's kind of like good to know but you don't need to.

So which one you want to know like from before?

EKG? DEXA? For example like if I have Actually, it's not.

um, It is good to know. It's good to see the information in the same place. But it's not very important.

Even I have two apps compared to different labs.

It's okay, but it's not convenient. But if you ask me how important it is to see your history from 20 years ago, not that important. But if you have it, Good to know. Okay, and if you have this data and you share it to your doctor, that would be a good life portfolio for your health.

Okay, and everyone like that, every doctor like that.

You mean as a patient I would be able to give you a link and then you can see all of my history or something?

Yeah, for example if you have that kind of service and then my patient come with your service and show me the history of the lab. Of course I won't go through 70 years ago history but it's good to have so I can spot something if it's happened because you know health is not static. Health is kind of like dynamic. Connected timeline is good to It is... It gives us a clue for long-term health, for potential health issue in the future.

We are in functional medicine, we call it a metric. It's health metric. Health metric is very important because we cannot just look at one lab test and spot the complete problem. But if we see the problem from the starting point like 10 years ago, we see the whole picture. That's very important.

So like you mean like things like cholesterol maybe somebody has chronically high cholesterol? Yeah yeah. Then maybe you want to look at some after reclogging or something?

Yeah something like that.

Is It's like, for example, if you think about your assets, right? but it would be good if you have Uh... The... How to say in English? It's like... your book to summarize all of your assets. You know which one you have, different types of assets you have. It's similar. For health, if you do the blood test in the last couple of months, couple of years, you have all the data in the same place.

X-ray, CT scan, everything in the same place.

I think it's good information to have. Yeah.

Okay, any other good company, bud?

You showed me last time what company I think that one best, the gradient color.

and interpretation with reference and with with the link to the reference yeah there's a few say folks yeah hero you like I think yes I fuck you yeah I think they're pretty good probably start with them so I guess the interpretation is something complicated. So, One thing I was thinking to start would be to, so, I have some pre-made panel that I can share with people. It's like, hey, if you want to, If you want to do biohacking or supplements, you know, we can have a...

You'll sell in Bangkok, so those packages are pretty good and you can ask any health or past lab and they will give you the price. And we just give the list of marker and people can just copy paste. Yeah. And this is good because even if we don't make money, We get the email. And we know it's people, spending money on this. So we know that when we have the product, because it's also for investor, right?

If I have a thousand email of people doing those tests, very easy for me to raise money. 'Cause I can go see investors, like, "Look, I already have a thousand people already doing this." If we have a product, they will buy from us. Great. And then the second thing is the interpretation. I was thinking to... Again, because PDPA, so people cannot give me medical record, I think it's difficult. I would think you just give them prompt.

So we have pre-made prompt. So one prompt is like, can you flag blah blah blah. One prompt is like, can you make a dietary plan? You know, just some nice prompt. And we're like, okay, you just take the PDF and you copy paste the prompt and then charge a PT will give you something Okay, it's not great, but people do that already.

Okay, I think you can do that with PDPA and then When when they upload the information, right?

Yes, okay, so I don't want it not so I don't want I don't want them to give me the information. Oh because then I need a clinic. And actually more than that. Do you need it?

Yeah. For example, if you share something like this, the website, they don't have. Do you think they have? I don't think they have it. When you upload the data, But because they are in aYeah, so you allow me to--But okay, this website, they don't have PDPA because it's not in Thailand.

So it's illegal?

Not illegal but we just give them the information without... Grey area.

Yeah, grey area. So maybe I put my website in Singapore or something.

Yeah, that's the way they do. So there is no legal problem with that.

You can do that actually.

But I think the problem is to get paid.

what they have is they are paid because the problem is if we interpret the result in its money it costs money but but for me i i still believe if you want to explain it in the future uh with this kind of thing you have still you you need to request pdpa yeah of course yeah and then when they allow it to give to to analyze the information yeah it's safe legally yes and uh for interpretation you don't have clinic you don't have to worry you just put this claimant yeah if it's generated by ai yeah is not diagnosing the disease, something like that, this camera will work fine.

Okay. Okay, that's all, that's all.

Yeah, so, But anyway, this can be, so this could be a step further, but what I was thinking is just, I give the prompt, and then I tell people, okay, you just do yourself, you know, you just get the prompt. Because I think, again, It's not Perfect, but at least At least people come back to my website and say, "Oh, I have a result. I'm going to get the prompt." And then maybe they ask me some question.

You know what I mean? It's just a way to start the relationship, you know? Even if I don't make money, at least they give me the email, they ask me questions. Yeah, yeah. You can start with that. Um, This is easy and can be done fast, you know. And then later on, yeah, then later have a proper structure with PDP and everything. Yeah. Peace out.

This PDPA is SIPAA, it's kind of like a medical thing.

Do you have this working?

So now you have everything? PDPA?

As a clinic, it's already applied PDPA. PDPA actually is not need to document.

It's just when we get the patient information, we don't share. We keep it inside. That should be okay.

Who is your Data, you need a data director or something?

No, just my staff, but my staff, everyone has to sign the agreement about this.

Don't share the information outside. Because if it leaks, it's their problem.

And your staff is what, is you? No, sorry, is your partner? I mean staff you have.

Everyone can see the information. But you have, how many staff you have? Now three. Oh, okay. Yeah.

Three staff, two panel. Very lean company.

Sorry. Yeah, it's pretty good. Yeah.

And you can look at my the reference guide and see what you can do from that.

the testThis one?

Oh, yes. I'll check. Yeah, thank you. Look. Great, thank you. I think that's it for today. Let's go.
# MyLife AI Open Development Sessions

- [Episodes](#episodes)
  - [current session](#20240927)
  - [archives](#episodes)

## Presentation

Currently on Zoom, promoted through LinkedIn personal account, as MyLife does not yet have 100 followers to use the LinkedIn Service

[Live Event Zoom Link](https://us02web.zoom.us/meeting/tZAsduuvrz8qEtKQLZbVlsfuktejbb6iBS6T/ics?icsToken=98tyKuGsrzooHdWRsBGBRpwIBYj4a-3zmClfj7d2rTPfARZfcQXjPfZHOLB9RtHy)

## Upcoming Episodes

### Serial Arcs

- Diary Bot
  1. Birth of a Diary Bot: based on specifications create flat OpenAI Diary Bot prototype from specifications
  2. Headless Diary Bot: Connect this working Diary Bot prototype with MyLife Backend via `actions`
  3. Head Transplant: from specifications (add two+ internal MyLife endpoints #4) and prototype instructions, build and show how Diary bot instructions are stored and realized in the MyLife platform
  4. Into the Pipeline: using `obscure` as the fundamental novelty
  5. Frontend - looking like 2 episodes
     - container
     - entries
     - options
     - build associated instruction-commands + options?
  6. Team: add new Diary Bot as default to memory team
- one-off episodes on bug-fixing [example: refresh of screen handled by backend]

### 20241004

#### Diary Bot Series Week 5

- [LinkedIn Event](https://www.linkedin.com/events/buildadiarybot-partfive-mylifea7245506294151884802/)

##### Cover Art

##### 20241004 Introduction

- [Slide 1: Title Slide] **powerpoint**

Hello, and welcome to today's session of `MyLife AI Open Development`! I'm Erik Jespersen, president and platform architect here at MyLife. MyLife's aim is to put you, and all of us, in control of our AI-experiences for our own private, personal and collective wellbeing.

In our ongoing "Diary Bot Series," it's time to put a face to the figure. Last week we explored the MyLife backend pipeline for LLM Engagement and today we create the interface elements needed to engage meaningfully with our Diary Bot.

- [Slide 2: Mission] **powerpoint**

`MyLife` is a 501c3 nonprofit member organization that offers its membership, at no charge, an intelligent ai-assisted platform that helps them collect and preserve their cherished memories, stories, media, and ideas for posterity as their digital legacy. MyLife is not affiliated with any paid, premium or freemium service, what you see is free and what you see is what you get.

What is this? How is it used? Well, before I show the interface, here are just a few of the use cases we've already been building towards with our initial functionality.

- [Slide 3: Use Cases] **powerpoint**

If you're someone lonely, perhaps in a retirement community, suffering from or worried about memory loss, or if you know someone in this condition, `MyLife` will help capture their story.

Or someone struggling to understand themselves, their identity and how they want to show up in the world? Or maybe you know someone who is? `MyLife` provides a safe and private sanctuary for such self-investigation and awareness.

-- insert content about military?

It's for all of us. Built by us for us. We are many and varied in our needs.

We began here at `MyLife` by building an intelligent opensource and free platform for all of us to use that helps elicit, store, protect, and ultimately **make** intelligent your narratives. According to your explicit consents. AI can make anything linguistically intelligent, including abstractions like: a story, a memory, an idea. That is the power we bring to bear at `MyLife`.

##### 20241004 MyLife Showcase

MyLife **Walkthrough**

- [SCREENSHARE Chrome](https://humanremembranceproject.org)
- Introduce **Q**
- Demonstrate Login
- Introduce **Interface**
  - this is all what you get when you become a member of mylife
- Introduce **Member Avatar**
  - Intelligent client, your intelligent account, digital you.
  - Avatars already coming on the market we are an aggregator, so if you want to use ours, or use another party (or some combination) that is intentional in the platform design
- Introduce **Bot Team**
  - Team of intelligences here to help you do the work of being human! Start with our cherished memories and narratives as well as innermost thoughts. The stuff you DON'T want to be sending to Google so they can own.
  - Select **Biographer**
  - Explain how options work
  - Copy/Paste story of today below
    - Today is 20241004; Please save this memory and title it "20241004"
- Introduce **Scrapbook**
  - show editing options
  - show activation contextualization (how we might contextualize anything)
- Demonstrate **Tutorial**
  - Fun, yes? But implies how relive memories are being cast (in progress)
- Demonstrate **Relive Memory**
  - Emphasize it will use same tech as `Tutorial`

##### 20241004 Learning Objectives

- [Slide 4: Learning Objectives] **powerpoint**

Now that we have our functional pipelines available to the Diary Bot (in utero imaginato) phantom, we need to build a way to access it. To Lakshmi's point, Lakshmi is one of our fantastic volunteers, you can already access some of this functionality through the OpenAI GPT prototype; by the way, you heard it here first, or at least _I_ did, that OpenAI is going public so that they can be bought by Microsoft. But there's no scrapbook over there, so...! Frontend it is. So we start as always with

- **MyLife GitHub Repository**

We are an open-source public platform, so you should feel encouraged to visit our [codebase on GitHub](https://github.com/MyLife-Services/mylife-maht) to review tickets or progress or you can chat architecture and some engineering directly with our [intelligent codebase GPT](https://chatgpt.com/g/g-oAvQvGv5f-gpt-maht).

- **MyLife Frontend Technology**

This is the one to skip. No. Don't skip it. I mean, I think you'll experience, as we investigate this, how fragile our very notions of frontend really are at the moment in the age of artificial intelligences that can dynamic permute code and text like HTML and CSS. Frontend will never be the same, it can never be the same, and here's MyLife's gap: I've never been good at it, and I haven't had the time to dedicate to realizing an efficient and sensible "intelligent client" model yet. It's organically _emerging_ through the concept of developing the Member Avatar into _exactly that engine_, but of course, for the moment, _I'm_ starting from the backend.

- [Slide 5: MyLife Service Consent and Control Architecture]

So if you're not into laughing at others' misfortune, then don't continue with this episode, because MyLife has definitely been injured for lack of a forward-thinking frontend UX and UI designer. Is that you? Call me.

Let's talk about this slide. The ultimate vision, rapidly nearing term, is a landscape where intelligent platforms that offer services engage with known or independent _client_ intelligences that consume the platform's API services.

So we are building our tools with the assumption of an architecture you see described here, which we'll enforce collaboratively with eco and exosystem partners.

- **Stage One**: _Negotiation Handshake_
- **Stage Two**: _Experience Exchange_
- **Stage Three**: _Conclude_

**Negotiation Handshake** allows the two entities looking to make a connection and engage in an experience or data exchange a format via which to negotiate consents and groundrules, compromise frameworks, and inject necessary protocols. In other words, you don't know how to render a set of experiential scenes? Let our avatar show you...

**Experience Exchange** is completely undertaken with the consensual liberties outlined in the negotiation. We propose this command and control architecture where the server drives the nature of the experience and data acquisition requests, and leaves it to the intelligent client to pantomime these requests in ways befitting their operator.

**Conclude** is the process for finalizing data storage, exchanging keys or receipts and human-in-the-loop requirements.

The future is here!

##### 20241004 Practical Session

- [GitHub Frontend Specifications](https://github.com/MyLife-Services/mylife-maht/issues/381)

##### 20241004 Wrap-Up

- [Slide 6: What We Need Now()] **powerpoint**

- **Lessons learned:** We learned how to create generic intelligent functionality inside of MyLife!
- **Get Involved!**
  - We need you!
  - Volunteers are already incredible, only too few in number: Special thanks this week to Steve, Russ, Avani, Lakshmi, Mark, Jesse, Jeff and Chris.
- **Next session**: `Week 6: All Together Now!` where we put the diary bot on a team, connecting the dots and accessing the dynamic instructions until we have a member-functional Diary Bot intelligence!

## Episodes

### 20240927

#### Diary Bot Series Week 4

- [LinkedIn Event](https://www.linkedin.com/events/buildadiarybot-partfour-mylifea7244939845918224384/)

##### Into the Pipeline

##### 20240927 Introduction

- [Slide 1: Title Slide]

Hello, and welcome to today's session of `MyLife AI Open Development`! I'm Erik Jespersen, president and platform architect here at MyLife. MyLife's aim is to put you, and all of us, in control of our AI-experiences for our own private, personal and collective wellbeing.

Today we are continuing with our "Diary Bot Series" jogging towards our ultimate aim of incorporating this technology into MyLife -- and we're halfway there! MyLife is highly configurable and scalable to create the intelligent solutions that work for you, your loved ones, and even your professional clients.

So last week we transplanted the brains we'd built inside of our OpenAI GPT Diary Bot prototype into the MyLife intelligence backbone. All with just some sensible copy/pasting and mild content development. Today, well, today we are going to walk through a couple of tunnels together.

Enormous Tunnels! Vast Tunnels! A tunneleers delight-time! Also something for unnecessary 3D enthusiasts like myself

- [Slide 2: Mission]

`MyLife` is a 501c3 nonprofit member organization that offers its membership, at no charge, an intelligent ai-assisted platform that helps them collect and preserve their cherished memories, stories, media, and ideas for posterity as their digital legacy. MyLife is not affiliated with any paid, premium or freemium service, what you see is free and what you see is what you get.

What is this? How is it used? Well, before I show the interface, here are just a few of the use cases we've already been building towards with our initial functionality.

- [Slide 3: Use Cases]

If you're someone lonely, perhaps in a retirement community, suffering from or worried about memory loss, or if you know someone in this condition, `MyLife` will help capture their story.

Or someone struggling to understand themselves, their identity and how they want to show up in the world? Or maybe you know someone who is? `MyLife` provides a safe and private sanctuary for such self-investigation and awareness.

Or someone who wants to leave behind an imprint of their art and ideas--we're all becoming quite aware that digital ghosts will be animated with corporate intelligences in order to model your behavior, and that is **not the face-to-the-future** you want to imagine for yourself? `MyLife` is the antidote. First-persona accounting of their truth, embolstered and animated for posterity by intelligent bots.

It's for all of us. Built by us for us. We are many and varied in our needs.

We began here at `MyLife` by building a headless intelligent opensource and free platform for all of us to use that helps elicit, store, protect, and ultimately **make** intelligent your narratives. According to your explicit consents. AI can make anything linguistically intelligent, including abstractions like: a story, a memory, an idea. For any wondering, this is just one reason why AI is **not** a fad but is illustrative of how AI will _change_ the world. This is one way we will build empathy and compassion.

##### 20240927 MyLife Showcase

- **Walkthrough** [Chrome]
  - [Login](https://humanremembranceproject.org/?type=select) as `system-one`
  - Explain Interface
    - this is all what you get when you become a member of mylife
    - explain Member Avatar: include intelligent client, your intelligent account, digital you. Avatars already coming on the market we are an aggregator, so if you want to use ours, or use another party (or some combination) that is intentional in the platform design
    - Explain Bot Team: team of intelligences here to help you do the work of being human! Start with our cherished memories and narratives as well as innermost thoughts. The stuff you DON'T want to be sending to Google so they can own.
    - Select Biographer and show/explain options
    - chat area and UX
  - share story of today [copy and paste sub-bullet]
    - Today is 20240927; I got up early in order to effectively tackle the mid-sized mound of work I need to do today. I still need to get the presentation in order (it's mostly there, I'm just not sure how to present it exactly yet), and I'm working on the script, well at this very second! I've got some fun slides today that show the pipeline of MyLife, and I'm really excited to go through it. Starts in 10 minutes from this entry! Please save this memory and title it "20240927"
  - introduce `scrapbook`
    - show editing options
    - show activation contextualization (how we might contextualize anything)
    - **Relive Memory**

##### 20240927 Learning Objectives

Today we're going to peruse the pipeline, investigate the tunnel, spelunk our way through the underbelly of MyLife, to stir metaphors. Before we get to that visualization and coding exercise, I want to show you:

- **MyLife GitHub Repository**

We are an open-source public platform, so you should feel encouraged to visit our [codebase on GitHub](https://github.com/MyLife-Services/mylife-maht) to review tickets or progress or you can chat architecture and some engineering directly with our [intelligent codebase GPT](https://chatgpt.com/g/g-oAvQvGv5f-gpt-maht), who, mind you, is in desperate need of a mind update.

- **Review LLM Knowledge Types**

- [Slide 5: LLM Knowledge Types]

Today's exercise will require demonstration of one of the primary pipelines for our platform intelligent interactions. It is through this pipeline, through this _tunnel_ that all aspects of our knowledge types come alive. Let's quickly review:

- static knowledge: instructions, files, references
- dynamic knowledge: functions, actions, datacore interactions
- interactive knowledge: MyLife architecture affords dynamic instructioning, thread management, bot team functionality, and more bells and whistles we have in our back pocket for another session.

- **MyLife Request Life-Cycle**

In order to incorporate the obscure functional dynamic knowledge inside of our MyLife Diary Bot, it will be critical to understand the life cycle of a request that contains a member's content in an interactive dialog _with_ the Diary Bot.

##### 20240927 Practical Session

So with this in mind, a function called `obscure` to build out, and a pipeline to survey, and short order in which to do it, let's quickly review our issue specifications for `obscure`

- [GitHub Obscure Functionality Issue](https://github.com/MyLife-Services/mylife-maht/issues/374)
- MVP proof-of-concept = Proper Human Names => Letter

Why would you want to obscure content? This is a diary bot, after all. So First let's examine what happens to your private input, where it goes and how it is stored.

- [Slide 6: Where Member Content Goes]

This is a high-level diagram of the request process through MyLife's platform architecture. Let's discuss it

- **Member Avatar**: stores it in locally memory, only to be committed at session end, by consent
- **LLM**, currently OpenAI: stores and runs, or _responds_ to, the content sent by our Member (with any additions required for functional clarity by the Member Avatar)
- Member Avatar => **Member Factory**: Stores item in MyLife database (direct source content _not stored_)
- and then, the response, often containing the mutated content, is sent back out to **you** at the frontend

Let's review the "physical" locations where your personal content and data is stored. All of this is critical to any security and privacy plan.

- [Slide 7: Where Member Content Is Stored]

- **MyLife**: Conversation (by consent), Item (by design)
- **OpenAI**: thread-based content
  - MyLife can delete/recreate thread
  - Allegedly paid services (like us) do not have content go to train models
  - MyLife decouples data threads at LLM level

Any questions, please ask in comments, and we'll get back to you asap!

Let's now checkout this pipeline. You type in personal content, and you hit submit. By showing you exactly what happens we'll be simultaneously paving the way for our `obscure` function. Watch!

- [Slide 8: Submit Chat: Frontend] **powerpoint**

Here you can see an unnecessary 3D representation of the pathways your content will take, for the most part the same as obscure functionality, not yet built into the frontend.

- [Slide 1: members.mjs] **screenshot**

As an example, you can see our frontend root javascript file's implementation of `submitChat`

POSTing to the server, MyLife's API or System Avatar takes over.

- [Slide 9: Submit Chat: MyLife API] **powerpoint**

It travels through the general API aperture exposed for chatting. Now we can start building some of the obscure functionality from the outside in.

- [Slide 2: routes.mjs] **screenshot**

By first creating a route for the member call, and then

- [Slide 3: functions.mjs] **screenshot**

defining the function. Let's take a look at those parameters. `:iid` is required in the path and refers to the itemId associated with the logged in member.

Now something really cool happens. The System Avatar hands it directly to your personal avatar instanced to manage the process from there.

- [Slide 10: Submit Chat: Member Avatar] **powerpoint**

So your avatar now needs to go about the business of obscuring your content

- [Slide 4: mylife-avatar.mjs] **screenshot**

It immediately leverages its internally protected factory instance to complete the work.

- [Slide 5: mylife-agent-factory.mjs] **screenshot**

Basic content validation and structure takes place here, and then it is handed off to a modular function to access the "generic" or general `mLLMServices`

- [Slide 6: mylife-agent-factory.mjs] **screenshot**

And from there, it's on its way to the LLM,

- [Slide 11: Submit Chat: OpenAI] **powerpoint**

trimmed pruned and metadata'd as necessary.

- [Slide 7: mylife-llm-services.mjs] **screenshot**

You can see here our interface with the OpenAI SDK, in this case of obscure, it's just a general chat call with a disposable thread. We obviously need an intelligence to handle this request since we are not directly yet embedded in the diary bot, 

- [Slide 8: GPT instructions] **screenshot**

so we have a general functioneer bot infused with the instructions:

- **OBSCURE**: When a request begins with OBSCURE the following content should be reviewed and altered such that any human names referenced in the content would be changed to just their first letter. **example:** "Edwardina went out" becomes "E. went out" even if there are multiple E's in the content. I don't make any other alterations to the content and return JSON Object with one string node called `obscuredSummary` that contains my modified summary

Great! So now reverse the process, which you've already seen in code,

- [Slide 12: Submit Chat: Member Avatar] **powerpoint**

And here we see something interesting in the avatar actions where it generates intelligent instructions for the, or "a", front-end to execute or render. In this case it was `updateItemSummary`

- [Slide 13: Submit Chat: Member API] **powerpoint**

And lastly, out the way we came! Voila, obscure is now a viable endpoint - let's see it in action using our local dev.

- **SCREEN SHARE** Postman, set up to obscure the Dorothy reference.

##### 20240927 Wrap-Up

- [Slide 13: What We Need Now()] **powerpoint**

- **Lessons learned:** We learned how to create generic intelligent functionality inside of MyLife!
- **Get Involved!**
  - We need you!
  - Volunteers are already incredible, only too few in number: Special thanks this week to Steve, Russ, Avani, Lakshmi, Mark, Jesse, Jeff and Chris.
- **Next session**: `Week 5: Cover Art` where we paint a face on the Diary Bot for the frontend!

##### 20240927 Outline

1. Introduction to Host, Session, MyLife and the Webinar Series, _5m_
2. Showcase the Current MyLife Member Biography Platform, _10m_
3. Learning Objectives, _5m_
   - GitHub Repository
   - LLM Knowledge Types
   - MyLife Request Lifecycle
4. Practical Session _20m_
   - `obscure()`
5. Wrap-up, _5m_

Total time: _45m_

### 20240920

#### Diary Bot Series Week 3

- [LinkedIn Event](https://www.linkedin.com/events/buildadiarybot-partthree-mylife7242598596003381248/)

##### Head Transplant

##### 20240920 Introduction

Hello, and welcome to today's session of the `MyLife Open Dev Sessions`! I'm Erik Jespersen, president, co-founder, and senior architect here at `MyLife`. I'm excited to share more about what AI can do for you and for all of us.

Today, we are continuing the critic-acclaimed "Diary Bot Series". Our aim is to create Diary Bot functionality into our baseline platform, and to demonstrate how easy and scalable it is, we'll build it directly in plain view, coding this for you. Come join and collaborate with us, it's easy.

So last week, we enabled our GPT Diary Bot to invite member feedback and store it directly in `MyLife`, illustrating what headless means and creating our intelligent, well semi-intelligent, API consumer, Diary Bot. This episode will see the transplant of the GPT prototype brains _into_ the MyLife instructioning system. 

Before we get any further, thanks so much for joining me today--I really hope you find this valuable. If you do, I'll invite you at the end to help collaborate on this epic project. It's been a lot of things, emotionally and professionally, working on this endeavor, but boring or simple or simple-minded have never been one of them.

Let's kick _all_ the butts. I mean bots. I mean butts.

- [Slide 2: Mission]

`MyLife` is a 501c3 nonprofit member organization that offers its membership, at no charge, an intelligent ai-assisted platform that helps them tell and preserve their cherished memories, stories, media, and ideas for posterity, and share them with others. We are not affiliated with any paid, premium or freemium service, we're trying to coax you with--what you see is exactly what we're trying to achieve.

What is this? `MyLife` is a personal platform that can help cature and share your most cherished nostalgia and ideas with posterity. How is it used? Well, before I show the interface, here are just a few of the use cases we've already been building towards with our initial functionality.

- [Slide 3: Use Cases]

We built this to help those suffering mild memory loss, and better want to capture, relive and identify with stories that make them whole, that they _themselves_ want to hear again... to those wanting to leave behind a time capsule for their two young children you know are about to inherit an over-digitalized and over-infomated world--let this be a time capsule to remember what it was like before the internet, before AI... to those who would benefit from an on-demand partner in self-reflection, in an intentionally private digital sanctuary (where else does _this_ exist?!) to process ideas and emotions, and struggling to come to conclusions about themselves...

It's for all of us. Built by us for us. We are many and varied in our needs.

We begin by building a headless intelligent platform for all of us to use that helps elicit, store, protect, and ultimately **make** intelligent your narratives. According to your explicit consents. AI can make anything linguistically intelligent, including abstractions like: a story, a memory, an idea. For any wondering, this is just one reason why AI is **not** a fad but is illustrative of how AI will _change_ the world.

##### 20240920 MyLife Showcase

- **Walkthrough** [Chrome]
  - [Login](https://humanremembranceproject.org/?type=select) as `system-one`
  - Explain Interface
    - this is all what you get when you become a member of mylife
    - explain Member Avatar: include intelligent client, your intelligent account, digital you. Avatars already coming on the market we are an aggregator, so if you want to use ours, or use another party (or some combination) that is intentional in the platform design
    - Explain Bot Team: team of intelligences here to help you do the work of being human! Start with our cherished memories and narratives as well as innermost thoughts. The stuff you DON'T want to be sending to Google so they can own.
    - Select Biographer and show/explain options
    - chat area and UX
  - share story of today [copy and paste sub-bullet]
    - Today is 20240920; it's been a rush from the beginning, I want to head off to the Cape tonight Brewster area to meet friends, and bring my dog Bryndy. We'll have a wonderful time, but meanwhile I need to allay all my butterflies about today's presentation. I think I'm good, we'll get started shortly. Please save this memory.
  - introduce `scrapbook`
    - show editing options
    - show activation contextualization (how we might contextualize anything)
    - **Relive Memory**

##### 20240920 Learning Objectives

I'll move on to Learning Objectives for today. Get your surgical gloves out, friends, we're about to perform a Diary Bot _head transplant_!

- **GitHub Repository**

We are an open-source public platform, so you can always visit our [codebase on GitHub](https://github.com/MyLife-Services/mylife-maht) to review tickets or progress or you can chat architecture and some engineering directly with our [intelligent codebase GPT](https://chatgpt.com/g/g-oAvQvGv5f-gpt-maht) in desperate need an of an update.

- [Slide 4: Member Login Initialization]

- **MyLife Bots**

Here's a peek behind the curtain at what you get when you become a member of MyLife. What's going on here? This shows a high-level process illustration of some of the things that happen under the hood when you become a member. First off, you receive a Member Avatar, who is the safe preserver of your data and functional controller of your experience. Once built and assigned to you, it creates core intelligences personalized and available _only to you_ to help you store your narratives and legacy. This inital team of intelligences is called the Memory Team and is designed specifically to help you capture biographical and introspective content. So for that team, it creates an initial biographer intelligence who is assigned a combination of dynamic clues and options to both tailor _and_ guardrail, maybe focus is a fine word to use, the member interactive intelligent experience on what you need to accomplish.

We'll dive into the specifics of how we will perform this instructional head transplant in the practical portion, so for the moment, I want to go over the types of "knowledge" we prepare our intelligences with and how. Some are unique to MyLife, but most are germain to almost all Large Language Models (or LLMs).

We think in terms of three types of artificial intelligence that drive our bots.

- Static Knowledge, which we've demonstrated as assigning natural language instruction sets and files
- Dynamic Knowledge, which we demonstrated last week in assigning functions and functionality with MyLife. This refers to the actions and functions that contribute to the capabilities and performance of an intelligence.
- **Personalized Interactive Knowledge**, which we're going to examine a bit today. This dynamic personalization helps not only secure your data, but also promotes an evolving intuitive experience for you, the member.

In our case today, we'll be focused on Interactive Knowledge which reflects the most agile customization of knowledge and context for our bots and how we implement it. We'll see how MyLife personalizes initial instructions to valuably shape the conversation and context-awareness. We'll see a bit how threads are used to both maintain consistency and provide a layer of security for your content, and we'll touch on how Dynamic Options can help round out a member's preferences for bot interaction.

To follow along today, I recommend you have some experience coding with javascript.

Let's dive in!

##### 20240920 Practical Session

- [Pick issue for this week](https://github.com/MyLife-Services/mylife-maht/issues/368)
- How MyLife creates bot intelligences using OpenAI GPTs
  - Member Avatar generates bots for member with a personal factory (with access to datacore)
    - `avatar.mBot()` modular function that determines whether it needs to update a bot in avatar memory or create one; here we're looking at creating, so we look to the factory.
      - => `factory.createBot()` passthrough for modular function
      - => `factory.mCreateBot()` modular function that validates incoming creation request, gathers and compiles instructions and tools, creates with LLM provider, and saves to MyLife.
      - => `factory.mCreateBotInstructions()` modular function that compiles instructions based on created bot type.
      - => `factory.mGetAIFunctions()` modular function that assigns functions based on created bot type.
      - => `factory.mCreateBotLLM()` modular function that saves bot to llm provider.
        - => `llmServices.createBot()` simple sdk call (in comment of issue)
      - => `dataservices.createBot()` factory calls dataservices to push document
- How MyLife designs and assigns instructions
  - [factory.mCreateBotInstructions()](https://github.com/MyLife-Services/mylife-maht/blob/6eeef0fbc362b00c18118313730962f139362082/inc/js/mylife-agent-factory.mjs#L1214)
  - [instructions in system database definition](https://github.com/MyLife-Services/mylife-maht/blob/625897d24e331e04b5e797bef1dc5788af68b0b3/inc/json-schemas/intelligences/biographer-intelligence-1.4.json)
- Convert Instructions
  - `prefix` add flags in addition to interests: `"## interests\n## flags\n"`
  - `general` use notepad and wordwrap to review key functionality and map to new Diary Bot instructions
  - `replacements` like birthdate and name
  - `references` like `## flags`
  - `greetings` determine greetings
- How MyLife designs and assigns functions referenced in instructions
  - [`factory.mGetAIFunctions()`](https://github.com/MyLife-Services/mylife-maht/blob/6eeef0fbc362b00c18118313730962f139362082/inc/js/mylife-agent-factory.mjs#L1422)
  - [`globals.getGPTJavascriptFunction()`](https://github.com/MyLife-Services/mylife-maht/blob/21dfce3e8e0b3cfd051f90a858e84f164e60a4aa/inc/js/globals.mjs#L251)
    - [globals constant mAiJsFunctions](https://github.com/MyLife-Services/mylife-maht/blob/6eeef0fbc362b00c18118313730962f139362082/inc/js/globals.mjs#L5) needs to be addressed and put into database, but this defines the functions that should be available to various bots. In this case we need to add one for `obscure` which will specifically be designed to accept two parameters - the first would be the itemId, and the second would be an array of names that should be disguised; note that these could become objects with relations in order to update the `relationships` dynamic array as well.

Well, it's "that" easy for now, but we have just moved the essential brains from our prototype to our MyLife incubator. Great work on your first head transplant!

##### 20240920 Wrap-Up

- **Lessons learned:** By transplanting the intelligence we tested into the MyLife System we're well on the way to personalizing one's own MyLife Diary Bot. We saw how instructions are dynamically derived on-demand (this demand happened to be _creation_ but we are not limited to that! Upgrades work too...!) to create an exceptional member experience.
- **Get Involved!**
  - We need you!  
  - [Slide 7: What We Need Now()]
  - Volunteers are already incredible, only too few in number: Special thanks this week to Steve, Russ, Avani, Lakshmi, Sheila, Jesse, Jeff and Chris.
- **Next session**: `Week 4: Simon Says` or, Writing New API Hooks, like obscuring a reference

##### 20240920 Outline

1. Introduction to Host, Session, MyLife and the Webinar Series, _5m_
2. Showcase the Current MyLife Member Biography Platform, _10m_
3. Learning Objectives, _5m_
   - How MyLife creates bots using OpenAI GPTs
     - OpenAI `.js` SDK
   - How MyLife designs instructions
   - How MyLife assigns instructions
   - How MyLife assigns functions
4. Practical Session _20m_
   1. Show llm-provider 
   2. Touch on migrateChat() as a requirement for functions
5. Wrap-up, _5m_

### 20240913

#### Diary Bot Series Week 2

##### Headless Diary Bot

##### 20240913 Introduction

Hello, and welcome to today's session of the `MyLife Open Dev Sessions`! I'm Erik Jespersen, president, co-founder, and senior architect here at `MyLife`. I'm excited to share more about what AI can do for you and for all of us.

Today, we are continuing the scintillating "Diary Bot Series". Last week, we built our diary bot prototype in OpenAI predominantly to test the type of instructions that would work. Our indefatigueable volunteer Lakshmi has tested the bot and has some updates. This week we are going to incorporate those changes _and_ assign functionality to our prototype so that it can send summaries of your entries to `MyLife`!

Before we get into the tech today, which still requires **no traditional computer coding skills**, thanks so much for joining me today--I really hope you find this valuable. If you do, I'll invite you at the end to help collaborate on this epic project. I have found this work rewarding and educational in ways I couldn't have imagined, and I'm ready to share some of that learning and labor with you.

- [Slide 2: Mission]

`MyLife` is a 501c3 nonprofit member organization that offers its membership an intelligent platform that helps them tell and preserve their cherished memories, stories, media, and ideas for posterity, and allows them to experience past human narratives. Good news, membership is free to any humans! Our intelligent platform is built by humans for humans.

What is this personal platform that can help cature and share your most cherished nostalgia and ideas with posterity? How is it used? Well, here are just a few of the use cases we've already been building towards with our initial functionality.

- [Slide 3: Use Cases]

From someone suffering memory loss, or even just boredom, perhaps living far away from their family wishing to remember and relive for themselves cherished memories bygone... and then share them with their loved ones. To someone wanting to leave behind their thoughts and emotions for the young children, just growing up in this crazy over-digitalized world they will inherit... To someone with a desire to on-demand have a partner in self-reflection, processing of ideas and emotions, divining conclusions about themselves, and sharing that interaction and its outcomes for themselves in the near or far future... To someone struggling with their identity, desiring a private, protected intelligent space to work through their frustrations and frictions...

Built by us for us. We are many and varied in our needs, and so each of our "MyLife"'s will be our own to use, manage and consent as we wish.

So how do we do this? We built a headless intelligent platform to allow you to store, protect, **and make** intelligent your narratives. AI can make anything linguistically intelligent, including abstractions like: a story, a memory, an idea. This is why AI is **not** a fad and how AI will change the world.

##### 20240913 MyLife Showcase

Now? Less expository, more demonstration. Let's take a look behind the scenes at the `MyLife` Platform.

- **Walkthrough** [Chrome]
  - [Login](https://humanremembranceproject.org/?type=select) as `system-one`
  - Explain Interface
    - this is all what you get when you become a member of mylife
    - explain Member Avatar: include intelligent client, your intelligent account, digital you. Avatars already coming on the market we are an aggregator, so if you want to use ours, or use another party (or some combination) that is intentional in the platform design
    - Explain Bot Team: team of intelligences here to help you do the work of being human! Start with our cherished memories and narratives as well as innermost thoughts. The stuff you DON'T want to be sending to Google.
    - Select Biographer and show/explain options
    - chat area and UX
  - share story of today [copy and paste sub-bullet]
    - Today is 20240913 I'm still cramming to get today's diary bot series done, it's looking good, but time squanders and fleets. I've got the opening script and my pieces, I just need to organize them and then wait for Joan and Hugh to come pick Margaret up for the beach, which I cannot go to today, for this MyLife work. Which is totally fine. I mean it. Really. No sarcasm. I do love it, but on a day like today, with beating heating sun, a known part of me would prefer to be there with my friends. But this is important to me, and it's a great learning experience for me, and a way to build more information about how the platform works without having to directly write all the documentation myself, as a lot of this is coming out in last-minute slides and loudmouthed scripting. Not yet _too_ nervous, would like to keep it that way! Please save this memory.
  - show editing options
  - show activation contextualization (how we might contextualize anything)
  - Relive Memory

##### 20240913 Learning Objectives

- **Headless**: What it means, sure, any frontend, but we need to think about the future and what happens when Intelligent platforms will talk to intelligent clients, and your MyLife Member Avatar (explained earlier) is exactly such a "smart" client. Any "semi-"intelligent consumer can conduct your consented business with MyLife. By end of this, when we make the OpenAI GPT prototype Diary Bot the main interface through which one integrates with MyLife.
- **"static" knowledge** focus for today, with allusions to dynamic (json schema)
- **Connecting Dots and Bots**: Using GPT and MyLife API (extant functionality) to connect prototype from last week to MyLife. No code environment.
- **Test GPT/Bot**: Use public links to test and improve (which include feedback)

##### 20240913 Practical Session

**IMPORTANT**: Never show `mbr_id` for any entity, and if so, in worst case, test case of Spritz.

- [review master issue with Diary Bot Specifications](https://github.com/MyLife-Services/mylife-maht/issues/347)
  - scroll to week 2: Headless Diary Bot
  - Share in Zoom
- [show and explain JSON Schema Ticket](https://github.com/MyLife-Services/mylife-maht/issues/355)
- [review previous instructions](https://github.com/MyLife-Services/mylife-maht/issues/348#issuecomment-2334520687)
- [review feedback from Lakshmi](https://github.com/MyLife-Services/mylife-maht/issues/349#issuecomment-2339091319)
- [review Diary Bot Prototype updates](https://chatgpt.com/g/g-rSCnLVUKd-mylife-diary-bot-prototype)
  - Go over how individual instructions were updated, included or moved to interface resolution (ex. Flagging for now)
- click through to actions describe what they do
  - **NOTE** sometimes need to destroy all actions and start again
  - Authentication in GPT
  - [demonstrate original Schema in GitHub also](https://github.com/MyLife-Services/mylife-maht/blob/base/inc/yaml/mylife_biographer-bot_openai.yaml)
  - Test in GPT area
- Test on public GPT
  - keyValidation
  - test story
- Confirm Save in `MyLife` database (talk through while doing)
  - find ID in VSCode Server log
  - Azure find entry
  - Copy and Paste into Notepad
  - erase id, mbr_id
  - share document
- **You** can Do Better than the AI GUY! (referring to initial instructions) This is a first draft, what would you do differently? Of course you can, even if just because you prefer to have yours act a little differently than the MyLife vanilla version.
- You have just built a diary assistant that has direct access to populate your MyLife account. Bravo! Now wait until you learn how to build one _inside_ of MyLife starting next week!

##### 20240913 Wrap-Up

- **Lessons learned:** You built your own Bot! And that's part of what we mean with headless, any interface can be connected through validation and verification to our system by design. And further, we are tailoring that design towards an end-state where we will have intelligent clients handshaking, validating, negotiating, contracting and otherwise interacting with our intelligent platform with their human driver at the helm.
- **Get Involved!**
  - We need you!  
  - [Slide 7: What We Need Now()]
  - Volunteers are already incredible, only too few in number: Special thanks this week to Steve, Sheila, Mark, Avani, Lakshmi, Russ, Todd Nilson from Clocktower Advisors, Diane Tarshis from Startup Distillery and our ED candidates!
- Winner: Break the Bot! It's up! It exists
  - [share link in Zoom](https://chatgpt.com/g/g-rSCnLVUKd-mylife-diary-bot-prototype)
- Next session: `Week 3: Dear Diary, Please Fetch My Carriage` or, Writing New API Hooks, like redacting

##### 20240913 Outline

1. Introduction to Host, Session, MyLife and the Webinar Series, _5m_
2. Showcase the Current MyLife Member Biography Platform, _10m_
3. Learning Objectives, _5m_
4. Practical Session _20m_
   1. Diary Bot in GPT, _10m_
   2. MyLife Validation, _10m_
5. Wrap-up, _5m_

Total time: _45m_

1. Brief introduction to the MyLife Platform **MAX** _5m_ @2:05pm
   - Introduce Self, current president and co-founder [Slide 1: Title]
   - Introduce MyLife [Slide 2: Mission] [click here to access content](#about-mylife)
   - Introduce Use Cases and Platform [slide 3: Use Cases]
2. Showcase the Current MyLife Member Biography Platform **MAX** _10m_ @2:15pm
   - [Login](https://humanremembranceproject.org/?type=select)
   - Walk through the **current MyLife member biography platform**.
   - This helps participants see MyLife in action, showcasing its **flexibility and power**.
3. Learning Objectives **MAX** _5m_ @2:20pm
   - **Headless**: What it means, example of what we've done
   - **"static" knowledge** focus for today, with allusions to dynamic (json schema)
   - **Connecting Dots**: Using GPT and MyLife API (extant functionality) to connect prototype from last week to MyLife. No code environment.
   - **Test GPT/Bot**: Use public links to test and improve (which include feedback)
4. Practical Session **MAX** _20m_ @2:40pm
5. Wrap-up _5m_ @2:45pm
   - Recap the lessons learned
   - How to contribute/get involved [Slide 7: What We Need Now()]
   - Volunteers, Thank Steve, Sheila, Mark, Avani
   - Winner: Break the Bot! It's up! It exists - send link
   - Next session: `Week 3: Dear Diary, Please Fetch My Carriage` or, Writing New API Hooks, like redacting

- hack-a-thon/looking for holes/Red Team
**note** have lots of content to paste in for playground demonstration, or generate on demand by other GPT - lol yes this

### 20240906

#### Diary Bot Series Week 1

##### Introduction to MyLife and Conceiving the Diary Bot

This represents the kickoff of a series dedicated to bot-construction and MyLife Bot Team expansion. In this instance, we will explore the diary-bot and how its requirements might be outlined to meet the needs of User Persona `Jhon`.

##### 20240906 Outline

Exploring the MyLife Platform and Conceiving an AI Diary Bot

1. Introduction to Host, MyLife and the Webinar Series, _5m_
2. Showcase the Current MyLife Member Biography Platform, _10m_
3. Learning Objective, _5m_
4. Practical Session _20m_
   1. Review Diary Bot Specifications, _5m_
   2. Stand Up Diary Bot in GPT Teams, _15m_
5. Wrap-up, _5m_

Total time: _45m_

1. Brief introduction to the MyLife Platform **MAX** _5m_ @2:05pm
   - Introduce Self, current president and co-founder [Slide 1: Title]
   - Introduce MyLife [Slide 2: Mission] [click here to access content](#about-mylife)
   - Introduce Platform [Slide 3: Roadmap Slide] [click here to access content](#about-mylife-platform)
   - Segue, referring to Diary Bot on graphic
2. Showcase the Current MyLife Member Biography Platform **MAX** _10m_ @2:15pm
   - [Login](https://humanremembranceproject.org/?type=select)
   - Walk through the **current MyLife member biography platform**.
     - Select Biographer
     - Tell it story of today [copy and paste sub-bullet]
       - Today is 20240906 and I am slated to give a presentation today on how to build a diary bot. I'd love to say I'm not nervous. Should I have had those four cups of coffee this morning? It was wonderful to talk with Steve and walk through the presentation. He's on the board of MyLife also. My wife ran out to grab some lunch just after we played Frisbee with Bryn -- she's a rescue just a 5 years old this December and the best at Frisbee you'll see! I had a delicious Banh Mi, it was delicious, but didn't help my nervousness. The AI development session is going to begin in just a few minutes. Zoinks! Please save this memory.
     - see results
     - show editing options
     - Relive Memory
   - This helps participants see MyLife in action, showcasing its **flexibility and power**.
3. Learning Objectives **MAX** _5m_ @2:20pm
   - **Basic AI Structure and Knowledge Concepts**: Using GPT and MyLife tools to build personalized bots [Slide 4: Roadmap Slide]
   - **SHARE** Edge [TAB: Public MyLife GPT](https://chatgpt.com/g/g-rEjoOt9hN-mylife)
   - **Create and Test GPT/Bot**: By the end of the session, participants will be able to start testing diary functions using GPT in the MyLife playground
4. Practical Session **MAX** _20m_ @2:40pm
   - MyLife Repo: Show & Copy/Paste into Zoom [TAB: MyLife Code Repo](https://github.com/MyLife-Services/mylife-maht)
     - https://github.com/MyLife-Services/mylife-maht
   - MyLife Current Alpha Project: [TAB: MyLife Alpha Project](https://github.com/orgs/MyLife-Services/projects/13/views/1)
   - Review Diary Bot Issue [TAB: MyLife Issue #347](https://github.com/MyLife-Services/mylife-maht/issues/347)
   - Explain specifications and how they will be included
   - Provide a hands-on session where participants work with GPT tools in the MyLife Playground to create a basic diary entry summary in the system
   - **You** can Do Better than the AI GUY! (referring to initial instructions) This is a first draft, what would you do differently?
5. Wrap-up _5m_ @2:45pm
   - Recap the lessons learned
   - How to contribute/get involved [Slide 7: What We Need Now()]
   - Volunteers, Thank Steve, Sheila, Mark, Avani
   - Winner: Break the Bot! It's up! It exists - send link
   - Next session: `Week 2: Dear Diary, Please Fetch My Carriage` or, Writing the API Hooks

- hack-a-thon/looking for holes/Red Team
**note** have lots of content to paste in for playground demonstration, or generate on demand by other GPT - lol yes this

### 20240830

- Initial live version

#### 20240830 Outline

- Brief introduction to the MyLife Platform **MAX** _5m_ @2:05pm
  - Introduce Self, current president and co-founder
  - Introduce MyLife (mission `slide`) [click here to access content](#about-mylife)
  - Introduce MyLife Tech (what MyLife is `slide`)
  - Introduce Session, Theme and Segue: AI for All of Us (engineering and interface `slides`)
    - The MyLife AI Open Dev Sessions are about empowering all of us with the ability to create solutions that matter to humanity--"By Humanity, for humanity." The type of network the internet promised, but the work required to execute and deliver on this promise fell to workhorses intent on corporatizing the internet. Largely successful.
    - MyLife and these sessions are AI for All of Us
    - We've been thinking for years now about the values and philosophies _behind_ MyLife, its organizational structure and what we can offer and afford one another when we put our technology to the test, and we've been passionate about consent, digital dignity, digital equity and justice--all of which baked into our basic mission and illuminated in the intelligent software platform we developed. Setting ourselves on this journey to design a system around the idea of "AI for All of Us", I'm so excited and happy to be able to share with you our lessons learned and our lessons _learning_, that we bring to the platform, to our members and to you.
  - Demo
    - I need to save a new memory: I woke up this morning 20240830 and had some coffee and helped the contractors and then I prepared for a mylife open dev session in zoom. Got a Lyft ride from a very nice driver who brought me to Delphine's that was far too crowded so I opted for some corner pizza (which has changed hands) instead; it was okay, but not the sort of crust I most enjoy, but the counter cooks were nice. Then I went to the library to almost intrude on another meeting in the Fogg room, and now I am sitting upstairs at the Beverly Library waiting to get into the Open Dev Session at 1:45pm ET; do I even have time to be nervous? please create that and save it
- Learning Objectives **MAX** _10m_ @2:25pm
  - Current LLM Technology as evidenced by Corporate Intelligence: Q
    - represents static(ish) knowledge [no coding necessary] defines boundaries of inherent repeatable knowledge
      - best practice instructions and files
        - Markdown headers with internal references when pertinent `[]()`
        - References to knowledge objects
        - "Modes" description
    - dynamic knowledge and memory [beginner coding]
      - actions
      - functions
      - database
    - personal on-demand knowledge and memory [advanced coding]
      - bot teams
      - experience-driven dynamic scripting
      - forced modes
      - personalized instructions
      - threads
    - bring together under one platform roof
- Practical Session **max** until _10m_ **remaining** @2:50pm
  - Pick Ticket: [GitHub Issue](https://github.com/MyLife-Services/mylife-maht/issues/341)
    - show projects?
  - Solution on: [MyLife OpenAI Agent](https://chatgpt.com/g/g-rEjoOt9hN-mylife)
  - In VSCode:
    - `mylife-help-documentation.md` - for issue, has instructions (explain testing mechanics)
    - `core.mjs` - for Q illustration in code
  - Include **Maht** in development
- Wrap-Up
  - Thank you! For watching!
  - why contribute?
    - Professional Development, learn against an ai-first platform
    - make a difference and give back (why I do it)
  - how contribute?
    - DM me on LinkedIn! paste into zoom
      - https://www.linkedin.com/in/megalomedia/
    - Volunteers!
    - [github repository](https://github.com/MyLife-Services/mylife-maht)
    - register for membership!
      - Alpha Pilot right now, open to volunteers
  - [github repository](https://github.com/MyLife-Services/mylife-maht)
  - call for talent
    - UI/UX
    - ED
    - Daring imagination is what we need now; I failed to imagine 3-years ago the scope of what is already possible

### 2024823 - initial prototype

#### 1. Introduction to MyLife Platform _10m_

- Brief overview of the MyLife Platform
  - mission as a nonprofit dedicated to serving humanity, public utility for remembrance and personal benefit
  - initial intent: narratives, but now so much more with bot teams
  - how we do it: walkthrough of absolute basics: **watch time**
- Highlight the volunteer team behind it and their commitment to integrity and empowerment through technology.
- Set the tone for how the session aligns with the mission of building global solutions that benefit everyone
  - better way to be remembered - how the 21st century human _can_ be remembered
- Humanity First: Empowerment with Integrity
  - Kick off the session with a message like “In today’s world of AI, we believe in putting humanity first. Let’s build tech that serves us all.”
  - Relate it to MyLife's goal of creating human-centered AI solutions that align with personal empowerment and global good.
  - Tools for _us_, not _business_ - web 2.0 was corporate takeover
  - Q as representative, equally our avatar representative of us

#### 2. Learning Objectives _5m_

- Focus on the purpose of the session: Learning to develop corporate intelligence solutions within the MyLife Platform.
- Highlight the learning points:
- Exploring instruction-sets and AI integration.
- Using MyLife APIs for corporate data intelligence.
- The role of the core systems like `core.mjs` and `mylife-avatar.mjs`.
- Align the learning with the mission of fostering open-source solutions that contribute to a better world.

#### 3. Practical Sessions: Pick a Ticket and Go _30m_

- Introduction (5 minutes):
  - Pick a Ticket:
  - Explain the practical session: participants pick a development ticket (task).
  - Describe the use case and expectations for each ticket.
  - Acknowledge contributors who helped set up the tickets.
  - Introduce "Q" Variants:
  - Discuss how the "Q" corporate intelligence framework operates within the MyLife Platform, utilizing GPT models, APIs (corporate intelligence modules), and core functionalities (`core.mjs` and `mylife-avatar.mjs`).
  - Explain how "Q" is executed inside the platform to display on-screen intelligence and responses.
- Work Session _25 minutes_
  - Participants start working on their selected ticket.
  - Encourage collaboration and questions during this time.
  - Frame this as a collective contribution to the global public good, emphasizing the role of their work in helping the community and promoting ethical AI.

#### 4. Wrap-up _10-15m_

- Q&A (10 minutes)
  - Address participant questions about the session, code, or platform.
  - Emphasize community-driven development, volunteer opportunities, and how contributions help maintain integrity within the platform.
  - Encourage questions about how to contribute, improve, or expand the MyLife Platform.
- Alternative if No Questions (5 minutes):
  - Use this time to walk through how to set up the environment for contributing to the MyLife platform (as a precursor to the detailed environment setup tutorial).
  - Provide insights on how to push contributions to the global codebase:
    - Explain contribution guidelines and procedures.
    - Highlight how every contribution, big or small, supports the nonprofit’s mission of empowering individuals and communities through AI.

## Appendix

### Empowerment Through Technology

- **AI for the People**: MyLife stands as a beacon for the ethical use of AI, designed to empower individuals and organizations, not just with technological prowess, but with the tools to make meaningful decisions that positively impact lives.
- **Human-Centered AI**: MyLife AI isn’t just a tool; it’s an extension of human potential. Our bots, data services, and APIs are designed with one goal in mind: enhancing the capacity of individuals to manage, understand, and grow in their personal and professional lives.
- **Accessible Tools for All**: We believe that everyone should have access to the most powerful tools available, from individuals managing their own lives to corporations handling vast datasets. The MyLife platform levels the playing field, giving small-scale contributors access to the same advanced AI that powers the world's largest organizations.
- **Volunteer-Driven, Mission-Focused**: MyLife’s foundation lies in its dedicated volunteer team, a global community committed to creating AI solutions that serve the greater good. Their work isn’t driven by profit but by a shared vision of technology that uplifts humanity. This gives every contribution greater meaning and ensures that integrity remains at the forefront of our mission.
- **Contributing to Something Greater**: Every contribution to MyLife isn’t just about code; it’s about building a system that empowers others. By contributing to our platform, developers and volunteers are helping shape a future where people can use AI to navigate complex corporate landscapes, make informed decisions, and improve their quality of life.
- **Integrity as a Guide**: MyLife embodies the belief that empowerment without integrity is hollow. Through our platform, users gain the power to shape their future while being guided by principles that ensure their actions have a positive impact. This aligns with the larger mission of MyLife to not only create powerful AI solutions but to ensure these solutions are used in ways that foster trust, compassion, and responsibility.

#### Quotes

- Maht: Our work is like a puzzle, where each piece—whether it’s a single line of code or a new instruction set—helps complete a picture of human empowerment
- Maht: Empowerment isn’t about giving someone power over others—it’s about helping them harness their power for one's betterment and the greater good, driven by integrity and a sense of purpose

### About MyLife

Hello and welcome to the MyLife Open Dev Sessions exciting new `Diary Bot Series`

I'm Erik Jespersen, president, co-founder and currently the senior architect and lone developer. Looking to change that and hoping to get you interested in what AI can do for you and for all of us.

Thanks so much for joining me today, I hope you find this valuable. If you do, I'll invite you at the end to help collaborate on this epic project.

MyLife is a 501c3 nonprofit member organization that offers its membership an intelligent platform that helps them tell and preserve their cherished memories, stories, media, and ideas for posterity, and allows them to experience past human narratives. Good news, membership is free to any humans, but only; no corporations, no ai's, no fictional characters. Our intelligent platform is built by humans for humans. And that's a bit of what we're here to talk about. What does it mean: AI for all of us?

### About MyLife Platform

MyLife guides you through the journey of crafting and sharing your digital self and digital legacy with posterity.

Let's take a look at this slide for a moment, it's a complex jumble, but I just want to share with you what you get when you become a member of MyLife.

explain graphic in sentence coding holes and top/bottom

First you get a personal member avatar. This is an intelligence that essentially _is_ your MyLife Account. It is a digital intelligence that is meant to interact with you _and_ when invited and consented, digitally act _as_ you sharing your selected content with others as you consent.

So you get this avatar, and then you get its ability to control an out-of-the-box team of bot intelligences called the 'Memory Team' that helps you collect, enhance, improve, relive and share your cherished memories, ideas and narratives for posterity.

MyLife, as a technology, is an open-source headless, intelligent api platform server, leveraging minimal opensource javascript server frameworks. MyLife currently uses the OpenAI SDK for all of its LLM services, but the larger aim is to be model agnostic, being an aggregator, the likes of which many of you have already seen on the market.

The frontend is currently a "work-in-progress" and in need of much improvement (I'll talk more about getting involved later). It represents a relatively minimalistic visual interface for our membership to interact with the intelligent platform. MyLife's aim is to afford its avatars with the ability to self-generate their user-interfaces in entirety on-command of login. We're a ways off from that, but it's a circular process of intelligent host speaks to intelligent client comin' o'er the Rye.

With that caveat, and a call out to designers, Let's take a look!

### About MyLife AI Open Development Sessions

MyLife AI Open Development Sessions offer a free, inclusive invitation to anyone interested in harnessing AI for human-centered solutions, led by the expert team behind the nonprofit, open-source MyLife Member Services Platform. This configurable, intelligent API system empowers developers, creators, and individuals alike to contribute to a global humanist network that ensures privacy, posterity, and accessibility for all.

This series is designed to benefit anyone, from seasoned developers to beginners, with or without traditional coding experience. Discover how AI can drive not just technological, but also societal progress through equitable, ethical practices.

Join us for free and be part of the movement to ensure every human legacy is digitally preserved and celebrated in perpetuity.

[Live Event Link](https://us02web.zoom.us/meeting/tZAsduuvrz8qEtKQLZbVlsfuktejbb6iBS6T/ics?icsToken=98tyKuGsrzooHdWRsBGBRpwIBYj4a-3zmClfj7d2rTPfARZfcQXjPfZHOLB9RtHy)

### Dev Session Format

- Brief introduction to the MyLife Platform [powerpoint] & [MyLife-Website](https://humanremembranceproject.org)
  - Introduce Self
  - Introduce MyLife (mission slide)
  - Introduce MyLife Tech (what it is slide)
  - Introduce Theme and Segueway (interface slides)
  - Demo
    - Yes one per session in my own _personal_ bio, since I'm doing it and it's true
- Learning Objectives
  - put a birdbrain on it!
- Practical Session
  - expect and outline certain outcomes
  - vet material for privacy
  - demonstrate engagement with products and bots
  - Include **Maht** in development
- Wrap-Up
  - Thank you! For watching!
  - how contribute?
    - Volunteers!
  - why contribute?
  - [github repository](https://github.com/MyLife-Services/mylife-maht)
  - call for talent

- [ ] Create backup slip - Focus on thanks and volunteer appreciation

### Asides

#### Avatar Marketplace

Some of these Replikas, You, but Virtual solutions are currently coming on the market, but none missioned to provide you secure, protected data privacy and ownership. That's one tiny way in which MyLife is different.

There are objects coming on the marketplace that offer this intention, Replika, Digital You, I'm sure you're seeing a lot of these already that are curios for the moment, but the Big Tech understands the results of this bonding with a digital entity is the only valuable data it has to mine, since they exist and are in situ to exploit our attention rather than elevate it. You will be offered many suits of armor, and it is in MyLife's interests and direction to partner with the those similarly missioned.

The frontend itself currently is a combination of HTML5, CSS and javascript. It is endeavoring upon emerging GenUI principles of _Consent and Control_ architecture, so that a frontend intelligence can negotiate an array of interactional experiences with an intelligent API service. We'll get more into that in the coming months, though I'll shortly show an example of this.

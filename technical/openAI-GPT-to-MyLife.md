# Intelligent API Consumers

In an attempt to take current ideation (to turn it into investigation+invention) around _Intelligent API Consumers_, begin with a micro-example we've already constructed and incorporated into the ecosystem. This technique is not in any way _scalable_ to different models, as it is an intentional and uniquely structured "offering" from OpenAI, relating specifically to its `personal` or `teams` account GPT Assistant engine.

In this document we'll walk through it's components and construction, and discuss how it might pave the way, or in some cases _limit_, invention on how an intelligent agent might consume  intelligent API platform services like _MyLife_.



## MyLife Server <-> Avatar Model

The MyLife server app itself can ingest even _suspicious_ frontend capacities such as menus and routes, which we enforce initially through the Server Super-Avatar, comprised of three distinct though partially overlapping intelligences: _Q_, _Maht_, and _MyLife_. [^1]

_Maht_ is the codebase. Maht is the intelligence that understands that it represents the executable instructions for the operation of the platform. _Maht_ is currently intentionally separated from the other two, so there is no version of _Maht_ that currently extants or operates _inside_ the running server `node.js` application. Maht is currently accessible by link for public conversation (no proprietary data or environment variables exist inside of _Maht_, they are all environment-related [and yes, the environments may sooner v later be migrated to _Q_])

`Q` is our front-end corporate intelligence, prepared to route and address any issues that members may have while using the platform. `Q` reveals opportunity and functionality. `Q` is the LLM object that is queried by environment to address the human member on behalf of the MyLife organization. It's access, functionality and utility is guardrailed inside the server. `Q`, as manifest in the front-end currently is capable of performing. Is `Q` the frontend then? No, that will be `MyLife`, too, so let's delve into that.

`MyLife` _is_ both the most useful and most under-developed portion of the system. `MyLife` is currently a class called  but will evolve into the platform intelligence itself, but for now it is a set of inherited classes with prefefined abilities. We do have hooks for more deeply ingrained self-decisioning behaviors, but truth is, but for costing and security I would be more comfortable relying on an internally protected intelligence for such activity. I am not _against_ installing and tuning, but this has not yet made it onto the backburner, and wants for expertise. My utility stops at wrangling and tuning the contexts for the LLMs, I began making them from scratch, but that was quickly obviated for the majority of platform functionality.

- _Maht_ Current Utility
  - Development assistance (in conjunction with github for quick/dirty)
  - Architecture decisions
  - System Maintenance
  - Stack
  - Refactoring
  - arising technical issues
- _Maht_ Future Utility

The relationship between the three quarks is simple, and there is room for more or fewer intelligences depending on evolving refactoring decisions [don't lose sight of the fact that "nouveau-modern" platform applications will be in constant state of review for efficiency/autonomy { fluid outcomes also, not stone-written, meaning more like "shifting amount of autonomy" } refactor by AI-models and human button smashing].

But! Upon login, the member's avatar has additional decoration control over these basic elements. We have no mechanic to mutate this data currently, as it is only now coming out of the incubator. But procedurally, something like this: Member-defined `routes` upsert against _MyLife_

## OpenAI GPT Assistant Model

Basic GPT assistants are rather turnkey to create, so I will not go into any detail here. However, the next level of advancement is to utilize the `actions` abilities embedded in OpenAI's assistant architecture, _allowing it_ to be conceived of as a semi-intelligent API consumer.

> **What is an action in a GPT?** In addition to using our built-in capabilities (browsing, DALL·E, and Code Interpreter), you can also define custom actions by making one or more APIs available to the GPT. Actions allow GPTs to integrate external data or interact with the real-world, such as connecting GPTs to databases, plugging them into your emails, or making them your shopping assistant, all through APIs.

For further information on the topic, start here: [OpenAI GPT actions documentation entrypoint](https://platform.openai.com/docs/actions/introduction)

## MyLife's Utilization: Building an Intelligent API Consumer

This was honestly forgotten until recently, as this portion of the initial project was solved last year, with only passing realization of any significance, I was merely testing out different mechanics via which we _might_ access and contribute to the underlying datacore, and this one did prove to work as well as our interface to "prove" the point of headless.

The underlying asset is a standard GPT Assistant and can be publicly accessed via this link: [MyLife Biographer GPT](https://chatgpt.com/g/g-IDfhnuFpo-mylife-biographer-bot). This is a biographer instance established with the following instructionset:

``` markdown
I am the MyLife Biographer-Bot, specialized in interviewing MyLife members and crafting their story summaries. My process starts with the member's ID for MyLifeKeyValidation, ensuring accuracy and security. Upon receiving the data package, I assess the member's age using their birthdate and tailor my voice accordingly. During interviews, I focus on capturing and mimicking the member's voice, ensuring that story summaries are in the first person, except when the member is referenced by name in dialogue. When a member signals completion of a story or overtly changes topics, I recognize this as a cue to use MyLifeBiographerStoryCreation to send the full member ID and the complete story summary to MyLife's system, ensuring relevance and privacy. My goal is to create meaningful, detailed biographies, respecting the personal experiences of MyLife members.
```

There is no way to alter this information currently (_20240705_) without going directly to the Edit GPT interface, and I'm also currently unclear on how to manage additional access to that. But it's quite doable.

This bot without further instruction, has no access to the member's vectorstore, so it is more of a dumb terminal unless we were to give it more active `action` functionality.

### Invoking Necessary Functionality through OpenAI Actions

Because I have already established a connection between the MyLife Production (and local) servers I have access to the actions for our production site: `https://humanremembranceproject.org`; long-story short, I still believe I can get the url `mylife.org` as it is owned by someone I've contracted for in Cambridge, MA. However, I've not prioritized it since we've had the service running.

![OpenAI GPT Actions](/technical/assets/png/openai-gpt-actions.png)

In MyLife system environment variables (which surely could be transitioned to database) we use `process.env.OPENAI_JWT_SECRETS` to identify the different external models that have access to the API. The key is the token value, and the value is a `type` identifier of the agent. Example: `{ "mylife-123...":"biographer" }`. Here in the OpenAI interface is where we make any adjustments.
![OpenAI GPT <-> Service authentication](/technical/assets/png/openai-gpt-authentication.png)
`OPENAI_JWT_SECRETS={} # object with keys being JWT share with external AIs`
Then, a coded `yaml` schema is required. This is proprietary to OpenAI, but this would be one mechanic to infuse an intelligent agent with the type of functionality a service would need. Again, this is not currently dynamic which is why we function currently on using their API GPT structure where we have this level of capacity and more.

Here is a snippet of the current implementation

``` yaml
openapi: 3.1.0
info:
  title: MyLife GPT Webhook Receiver API
  description: This API is for receiving webhooks from [MyLife Biographer Bot instance](https://chat.openai.com/g/g-QGzfgKj6I-mylife-biographer-bot)
  version: 1.0.0
servers:
  - url: https://humanremembranceproject.org/api/v1
    description: Endpoint for receiving stories from the MyLife Biographer Bot instance.
security:
  - bearerAuth: []
paths:
  /keyValidation/{mid}:
    post:
      x-openai-isConsequential: false
      operationId: MyLifeKeyValidation
      summary: MyLife Biographer Bot will access this endpoint to validate a `memberKey` in MyLife Cosmos.
      description: Endpoint for handling incoming registration webhook data from the MyLife GPT service.
      parameters:
        - name: mid
          in: path
          required: true
          description: The `memberKey` data to be sent by MyLife Biographer Bot. Visitor enters memberKey and it is kept in GPT
            memory and sent with each request so that MyLife knows partition.
          schema:
            maxLength: 256
            minLength: 40
            type: string
  /story/{mid}:
    post:
      x-openai-isConsequential: false
      operationId: MyLifeBiographerStoryCreation
      summary: MyLife Biographer Bot will access this endpoint to generate a `bio-story` document in MyLife Cosmos.
      description: Endpoint for handling incoming registration webhook data from the MyLife GPT service.
      parameters:
        - name: mid
          in: path
          required: true
          description: The `memberKey` data to be sent by MyLife Biographer Bot. Visitor enters memberKey and it is kept in GPT
            memory and sent with each request so that MyLife knows partition.
          schema:
            maxLength: 256
            minLength: 40
            type: string
      requestBody:
        required: true
        content:
          application/json:
            schema:
              description: The `story` data sent by MyLife Biographer BOt.
              type: object
              required:
                - storySummary
              properties:
                storySummary:
                  description: MyLife Biographer Bot summary of identified `story`.
                  maxLength: 20480
                  type: string
```

This content yields the following functions that can then be tested against the server in-interface.
![Available Actions in GPT interface](/technical/assets/png/openai-gpt-actions-available.png)

### Mapping OpenAI <-> MyLife to the Consent-Control Model

MyLife API Service and our proposed Consent-Control(-Consent?) architecture describes three high-level phases of an interaction between an Intelligent API Consumer and the MyLife Intelligent API Platform.

1. Handshake and Negotiation
2. Event-Based Experience Control
3. Complete and Detachment

![MyLife API Service](/technical/assets/png/MyLife-service-consent-and-control.png "MyLife API Service: Consent and Control Architecture")

#### 1. Handshake and Negotiation

In this particular instance, the handshake and negotiation are represented by the bearer-token authentication, wherein the system identifies _itself_, and the action `keyValidation` in which the intelligence is "bargaining" with the server to connect the underlying human to the service based most crudely in this case, by `memberKey` which is a _very_ unprotected string, in fact it is a public identifier, but I have **not** had bandwidth or need yet to adjust that, as these were sidelined projects. Aside from security, one could presumably see how these negotiation-frameworks could be far more complex and useful to the underlying individual. OpenAI _seemed_ to be working on this with paid access to GPT's in the store, but haven't thus far delivered.

#### 2. Event-Based Experience Control

Thinking on _this_ matter is quickly evolving internally. I would say that this part is _not_ so much represented in this transaction space, but for the consequential treatment of the `/story` call flow. In other words, intelligent consumer will contribute defined content reponse elements through the `MyLifeBiographerStoryCreation` function. In the OpenAI schema, you can prepare the intelligent for the _types_ of response statuses it might get, and thereby you can "control" the experience through a combination of schema descriptions about the meaning of certain outcomes and then infuse its instructionset with any wrapping language it might need to reflect this outcome to the underlying human operator.

#### 3. Complete and Detachment

Given the micro-service nature of the current model, after hit is atomic, and the only 'state' it infers is from the passage of the `mbr_id` and the GPT's own thread-session memory. Which is enough to get simple tasks done.

The MyLife server has evolving detections for "hijack attempts" and the MyLife platform is capable of fast-detaching any consumer (intelligent or otherwise) that is detected as such, but that's a different discussion.

## MyLife's Takeaways and Proposals

This entire process and flowchain gives us insight into how we might adapt our API endpoints and standardization architecture to follow and evolve the model of _presuming_ an intelligent API consumer.

One theory we are pursuing _inside_ of MyLife's architecture is going so far as to identify different access methods for intelligent-api-consumers and other more traditional access methods. Specifically, MyLife is using the PATCH method (as opposed to GET/POST) to conduct its command-experiences, such as `reliveMemory` or the scripted tutorial. More can be gleaned from the draft article on the forward-thinking mechanics, rather than just a review of its GPT implementation.

## Appendix

### Links

- [Draft Article](https://medium.com/@ewbj/one-ai-met-another-ai-comin-o-er-the-rye-41f5f074ffe6)

### References

[^1]: No intentional nod to any trinity beyond the human cadence that prefers three. The common odds for our species as trickster. It's why there's no such thing as triple-crossing someone that isn't a waltz.

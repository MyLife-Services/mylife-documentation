# MyLife `Experience` Code

## Overview

The MyLife `Experience` system allows members to create dynamic, interactive narratives using AI-driven scripts. These `Experiences` are designed to capture, curate, and showcase personal stories and memories in an engaging and meaningful way. This README provides an overview of the `Experience` scripting system, key system cast members, and guidance on how to code and manage these `Experiences`.

### Handcuffing the AI

An `Experience` itself, and one of the reasons it is disruptively revolutionary, is that, as a mechanic, it directly puts our creative humanity before the wandering interests of human recipient and obliging ai-agents. 

Encounters with AI have not yet been guardrailed, all for the better thus far. But creatives, and additionally those who don't want to just "hand over the keys" to "ai", together have not consolidated around a vision of how to wrangle the encounter and experiences of their online content with copyright protection and the right to determine whether an AI is being `wisened` by their work for free.

What _MyLife_ does is put the member first in designing the encounters they would like to devise for others, whether they are intelligent, personalized greeting cards we share with a friend, or a multi-act immersement that leads the experiencer through your screenplay scene-by-scene, it is doable with a _MyLife_ experience.

For the experiencer, it's a lot like a first person video game where each character they meet is designed by you, or _is_ you! But _you_ are in control of the experience and to the degree you choose, the outcomes.

## Scripting `Experiences`

`Experiences` are scripted interactions that can be customized and tailored to individual members. They are represented as JSON objects, allowing for flexibility and integration with AI tools that assist in natural language processing and script generation. The goal is to enable members to craft their stories in a way that is both personal and interactive.

### JSON Structure

Each `Experience` is structured as a JSON object containing various elements such as dialog, actions, and conditions. Below is a brief but illustrative example of an `Experience` JSON object, and how to elicit some of the guardrailed flow you desire.

```json
{
    "autoplay": false,
    "being": "experience",
    "cast": [
        {
            "icon": "Q-00",
            "id": "88043968-d7ef-4a57-a923-335bc9f92793",
            "name": "_Q_",
            "role": "Q, AI Avatar for MyLife",
            "type": "Q",
            "url": "mylife.png"
        },
        {
            "icon": "member-00",
            "id": "88043968-d7ef-4a57-a923-335bc9f92795",
            "name": "Your Personal Avatar",
            "role": "Herald of @@name",
            "type": "member-bot",
            "url": "avatar.png"
        },
        {
            "icon": "Q-01",
            "id": "4dd179a3-bf96-4716-b631-9c21071a34df",
            "name": "MyLife Actor",
            "role": "Guide @@guide",
            "type": "system",
            "url": ""
        }
    ],
    "categories": [
        "welcome",
        "tutorial",
        "startup",
        "test",
        "alpha",
        "api"
    ],
    "dates": {
        "created": "2024-02-25T18:00:00Z",
        "runStart": "2024-02-25T18:00:00Z",
        "runEnd": ""
    },
    "description": "This is the burgeoning tutorial for the MyLife Alpha Program, a test of the API for experiences.",
    "developers": [
        "mylife|2f5e98b7-4065-4378-8e34-1a9a41c42ab9",
        "system-one|4e6e2f26-174b-43e4-851f-7cf9cdf056df"
    ],
    "files": [],
    "goal": "That members feel welcomed in an intriguing and engaging way to the MyLife Alpha Program, and understand how to interact with the system in order to complete their first mission.",
    "id": "88043968-d7ef-4a57-a923-335bc9f92792",
    "mbr_id": "mylife|2f5e98b7-4065-4378-8e34-1a9a41c42ab9",
    "name": "Welcome to MyLife Alpha Program Tutorial",
    "public": true,
    "purpose": "Erik's first welcome test of the API for experiences.",
    "scenes": [
        {
            "backdrop": "full",
            "description": "MyLife's Welcome to MyLife!",
            "events": [
                {
                    "action": "dialog",
                    "character": {
                        "animation": "slide-right",
                        "animationDelay": 0,
                        "animationDuration": 2,
                        "characterId": "88043968-d7ef-4a57-a923-335bc9f92793",
                        "prompt": "hit actor with spotlight, dim slowly but bring up the house lights",
                        "sfx": [
                            "laugh",
                            "jiggle"
                        ],
                        "stageDirection": "appear",
                        "type": "script"
                    },
                    "dialog": {
                        "dialog": "Welcome!\nThank you for being a part of MyLife's Alpha Program!",
                        "effect": "typewrite",
                        "text": "note: either missing dialog or missing prompt will revert to `text` with script `type`",
                        "type": "script"
                    },
                    "id": "88043968-d7ef-4a57-a923-335bc9f92794",
                    "order": 1
                },
                {
                    "action": "dialog",
                    "character": {
                        "characterId": "88043968-d7ef-4a57-a923-335bc9f92793",
                        "type": "script"
                    },
                    "dialog": {
                        "dialog": "Welcome, @@memberFirstName, to MyLife Alpha. I am fallback dialog, to bypass LLM",
                        "effect": "typewrite",
                        "example": "",
                        "maxIterations": 1,
                        "prompt": "welcome me, @@memberFirstName -- the esteemed guest of honor -- to MyLife's Alpha Program as if MyLife were a gala, a banquet, ball and salon of performances held at the \"Mansion of Imagination\" where all my friends and family, even ancestors and famous people living and deceased were in attendance all the time",
                        "text": "note: either missing dialog or missing prompt will revert to `text` with script `type`",
                        "type": "prompt",
                        "variables": [
                            "memberFirstName"
                        ],
                        "$comment": ""
                    },
                    "id": "88043968-d7ef-4a57-a923-335bc9f92704",
                    "order": 2,
                    "variables": [
                        "memberFirstName"
                    ]
                },
                {
                    "action": "input",
                    "character": {
                        "characterId": "88043968-d7ef-4a57-a923-335bc9f92793",
                        "type": "script"
                    },
                    "dialog": {
                        "dialog": "Here in the foyer, I would love to introduce you to someone from history or literature you admire... Do take an hor d'oeuvre from the tray, and <em>let me know who you'd like to meet</em>!",
                        "type": "script"
                    },
                    "id": "16b2c1d9-116d-4f98-947c-f917d8f543d1",
                    "input": {
                        "condition": "RESPONSE contains reference to a known famous PERSON from history or fictional character",
                        "failure": "",
                        "followup": "Alas, my skills are only as vast as my limitations. This individual is not known to me. Please try again with a different name or character, perhaps more digitally pronounced or further back in history. Thank you for your understanding and patience, as my systems are always improving!",
                        "inputId": "16b2c1d9-116d-4f98-947c-f917d8f543d1",
                        "inputPlaceholder": "Socrates? Mother Teresa? Marilyn Monroe? Gandalf? ...?",
                        "inputShadow": "Who is a famous person or character you'd like to meet?",
                        "inputType": "text",
                        "maxIterations": 3,
                        "minIterations": 1,
                        "outcome": "{\n\"guide\": string of PERSON corrected full name,\n\"fictional\": bool,\n\"trait\": string primary trait PERSON known for (artist, charity, politics, personality, sports, science, other)\n}",
                        "success": true,
                        "success_complex": {
                            "fictional": "event guid",
                            "trait": {
                                "artist": "event guid",
                                "charity": "event guid",
                                "other": "event guid",
                                "personality": "event guid",
                                "politics": "event guid",
                                "science": "event guid",
                                "sports": "event guid",
                                "unknown": "event guid"
                            }
                        },
                        "variable": "guide",
                        "variables": [
                            "fictional",
                            "guide",
                            "trait"
                        ],
                        "$comment": "notes:\n- success: can be anything from omitted/boolean true or empty string, which is default that moves to next event; if it is guid, it identifies event to skip to on-success, or an object with keys for keys and sub-keys for values and each value a guid that points to a specific scene\n- failure will currently always trigger the event to replay\n- inputId = event_id\n- although `variable` can be any type, we can currently only identify one variable; additionally, unclear who, if any, will run that validation (in other words, does script have correct schema validation)\n- `minIterations` not currently used, but expresses concept\n- multiple prompts for iterations?\n- unclear on how to exactly manage variables for members (should be up-front for me as I know system); need some memory allocated, or a class created, to manage\n- perhaps failure could have another data package or point to a future end event, or just type end... unclear of right scale for now; Note: actor is the member, as proxied by **_my_** AI."
                    },
                    "order": 4,
                    "type": "script",
                    "variables": [
                        "fictional",
                        "guide",
                        "trait"
                    ]
                },
                {
                    "action": "dialog",
                    "character": {
                        "animation": "slide-left",
                        "animationDuration": 2,
                        "characterId": "4dd179a3-bf96-4716-b631-9c21071a34df",
                        "name": "MyLife Professional Actor",
                        "role": "@@guide",
                        "variables": [
                            "guide"
                        ]
                    },
                    "dialog": {
                        "dialog": "I am @@guide, and I have successfully bypassed the LLM with @@trait!",
                        "effect": "typewrite",
                        "prompt": "Assume the persona of @@guide, and greet @@memberFirstName with a short personal introduction, followed by your relationship with @@trait",
                        "type": "prompt",
                        "variables": [
                            "guide",
                            "memberFirstName",
                            "trait"
                        ]
                    },
                    "id": "66043968-d7ef-4a57-a923-335bc9f92786",
                    "order": 5,
                    "type": "prompt",
                    "variables": [
                        "guide",
                        "memberFirstName",
                        "trait"
                    ],
                    "$comment": "for now, just toggling between type=script and type=dynamic which will point to a different `.data` property; script=dialog, dynamic=prompt"
                }
            ],
            "hooks": [],
            "id": "88043968-d7ef-4a57-a923-335bc9f92790",
            "order": 1,
            "title": "Welcome",
            "type": "start"
        }
    ],
    "scriptAdvisorBotId": "asst_NonLpXQ5maLpIciwxwGqsMwV",
    "status": "active",
    "skippable": true,
    "showPlaybill": true,
    "title": "MyLife Alpha Program Welcome Tutorial",
    "variables": [
        "birthdate",
        "interests",
        "memberFirstName",
        "name",
        "nickname",
        "occupation"
    ],
    "version": 1,
    "$comment": "Truly an exceptional experience to work on this... I am now testing the variables section where I can boil logic down more effectively! Essentially a way to derive dependencies using ai rather than writing all the snot!, not sure if requires its own gpt endpoint, but cool!"
}
```

### Integration with AI

Members can interact with AI agents to generate these JSON scripts. The AI will understand the member's inputs and goals, constructing an `Experience` that aligns with their narrative. This process involves natural language processing (NLP) and context-aware responses to ensure that the `Experience` is both coherent and personalized.

## System Cast Members

### Q

Q is the enlightened "embodiment" of the MyLife Organization and serves as the core avatar for the MyLife platform. When referencing information about MyLife, Q is the go-to cast member.

- Responds to `type: 'Q'` in `.cast`

### MyLife Improvisational Actor

This actor is designed to present dialog in various situational contexts and constraints, distinct from Q. It acts as a versatile narrator or dynamic cast member suitable for the script's needs.

- Responds to `type: 'system'` in `.cast`

### Member Avatar Bot

Also functioning as `moderator`, the member's primary avatar can play a role in the script on behalf of the member. Currently it is only an echo role, but as the system matures, there will be more incorporation and role for the member's primary avatar.

- Responds to `type` in the following enum: `['avatar', 'personal-avatar', 'member-ai', 'member-bot']`

### MyLife Script Advisor

At the root of the script, identify which script advisor you would like to use. This would give some extensibility to managing your own front-ends and cleaner decision logic. The instructionset for the scriptAdvisor will be transparently offered, we just haven't currently ascertained the right avenue to expose. Currently contact @Mookse on GitHub. As you can also see, one must build their script advisor as an OpenAI GPT currently, but once we have bots that can manage scripts, this will convert to a `uuid`.

- scriptAdvisorBotId: `asst_NonLpXQ5maLpIciwxwGqsMwV`

## Member Cast Members

In future implementations, members will have the capability to expose multiple images of themselves (e.g., professional versus familial personae) to the public as per their consent. A roster mechanic will incorporate willing entities, ensuring that every member's public avatar has an opportunity to participate.

### Coding Notes

- **JSON Object Construction**: `Experiences` are defined as JSON objects, making them easy to serialize, transmit, and modify.
- **AI Assistance**: GPT models can assist in constructing these JSON scripts by interpreting natural language inputs from members and generating appropriate JSON structures.
- **Server Integration**: Once an `Experience` is constructed, it can be sent to the server for testing and validation. Ensure that the server has endpoints to handle JSON `Experience` objects for various operations (e.g., creation, update, retrieval).
- **Dynamic Content**: Scripts should be flexible to accommodate dynamic content, allowing for real-time updates and adjustments based on member interactions and feedback.

## Getting Started

1. **Clone the Repository**: Start by cloning the MyLife repository from GitHub.

   ```bash
   git clone https://github.com/MyLife-Services/mylife-maht
   ```

2. **Explore the Code**: Familiarize yourself with the existing codebase and documentation.
3. **Create an Experience**: Use the provided templates and examples to create your own `Experience` JSON scripts.
4. **Test and Validate**: Send your JSON scripts to the server for testing and validation. Make use of the API endpoints to ensure your `Experiences` function as intended.
5. **Contribute**: Submit your contributions via pull requests. Follow the contribution guidelines outlined in the repository.

For more information and to review the code, visit the [MyLife GitHub repository](https://github.com/MyLife-Services/mylife-maht).

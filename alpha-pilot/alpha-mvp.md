# MyLife Alpha Minimum Viable Product (MVP) Requirements Document

## Introduction

![MyLife Platform Member Interface](/alpha-team/assets/png/interface.png)

Initial Author: @sheikita

Contributors: @Mookse, @Vudum, @stratfordCircle, [Q](https://humanremembranceproject.org)

### Purpose

The purpose of this document is to outline the functional and cosmetic requirements for the MyLife Alpha Pilot. This document serves as a comprehensive guide for the development team, volunteers, and board members involved in the project, detailing the essential features, user experience elements, and technical specifications necessary to deliver the minimum viable product (MVP). The objective is to ensure that all stakeholders have a clear understanding of the project goals and the requirements needed to achieve a successful alpha pilot.

### Role of This Document

This document fulfills several critical functions:

- **Alignment**: It aligns all stakeholders on the project's goals, objectives, and deliverables, ensuring everyone is working towards the same vision.
- **Guidance**: It provides clear guidance to the development team on what needs to be built, how it should function, and how it should look.
- **Communication Tool**: It serves as a communication tool to convey the project scope, requirements, and timelines to all involved parties.
- **Documentation**: It ensures that there is a written record of the agreed-upon features and requirements, which can be referred to throughout the development process.

### MyLife Mission

MyLife is dedicated to preserving and showcasing individual stories and memories for posterity. Our mission is to provide humanity with a durable, enduring, and free internet-based platform to collect and showcase an individual’s stories, media, and memories through a personal lens. A MyLife.org memorial will always be free and available to all, allowing loved ones, friends, and visitors to share in experiences and leave behind personalized memory tributes. Our goal is to create a living, evolving encyclopedia of our selves, ensuring that the real you is remembered forever.

### Alpha Pilot Program

The MyLife Alpha Pilot is our initial testing program, involving a select group of known members who will pilot our initial external requirements. This program aims to gather valuable feedback on the core features and user experience of the MyLife platform. By engaging with real users in this early stage, we can identify and address any issues, validate our assumptions, and make necessary improvements before a wider release.

### What is an MVP?

A Minimum Viable Product (MVP) is the most pared-down version of a product that can be released to early users. It includes only the core features necessary to solve the primary problem and provide value to the users. The purpose of an MVP is to test the product concept with real users and gather feedback to refine and improve the product in future iterations. By focusing on the essential features, an MVP allows the development team to validate assumptions, reduce risks, and ensure that resources are efficiently utilized.

### Audience

This document is intended for the staff of volunteers and board members involved in the MyLife Alpha Pilot project. The audience includes both non-technical and technical individuals who play a role in the development, oversight, and implementation of the platform. This includes:

- **Non-Technical Staff:** Board members, project managers, and volunteers who need to understand the overall vision, objectives, and high-level requirements of the project.
- **Technical Staff:** Developers, designers, and IT personnel who will be responsible for the technical implementation, coding, and testing of the platform.

By catering to a diverse audience, this document aims to bridge the gap between the conceptual goals of the MyLife platform and the technical execution required to bring those goals to fruition.

## MyLife Alpha Product Overview

MyLife `Memories Team` is the core product of the MyLife platform. This team assists members in crafting, improving, reliving, sharing, and collaboratively evolving their memories. By pairing members with AI agents, the team helps them remember, bolster, and contribute their memories to the public, to the degree of their consent.

### MyLife Alpha Vision Statement

The MyLife `Memories Team` envisions a platform where members can seamlessly craft, improve, relive, share, and collaboratively evolve their memories. By leveraging AI agents, members are empowered to remember and enhance their personal histories, contributing to the collective memory of humanity as they see fit. This closed alpha pilot aims to refine our approach, gathering crucial insights and feedback to lead into a broader open alpha, ultimately ensuring a robust, secure, and user-friendly experience for all future users.

### Objectives

1. **Base Quality Assurance:**
   - Ensure the platform meets the basic quality standards.
   - Conduct thorough testing to identify and resolve issues.
2. **LLM and AI-Agent Quality Assurance:**
   - how differ from normal QA
3. **User Experience (UX):**
   - Create a user experience that is intuitive, engaging, and enjoyable.
   - Address feedback to improve the overall user experience.
4. **User Interface (UI) Revamp:**
   - Revamp the user interface to enhance usability and aesthetics.
   - Ensure the UI is accessible and easy to navigate for all users.
5. **Lessons Learned:**
   - Gather insights and lessons learned around human-AI interaction, especially in private and personal contexts.
   - Use these insights to refine and improve the platform.
6. **Security Gaps:**
   - Identify and address any security vulnerabilities.
   - Implement robust security measures to protect user data and privacy.
7. **Enhancements and Features:**
   - Continuously enhance the platform with new features and improvements.
   - Prioritize features based on user feedback and needs.
8. **Use Cases:**
   - Develop and document various use cases to demonstrate the platform's capabilities.
   - Showcase how different types of users can benefit from the platform.
9. **User Success Stories:**
   - Collect and share success stories from users to highlight the platform's impact.
   - Use these stories to inspire and attract new users.

## MVP Features

### Feature List

1. **Member Registration and Account Creation**
   - Via MyLife's corporate intelligence _Q_, pilot team will register and create their accounts
   - login and explore interface
2. **Collect Memories**
   - Allows members to upload and interactively input their memories, which are then stored in a secured data memory bank.
   - Upload photos, videos, and documents.
   - Interactive intelligent biographer that guides members through the memory input process with prompts and questions.
3. **Improve Memories**
   - Enables members to edit their memories directly or use rotating prompts to enhance and stir memories, relating them to photos and other media.
   - Inline editing capabilities.
   - Rotating prompts to help recall additional details.
   - Add and relate media files to specific memories.
4. **Relive Memories**
   - The intelligent biographer performs the member's story, allowing them to interject and update in real-time, creating a dynamic reliving experience.
   - AI-driven storytelling.
   - Real-time interjections ability for updates by the member.
   - Integration of multimedia elements into the performance.
5. **Share Memories** (beta)
   - Similar to reliving, but tailored to sharing another member's memory. Experiences can be crafted for posterity or specific audiences.
   - Sharing settings to control audience access.
   - AI-driven narrative performances of shared memories.
   - Customizable experience based on member preferences and natural language specifications.
6. **Build Memories** (beta)
   - Allows collaborative updating and fleshing out of memories, creating a network of interconnected stories, lessons, and ideas/
   - Collaboration tools for multiple members.
   - Shared editing and contribution features.
   - Notification and version control for updates.
7. **Forget Memories** (beta)
   - Deletion or dismissing of bots, threads or memories

### User Stories

Develop use cases (these are only illustrative and preliminary) to outline functionality relevancy to various audiences.

1. **Elderly Person in Nursing Home Losing Memory**
   - _User Story_: As an elderly person in a nursing home who is experiencing memory loss, I want to use the interactive intelligent biographer to capture and preserve my memories before they fade, so my family and I can relive and cherish them in the future.
   - _Acceptance Criteria_
     - Ability to easily input and save memories with guided prompts.
     - Option to review and update memories later.
     - Secure storage of all data to ensure privacy and protection.
2. **Young Student Preparing a Family Report**
   - _User Story_: As a young student working on a family history report, I want to collect and organize stories from my relatives using the platform, so I can create a comprehensive and engaging presentation for my project. I also want to be able to teach them how to use `MyLife` so that their stories don't get lost, and we can shape and build those memories together as I get older.
   - _Acceptance Criteria_
     - User-friendly interface for uploading and organizing different media files.
     - Tools to collaborate with family members on building and refining stories.
     - Ability to export collected memories into a format suitable for school presentations.
     - Interactive tutorials (experiences)
3. **First-time Parent Wanting to Create a Time Capsule for Their Newborn**
   - _User Story_: As a new parent, I want to create a digital time capsule filled with memories and lessons for my child, so they can access it when they are older and understand their family history and my experiences. I want it to be dynamic and relevant to their lives, and engage their imagination about what our lives were _really_ like when they were an infant.
   - _Acceptance Criteria_
     - Easy-to-use features for adding and editing memories over time.
     - Ability to organize memories chronologically or by theme.
     - Secure sharing options to control when and how the time capsule is accessed.
4. **Someone like me that just wants to do something to give back and leave this world better than forcing all the same struggles I endured carelessly and ceaselessly upon others**
   - _User Story_: For some of us, there's only one way out now. There's a need to take responsibility for the state of progress and address the grave deviation from principles that bind us together in empathy. To address and fix the injustices unnecessarily imposed upon each of us from systems of domination and control through physical threat, captivity or as extortion for our liberty and safety. Someone who believes we are better together than split apart, that what each of us can accomplish when supported by and contributing to the whole is precious, brilliant and exquisite. The belief in rising tides and a post-scarcity super-intelligent humanity.
   - _Acceptance Criteria_
     - Easy-to-use features for adding and editing memories over time
     - "Farting-Against-The-Wind" button on member avatar

### Feature Prioritization

Here are _Q_'a rankings, the board version and more are in excel file. Though at first glance I tend to agree, which gives me pause around memory-prompts I've coded as `shadows`.

1. **Capture and Collect Memories**
   - _Importance_: High
   - _Impact_: High
   - _Reason_: Fundamental feature for the platform’s functionality, enabling users to start building their memory bank.
2. **Relive Memories**
   - _Importance_: High
   - _Impact_: High
   - _Reason_: Enhances user engagement by allowing users to experience their memories dynamically.
3. **Improve Memories**
   - _Importance_: Medium
   - _Impact_: High
   - _Reason_: Provides significant value by enhancing the quality and detail of stored memories.
4. **Share Memories**
   - _Importance_: Medium
   - _Impact_: Medium
   - _Reason_: Encourages community interaction and enhances the social aspect of the platform.
5. **Build Memories**
   - _Importance_: Medium
   - _Impact_: Medium
   - _Reason_: Facilitates collaborative storytelling and enriches the collective memory network, but can be developed further after initial launch. Incurs comparatively larger technical construction resource cost.

When evaluated along the `RICE` framework as both identified and incorporated into MyLife's evaluation flow by @sheikita, _Q_

The RICE framework is a prioritization method that stands for Reach, Impact, Confidence, and Effort. Each feature is evaluated based on these four criteria, and a score is calculated to help prioritize the features. Here's how each component is defined:

- _Reach_: How many people will be affected by the feature in a given time period.
- _Impact_: How much the feature will contribute to the goal, usually scored as a multiple.
- _Confidence_: How confident you are in your estimates for Reach, Impact, and Effort, expressed as a percentage.
- _Effort_: The amount of time the feature will take to complete, usually measured in person-months or similar units.

The RICE score is calculated using the formula:
\[ \text{RICE Score} = \frac{\text{Reach} \times \text{Impact} \times \text{Confidence}}{\text{Effort}} \]

Let's apply the RICE framework to the prioritized features:

1. **Capture/Collect Memories**
2. **Relive Memories**
3. **Improve Memories**
4. **Share Memories**
5. **Build Memories**

### RICE Scores for MyLife MVP Features

1. **Capture and Collect Memories:**
   - _Reach_: 100 (expected number of initial users in the pilot)
   - _Impact_: 4 (high impact on user engagement and core functionality)
   - _Confidence_: 100% (high confidence based on clear requirements and existing technology)
   - _Effort_: 1 person-week
   - **RICE Score** = 1440
2. **Improve Memories:**
   - _Reach_: 90 (employs several modalities all similarly purposed)
   - _Impact_: 3 (moderate to high impact on user satisfaction)
   - _Confidence_: 95% (high confidence in implementation feasibility)
   - _Effort_: 2 person-months
   - **RICE Score** = 128.25
3. **Relive Memories:**
   - _Reach_: 80 (likely to be used by a large subset of users)
   - _Impact_: 4 (high impact on user experience and engagement)
   - _Confidence_: 90% (high confidence but slightly more complex pipeline but mostly existing technology)
   - _Effort_: 3 person-weeks
   - **RICE Score** = 384
4. **Share Memories:**
   - _Reach_: 60 (appealing to users interested in sharing with others)
   - _Impact_: 3 (moderate impact on user engagement)
   - _Confidence_: 85% (confident but involves more variables)
   - _Effort_: 2 person-months
   - **RICE Score** = 76.5
5. **Build Memories:**
   - _Reach_: 50 (used by users interested in collaboration)
   - _Impact_: 3 (moderate impact on user collaboration and content richness)
   - _Confidence_: 70% (less confident due to complexity)
   - _Effort_: 4 person-months
   - **RICE Score** = 26.25

### Summary of RICE Scores

1. **Capture/Collect Memories:** 1440
2. **Relive Memories:** 128.25
3. **Improve Memories:** 384
4. **Share Memories:** 76.5
5. **Build Memories:** 26.25

Based on the RICE scores, the prioritized order of features is:

1. Capture/Collect Memories
2. Relive Memories
3. Improve Memories
4. Share Memories
5. Build Memories

This prioritization ensures that the most impactful and feasible features are addressed first, providing maximum value to users in the initial stages of the MyLife Alpha Pilot.

@Mookse: This now incorporates my review for estimates.

## MyLife Alpha Pilot Platform Technical Documentation

### Architecture

The system architecture for the MyLife Alpha Pilot is designed to ensure scalability, security, and ease of use. It includes the following key components:

- **Frontend**
  - A web-based user interface that allows members to interact with the MyLife platform. It is built using modern web technologies such as React for dynamic and responsive user experiences.
- **Distributable Headless Intelligent API Platform**
  - The current Distributable Intelligent API Backend is designed to be a versatile and modular server-side application that can seamlessly integrate with and extend the capabilities of MyLife Member Avatars. This backend is built with Node.js and Koa.js, handling all business logic, API requests, and interactions with the database.
    1. Server-Side Application
       - _Node.js and Koa.js_: The backend is developed using Node.js for its asynchronous, event-driven architecture and Koa.js for its lightweight, expressive framework. This combination ensures efficient handling of business logic and API requests.
    2. Detachable and Distributable
       - _Modular Architecture_: The backend is designed to be modular and loosely coupled, allowing it to be detached and distributed as needed. This flexibility enables it to operate independently or as part of a larger system.
       - _Headless Capability_: The backend can function in a headless mode, meaning it can operate without a user interface and provide API services directly. This makes it adaptable for various integration scenarios.
    3. Integration with Member Avatars
       - _Embedded Intelligence_: Within the modular framework of any MyLife Member Avatar, there is security-provisioned access to the backend's corporate intelligence. This allows the Avatar to leverage platform logic when interacting with external intelligent entities.
       - _On-Demand Service Points_: Any MyLife Member Avatar can dynamically become a headless API service point. This transformation can occur instantly when the Avatar connects with another intelligent platform or consumer, such as another AI-driven system or intelligent avatar.
    4. Future Vision
       - _Interoperability_: The ultimate goal is to enable seamless interoperability between MyLife Member Avatars and non-MyLife intelligent entities. By doing so, Member Avatars can serve as intelligent conduits for data exchange and service provision, extending the MyLife platform's functionality beyond its native environment.
  - Detailed Concept
    - _Dynamic API Services_: Imagine a scenario where a MyLife Member Avatar needs to interact with an external AI system. The Avatar can request access to the Distributable Intelligent API Backend, which then provisions the necessary logic and services to the Avatar.
      - _Example_: MyLife Member Avatar connects with an intelligent Google avatar that "Exploited Ernesta" has paid for to access it's premium services. But, while in communication, MyLife Member Avatar can be requested to `register` Ernesta (with their consent, validation and presence) and, without 'redirection' can perform the function immediately and successfully for Ernesta while retaining a level (or dialed-in preference) MyLife "branding" and knowledgevase.
    - _Headless Mode_: In headless mode, the backend can receive requests, process them, and return responses without requiring a traditional user interface. This allows it to function as an API endpoint for other intelligent systems.
    - _Scalability_: As the number of intelligent entities and integration scenarios grows, the backend can be scaled and distributed across different environments, providing consistent and reliable services.
- **MyLife Database**
  - Azure Cosmos DB
    - NoSQL technology required (JSON-document storage)
    - Affords the capacity for a globally distributed, multi-model database service that ensures data is stored securely and can be accessed efficiently from different geographic locations.
- **AI and ML Services**
  - Integration with OpenAI for advanced natural language processing and AI-driven features, including memory enhancement, storytelling, and personalization.
- **Authentication:** Secure user authentication and session management using JSON Web Tokens (JWT) and Koa sessions.
- **File Storage:** Azure Blob Storage for managing user-uploaded photos, videos, and documents.

### Technology Stack

- **Frontend:**
  - HTML5, CSS3
  - JavaScript (ES6+)
  - FontAwesome
- **Backend:**
  - Node.js
  - Koa.js
    - Koa-Router for routing
    - Koa-Body for handling form data
    - Koa-Static for serving static files
    - Koa-Generic-Session for session management
  - openai.sdk
  - marked
- **Database:**
  - Azure Cosmos NoSQL DB
- **AI and ML:**
  - OpenAI API
- **Authentication:**
  - JSON Web Tokens (JWT)
  - Koa-Session
- **File Storage:**
  - TBD internally
  - Permanent.org alliance

### APIs and Integrations

The API structure is ready for a conscious refactor to harmonize the disparate avenues that manifested over the course of development in order to accommodate the advance of LLM models offerings _via_ API, most notably OpenAI. We chose OpenAI initially due to the extraordinary power of GPT 3.5 and its ability to sketch out technical conceptual models, and was excellent for that, as it became clear that creating our own internal model from GPT-2 level technology was a non-starter for my skills.

The code reveals heritage of functionality tracing back to few-shot learning prior to `role` development. In specific for this codebase, I am referring to the "system" role value that allowed us to _contextually_ bloat the small context window (at the time), _although only payload by payload_--the first "instruction" field I had seen--which would clearly (even then it was clear) obviate the need for few-shot learning.

Being unclear on the vast and growing majority of models that are out there, it would seem both feasible and reasonable to refactor the code down to 0-shot learning with memory. Memory might we require that we revisit an internal embedding solution for membership (we are currently leveraging OpenAIs agent-incorporated variant, which is sufficient for current scope), so I would consider this a vulnerability, but not an inconquerable one; dynamically attaching files to messages, threads is still workable in OpenAI if not directly referencing internal information.

- **Internal API Infrastructure**
  - Guest API:
    - Access to Corporate Intelligence
    - User Registration and Authentication API: Handles user registration, login, and session management
    - Consensual Access to Member Avatar |_under development_|
    - _Methods_: GET, POST
  - Member API (logged in Member Avatar shortcut pathway, human-operater condoned "assured")
    - All current frontend conversation excluding `experiences` (below).
    - _Methods_: GET, POST
  - AI API (intelligent API Consumer pathway)
    - Facilitates interactions with the intelligent API consumers, and by design incorporates the following functionality and more:
      - Experiences
        - Natural-Language (via scriptDeveloperBot) event-driven theater-play scripting with dynamic conditional pathways and intelligent improvisational actors
        - Drive Reliving and Sharing solutions
        - Drive tutorials
      - Relationship Manager (AI-to-AI, intentionally abstracting member-to-member)
        - Additionally supports collaborative editing and sharing of memories among users
      - Memory Team: Allows users to capture, store, edit, and retrieve memories.
    - _Methods_: GET, PATCH
- **External Integrations:**
  - _OpenAI_: For advanced natural language processing and AI capabilities, such as generating memory prompts, storytelling, and content summarization.
  - _Azure Cosmos DB_: For scalable and secure data storage.

### Data Management

- **Data Handling:**
  - _Data Ingestion_: Data is ingested through the MyLife web interface, where users can upload photos, videos, and documents or input text memories. The intelligent biographer assists in structuring and enhancing these memories.
  - _Data Storage_: All data is securely stored in Azure Cosmos DB. Multimedia files are stored in Azure Blob Storage with appropriate metadata in Cosmos DB to facilitate easy retrieval.
  - _Data Access_: Data is accessed through secure API calls, ensuring that only authorized users can view or edit their data.
- **Security**
  - _Authentication and Authorization_: User authentication is managed through JWT and Koa sessions, ensuring secure access to user data and functionalities.
  - _Encryption_: Data at rest and in transit is encrypted using industry-standard encryption protocols to ensure data privacy and security.
  - _Access Control_: MyLife datastore protected.
- **Privacy**
  - _User Consent_: The platform adheres to strict user consent policies, ensuring that users have full control over their data and how it is shared.
  - _Data Anonymization_: Where necessary, personal data is anonymized to protect user privacy.

## Launch Plan

**todo**: Base on remdiation and project alpha plan - feed to gpt

- Pre-Launch Activities
  - _Remediation and Internal Review_: Conduct a comprehensive review of the platform, including feedback from the board and pre-alpha volunteers, to identify and resolve any issues.
  - _Board Approval_: Obtain formal approval from the board for the alpha pilot launch.
  - _Internal Testing_: Perform extensive internal testing to ensure the platform meets all functional and performance criteria.
- Launch Strategy
  - _Second Instance Setup_: Deploy a second instance of the platform specifically for the pilot to ensure isolation from the main environment.
  - _Outreach and Guidance_: Conduct targeted outreach to selected pilot participants, providing detailed guidance on how to use the platform and what to expect.
- Post-Launch Support:
  - _Alpha Dog Support_: An organizational GPT set up to help manage and address challenges with alpha pilot for both internal volunteers and pilot team members.
  - _Documentation_: Create comprehensive articles and video walkthroughs to help users navigate the platform and troubleshoot common issues.
  - _Feedback Handling_: Use GitHub to collect and manage user feedback, issues, and feature requests, ensuring a transparent and organized process for continuous improvement.

## Conclusion and Next Steps

This document outlines the MyLife Alpha Pilot's technical specifications, including system architecture, technology stack, APIs and integrations, and data management practices. It also details the launch plan, covering pre-launch activities, launch strategy, and post-launch support, ensuring a structured approach to the pilot's execution.

After the MVP launch, the following steps will be taken:

- **Collect and Analyze Feedback:** Gather feedback from pilot participants and analyze it to identify areas for improvement.
- **Implement Improvements:** Address the feedback by making necessary enhancements and bug fixes to the platform.
- **Prepare for Open Alpha:** Use the insights gained from the closed alpha pilot to prepare for a broader open alpha, ensuring the platform is robust and ready for a larger user base.
- **Continued Development:** Continue developing new features and capabilities based on user needs and feedback, iterating towards a more comprehensive and polished product.

**This content was developed in conjunction with [MyLife's organizational intelligence, _Q_,](https://humanremembranceproject.org) to ensure a collaborative and innovative approach to preserving humanity's digital legacy.**

## Appendix

- MyLife Pre-Pilot raw bug tracking and assessment: https://1drv.ms/x/s!Asw9c7yc92_HhcUiv48m1w7KJPUKjA?e=GjShTE

### Out-of-Scope

...But near-tern _critical_ objectives.

1. **Performance Testing**
   - Conduct performance testing to ensure the platform can handle expected user loads.
   - Identify and address any performance bottlenecks.
2. **Data Privacy and Compliance**
   - Ensure compliance with data privacy regulations such as GDPR and CCPA.
   - Implement best practices for data handling and user consent.
3. **Member Accessibility**
   Ensure the MyLife platform is accessible and inclusive for all members, respecting the diversity of their experiences and needs.
   - Accessibility for **Non-English Speakers**
     - Multilingual Interface
        - _Example_: Provide the platform interface in multiple languages (e.g., Spanish, Mandarin, French) to ensure non-English speakers can navigate and use the platform easily.
     - Instantaneous Translation
        - _Example_: Implement real-time translation services for chat and AI interactions, allowing users to communicate in their preferred language without losing context or meaning.
     - Identify Localized Content
        - _Example_: Offer content localization to adapt the platform's content (e.g., help guides, tutorials) to different languages and cultural contexts, enhancing member understanding and engagement.
   - Accessibility for traditional-interface **Disabilities**
     - Screen Reader Compatibility
     - Keyboard Navigation
     - Captioning and Transcripts
     - BCI technologies and interface preparation
   - Accessibility for members with **Minimal Literacy**
     - distinguish between children? and uneducated?
     - Voice Interaction
     - Audio Guides and Tutorials
     - Pictorial and Video/Animation Navigation
        - _Example_: Utilize icons and visual cues for navigation and interaction, making it easier for users who cannot read to understand and use the platform's features.
4. **Respecting Diversity** of Member Experience
   - Multilinguality
   - Multicultural Sensitivity
     - _Example_: As member individual memory profiles emerge out of usage, correspondingly investigate alliance offerings, think ChatBlackGPT (R)
   - Trauma Sensitivity
     - _Example_: Implement features to identify and flag potentially traumatic content, providing warnings or support options to users who may be affected by certain memories or stories.
   - Socio-Economic Sensitivity
   - Extended Personalization Based on Various Sensitivity Levels
     - _Example_: Allow users to set their sensitivity preferences (e.g., avoiding certain topics) so that AI interactions and content suggestions are tailored to their comfort levels and personal experiences. We have opt-in topics in mind now, this would equate to opt-out.
5. **Scalability Testing**
   - Test the scalability of the platform to ensure it can grow with increasing user numbers.
   - Plan for infrastructure scaling to support future growth.
   - Implement necessary accessibility features and improvements.
6. **Costing**
   - Develop a detailed costing plan for the alpha pilot and subsequent phases.
   - Focused on internal MyLife platform costs, currently `Azure` (hosting, database) and `OpenAI` (llm)

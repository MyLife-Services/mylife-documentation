# MyLife API Intelligent Endpoints

- [API Endpoints](#api-endpoints)
- [Authentication Endpoints](#authentication-endpoints)
- [Member Endpoints](#member-endpoints)
- [Page Endpoints](#page-endpoints)

## API Endpoints

Here is the description of all MyLife API intelligent endpoints accessible to independent intelligent systems or burgeoning clients.

- [API GET Endpoints](#api-get-endpoints)
- [API HEAD Endpoints](#api-head-endpoints)
- [API PATCH Endpoints](#api-patch-endpoints)
- [API POST Endpoints](#api-post-endpoints)

### API GET Endpoints

- **/alerts**
  - => `alerts()`
  - Retrieves all available system alerts
- **/alerts/_:aid_**
  - => `alerts(aid)`
  - Retrieves a specific alert by its ID
  - `:aid` is the alert ID
- **/experiences/_:mid_**
  - => `experiences(mid)`
  - Retrieves experiences for a member
  - `:mid` is the member ID; note: can ask to trigger autoplay
- **/experiencesLived/_:mid_**
  - => `experiencesLived(mid)`
  - Retrieves the lived experiences for a member
  - `:mid` is the member ID
- **/logout**
  - => `apiLogout()`
  - Logs out of API session

### API HEAD Endpoints

- **/keyValidation/_:mid_**
  - => `keyValidation(mid)`
  - Performs an instant validation check on the API key for the specified member
  - `:mid` is the member ID

### API PATCH Endpoints

- **/experiences/:mid/experience/_:eid_/cast**
  - => `experienceCast(mid, eid)`
  - Retrieves the cast of an experience
  - `:mid` is the member ID (for validation) and `:eid` is the experience ID.
- **/experiences/:mid/experience/_:eid_/end**
  - => `experienceEnd(mid, eid)`
  - Ends a specific experience
  - `:mid` is the member ID and `:eid` is the experience ID
- **/experiences/:mid/experience/_:eid_/manifest**
  - => `experienceManifest(mid, eid)`
  - Retrieves the manifest of a specific experience
  - `:mid` is the member ID and `:eid` is the experience ID. This can act as a proxy for both cast and navigation
- **/experiences/:mid/experience/_:eid_/navigation**
  - => `experienceNavigation(mid, eid)`
  - Retrieves the navigation for a specific experience
  - `:mid` is the member ID and `:eid` is the experience ID
- **/experiences/:mid/experience/_:eid_**
  - => `experience(mid, eid)`
  - Updates or progresses the state of a specific experience
  - `:mid` is the member ID and `:eid` is the experience ID

### API POST Endpoints

- **/challenge/:mid**
  - => `challenge(mid)`
  - Challenges the access with a passphrase
  - `:mid` is the member ID
- **/entry/:mid**
  - => `entry(mid)`
  - Submits a journal entry for the member
  - `:mid` is the member ID
- **/keyValidation/:mid**
  - => `keyValidation(mid)`
  - Validates the API key for a specific member
  - `:mid` is the member ID
- **/memory/:mid**
  - => `memory(mid)`
  - Creates or manages a memory entry for the member
  - `:mid` is the member ID
- **/obscure/:iid**
  - => `obscure(iid)`
  - Obscures a specific item
  - `:iid` is the item ID
- **/register**
  - => `register()`
  - Registers a new member via API (outward-extension functionality)
- **/upload/:mid**
  - => `upload(mid)`
  - Handles a file upload for a specific member
  - `:mid` is the member ID

## Authentication Endpoints

- [Authentication GET Endpoints](#authentication-get-endpoints)
- [Authentication POST Endpoints](#authentication-post-endpoints)

### Authentication GET Endpoints

- **/select**
  - => `loginSelect()`
  - List hosted members available for login
- **/status**
  - Whether or not session is logged in
- **/logout**
  - => `logout()`
  - Log out a member

### Authentication POST Endpoints

- **/challenge/_:mid_**
  - =>`challenge()`
  - Validates member's passphrease
  - Challenge path requires passphrase (string) as `ctx.body`
  - `:mid` is the member ID
- **/signup**
  - => `signup()`
  - Signup a new member

## Member Endpoints

- [Member DELETE Endpoints](#member-delete-endpoints)
- [Member GET Endpoints](#member-get-endpoints)
- [Member PATCH Endpoints](#member-patch-endpoints)
- [Member POST Endpoints](#member-post-endpoints)
- [Member PUT Endpoints](#member-put-endpoints)

### Member DELETE Endpoints

- **/items/_:iid_**
  - =>`deleteItem(iid)`  
  - Deletes a specific item
  - `:iid` is the item ID

### Member GET Endpoints

- **/**
  - => `members()`
  - Retrieves information for the member's home
- **/bots**
  - => `bots()`
  - Retrieves all bots
- **/bots/_:bid_**
  - => `bots(bid)`
  - Retrieves a specific bot by its ID
  - `:bid` is the bot ID
- **/collections**
  - => `collections()`
  - Retrieves all collections associated with the member
- **/collections/_:type_**
  - => `collections(type)`
  - Retrieves a specific type of collection
  - `:type` represents the collection type (e.g., files, stories)
- **/experiences**
  - => `experiences()`
  - Retrieves all experiences
- **/experiencesLived**
  - => `experiencesLived()`
  - Retrieves the lived experiences
- **/greeting**
  - => `greetings()`
  - Retrieves greeting message
- **/item/_:iid_**
  - => `item(iid)`
  - Retrieves a specific item
  - `:iid` is the item ID
- **/mode**
  - => `interfaceMode()`
  - Retrieves the current interface mode
- **/teams**
  - => `teams()`
  - Retrieves available teams

### Member PATCH Endpoints

- **/experience/_:eid_**
  - =>`experience(eid)`
  - Updates an experience
  - `:eid` is the experience ID
- **/experience/_:eid_/end**
  - =>`experienceEnd(eid)`
  - Ends a specific experience
  - `:eid` is the experience ID
- **/experience/_:eid_/manifest**
  - =>`experienceManifest(eid)`
  - Retrieves the manifest of a specific experience
  - `:eid` is the experience ID
- **/memory/relive/_:iid_**
  - =>`reliveMemory(iid)`
  - Relives a specific memory
  - `:iid` is the item ID
- **/memory/end/_:iid_**
  - =>`endMemory(iid)`
  - Ends the reliving of a specific memory
  - `:iid` is the item ID

### Member POST Endpoints

- **/**
  - =>`chat()`
  - Sends a message to active bot
- **/bots** - `bots()`  
  - Creates or updates a bot
- **/bots/create**
  - =>`createBot()`
  - Creates a new bot for the member
- **/bots/activate/_:bid_**
  - =>`activateBot(bid)`
  - Activates a specific bot
  - `:bid` is the bot ID
- **/category**
  - =>`category()`
  - Sets a category for the member's avatar
- **/migrate/bot/_:bid_**
  - =>`migrateBot(bid)`
  - Migrates a bot
  - `:bid` is the bot ID
  - Returns new bot ID
- **/migrate/chat/_:tid_**
  - =>`migrateChat(tid)`
  - Migrates a chat
  - `:tid` is the chat thread ID to migrate
  - Returns new thread ID
- **/mode**
  - =>`interfaceMode()`
  - Sets the interface mode
- **/obscure/:iid**
  - =>`obscure(iid)`
  - Obscures a specific item's contents
  - `:iid` is the item ID
- **/passphrase**
  - =>`passphraseReset()`
  - Resets the member’s passphrase
- **/retire/bot/_:bid_**
  - =>`retireBot(bid)`
  - Retires a specific bot
  - `:bid` is the bot ID
- **/retire/chat/_:tid_**
  - =>`retireChat(tid)`
  - Retires a chat
  - `:tid` is the chat thread ID
- **/summarize**
  - =>`summarize()`
  - Summarizes a memory or other content entity type
- **/teams/_:tid_**
  - =>`team(tid)`  
  - Retrieves top-level team information
  - `:tid` is the team ID
- **/upload** - `upload()`  
  - Uploads file(s)

### Member PUT Endpoints

- **/bots/_:bid_**
  - =>`bots(bid)`
  - Updates a specific bot
  - `:bid` is the bot ID
- **/bots/system-update/_:bid_**
  - =>`updateBotInstructions(bid)`
  - Force updates bot instructions
  - `:bid` is the bot ID
- **/item/_:iid_**
  - =>`item(iid)`  
  - Updates fields in a specific item
  - `:iid` is the item ID

## Page Endpoints

All of these exposures require the GET method. All deliveries are in html and through the Koa pipeline with EJS flavor (can be deprecated). All include `layout.html`.

Example: `await ctx.render('about')`

- **/**
  - `index()`
  - Delivers `index.html`
- **/about**
  - `about()`
  - Delivers `about.html`
- **/members/**
  - Validates via `memberValidation()` in `routes.mjs`
  - `members()`
  - Delivers `members.html`
- **/privacy-policy**
  - `privacyPolicy()`
  - Delivers `privacy-policy.html`

## Help Endpoint

- POST **/help**

## Appendix

### Explanation of Path Variables

- **`:aid`** - Represents an **Alert ID**, used to identify a specific alert
- **`:bid`** - Represents a **Bot ID**, used to identify a specific bot that the member is interacting with
- **`:eid`** - Represents an **Experience ID**, used to identify a specific experience
- **`:iid`** - Represents an **Item ID**, used to identify a specific item (e.g., file, memory, journal entry)
- **`:mid`** - Represents a **Member ID**, used to identify a specific member
- **`:tid`** - Represents a **Thread ID**, usually for managing chat threads or teams

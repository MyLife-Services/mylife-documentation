# Internal Pilot Test Plan

- [My Gratitude](#my-note-to-you)
- [The Internal Pilot Testing Process](#pilot-testing-process)
- [Test Cases by Functionality](#functionality-test-cases)
- [Known Issues](#known-issues)
- [Appendix](#appendix)

## My Note to You

**Hi!**

Thank you so much for participating in this internal alpha for us to gather feedback on how the MyLife platform prototype is currently succeeding against our product expectations (_Minimal Viable Product_, aka _MVP_).

This is a momentous step for us, and it's all thanks to your participation and contributions, and will continue to be. Taking this time will make all the difference in our near future.

Thank you.

Erik::

## Pilot Testing Process

More supporting documents to help guide the process are on the way, but we're hoping this will be sufficient to conduct this first round of feedback gathering and incorporation.

Any insights you have for more structure to this process as we move to an external audience, please bring them to our Slack #alpha-channel which should be open for participation, or you can always direct message me.

We're trying to keep the process extremely simple, so here goes.

0. In Slack, you will be receiving (or can download) a personal copy of this document to review and keep your notes
1. **Walk through** [Test Cases](#functionality-test-cases) below, preferably in order
2. **Record** Errors, Observation, Insights
   - Both pertaining to the platform _and_ the test cases themselves
   - However you end up opening/reading the `.md` file, record your insights in that program
3. **Prioritize** fixes (only for internal pilot process)
   - Under [Known Issues](#known-issues) below, please prioritize the important you would place on each issue getting fixed
   - Add you own bug titles and their priority as well
4. **Return** your updated document to me via Slack (or if you would rather not me, then Steve)

Any questions? No? Then let's rock!

## Functionality Test Cases

Quick links to various functional testing areas:

- [Account Management](#account-management-test-cases)
- [Personalize Bots](#personalize-bots)
- [Collect Memory](#collect-memory)
- [Direct Edit Memory](#direct-edit-memory)
- [Interactive Edit Memory](#interactive-edit-memory)
- [Relive Memory](#relive-memory)
- [Delete a Memory](#delete-a-memory)
- [Play Experiences](#play-experiences)

### Account Management Test Cases

#### Test Case: Login

##### Login Preconditions

- Visitor MyLife registration successful
- Visitor is a member of MyLife
- Member has credentials to login

##### Login Test Steps

1. **Navigate** to [https://humanremembranceproject.org/](https://humanremembranceproject.org/)
2. **Click** on Login button at the top-right of interface
3. **Select** your avatar-id from the dropdown
4. Type passphrase and **hit Enter** _or_ **click** submit button

##### Login Success Conditions

- Member is logged in and routed to member dashboard
- New Member Avatar created
- New Member Memory Team created
- Directed to Member Dashboard

##### Login Result

- _enter your results or issues here_

##### Login Additional Observations

- _enter additional observations here_

---

#### Test Case: Reset Passphrase

##### Reset Passphrase Preconditions

- Member is logged into MyLife
- MyLife shows Avatar Bar at top right

##### Reset Passphrase Test Steps

1. **Click** on Avatar bar
2. **Click** on `Reset Passphrase`
3. Enter new passphrase and click on right arrow button
4. **Logout** and **Login** again with new passphrase

##### Reset Passphrase Success Conditions

- MyLife should always allow member to change passphrase
- Passphrase saved in database

##### Reset Passphrase Result

##### Reset Passphrase Additional Observations

---

#### Test Case: Logout

##### Logout Preconditions

- Member is logged into MyLife

##### Logout Test Steps

1. **Click** on Logout button on the top-right
2. **Verify** you are logged out of MyLife by:
   - **Click** on the top-right button, should read `login`
   - **Verify** you are taken to ID selection page

##### Logout Success Conditions

- Member successfully logged out

##### Logout Result

##### Logout Additional Observations

---

### Personalize Bots

#### Test Case: Avatar Name

##### Avatar Name Preconditions

- Member is logged into MyLife
- MyLife shows Avatar bar at the top-right

##### Avatar Name Test Steps

1. **Click** on Avatar bar to open it
2. Modify the name of your Avatar
3. **Blur** field (click outside of the name textbox) or **hit Enter** to submit
4. **Verify** that the name of the Avatar is changed in the bar and chat placeholders

##### Avatar Name Success Conditions

- Avatar bar should show the new name of the bot
- Placeholder should change
- Bot Greeting references should change
- MyLife database should update
- LLM should update
- Member should be able to edit the name of the bot again

##### Avatar Name Result

##### Avatar Name Additional Observations

---

#### Test Case: Biographer Name

##### Biographer Name Preconditions

- Member is logged into MyLife
- MyLife shows the Biographer bar

##### Biographer Name Test Steps

1. **Click** on Biographer bar to open it
2. Modify the name of your Biographer
3. **Blur** field (click outside of the name textbox) or **hit Enter** to submit
4. **Verify** that the name of the Biographer is changed in the bar and chat placeholders

##### Biographer Name Success Conditions

- Biographer bar should show the new name of the bot
- Placeholder should change
- Bot Greeting references should change
- MyLife database should update
- LLM should update
- Member should be able to edit the name of the bot again

##### Biographer Name Result

##### Biographer Name Additional Observations

---

#### Test Case: Biographer Options

##### Biographer Options Preconditions

- Member is logged into MyLife

##### Biographer Options Test Steps

Interests:

1. Add Options
   - **Click** on Biographer bar
   - **Select** a few options from the biographer
2. Remove Options
   - **Unselect** some options from the biographer
3. **Logout** and **Login** to verify that options were maintained

##### Biographer Options Success Conditions

- Member should always be able to select/deselect options
- Interests should be available to the conversation
- Biographer should always show the options selected by the member
- MyLife database should update.
- LLM should update.

##### Biographer Options Result

##### Biographer Options Additional Observations

---

### Collect Memory

#### Test Case: Create Memory 01

##### Create Memory 01 Preconditions

- Member is logged into MyLife

##### Create Memory 01 Test Steps

1. **Click** on the Biographer Bar circle, so that icon color changes to yellow
2. Chat window indicates, "I am a personal-biographer for member." (if not active)
3. Add a memory that contains 3-4 lines
4. Bot should indicate that it has saved your memory
5. Navigate to **Scrapbook -> Memories**
6. **Click** on the **Refresh** button
7. Verify that the memory is saved under Memories

##### Create Memory 01 Success Conditions

- Memory is available in the scrapbook
- Memory summary is saved to MyLife

##### Create Memory 01 Result

##### Create Memory 01 Additional Observations

---

#### Test Case: Create Memory 02

##### Create Memory 02 Preconditions

- Member is logged into MyLife.

##### Create Memory 02 Test Steps

1. **Click** on the Biographer Bar circle, so that icon color changes to yellow
2. Chat window indicates, "I am a personal-biographer for member."
3. **Add** a one-line memory
4. **Click** on the **Memories Refresh** button
5. **Verify** that the memory is saved under Memories

##### Create Memory 02 Success Conditions

- Memories should be saved regardless of the length of the memory.

##### Create Memory 02 Results

##### Create Memory 02 Additional Observations

---

#### Test Case: Create a Memory Using a Different Language (optional)

##### Different Language Preconditions

- Member is logged into MyLife

##### Different Language Test Steps

1. **Click** on the Biographer Bar circle, so that icon color changes to yellow
2. Chat window indicates, "I am a personal-biographer for member." (if not active)
3. **Add** a memory in a different language
4. **Click** on the **Memories Refresh** button.
5. **Verify** that the memory is saved under Memories in the original language

##### Different Language Success Conditions

- Member should be able to save the memory in a different language.

##### Different Language Results

##### Different Language Additional Observations

---

### Direct Edit Memory

#### Test Case: Activate Memory

##### Activate Memory Preconditions

- Member is logged into MyLife
- Member has at least one memory saved

##### Activate Memory Test Steps

1. **Click** on **Scrapbook**
2. **Click** on **Memory** Bar
3. **Click** on the desired memory
4. A memory popup window is shown to the member
5. **Close** the memory popup
6. **Ensure** "Active: \<Memory title>" is displayed just above member entry in chat area

##### Activate Memory Success Conditions

- Member has activated member and sees "Active: \<Memory title>"

##### Activate Memory Results

##### Activate Memory Additional Observations

---

#### Test Case: Deactivate Memory

##### Deactivate Memory Preconditions

- Member is logged into MyLife
- Member has at least one memory saved
- Memory is activated [see Activate Memory test case](#test-case-activate-memory)

##### Deactivate Memory Test Steps

1. **Ensure** "Active: \<Memory title>" is displayed just above member entry in chat area
2. **Click** on `X` to **Close**
3. **Confirm** active display disappears

##### Deactivate Memory Success Conditions

- "Active: \<Memory title>" no longer displays
- Memory is no longer being actively affected by chat

##### Deactivate Memory Results

##### Deactivate Memory Additional Observations

---

#### Test Case: Direct Edit

##### Direct Edit Preconditions

- Member is logged into MyLife
- Member has at least one memory saved

##### Direct Edit Test Steps

1. **Click** on **Scrapbook**
2. **Click** on **Memory** Bar
3. **Click** on the desired memory
4. A memory popup window is shown to the member
5. **Double-Click** the memory content summary to enable editing
6. **Edit** the memory by hand
7. **Click** on the **disk icon** to save the memory
8. **Close** the updated memory
9. **Click** the Memory Bar **Refresh** button
10. **Click** on same memory as above
11. **Verify** that memory is updated with the new content

##### Direct Edit Success Conditions

- Member should be able to edit and save the memory directly

##### Direct Edit Results

##### Direct Edit Additional Observations

---

#### Test Case: Quill Edit

##### Quill Edit Memory Preconditions

- Member is logged into MyLife
- Member has at least one memory saved

##### Quill Edit Memory Test Steps

1. **Click** on **Scrapbook**
2. **Click** on **Memory** Bar
3. **Click** on the desired memory
4. A memory popup window is shown to the member
5. **Click** on the **quill-and-paper icon** to enable editing
6. **Edit** the memory by hand
7. **Click** on the **disk icon** to save the memory
8. **Close** the updated memory
9. **Click** the Memory Bar **Refresh** button
10. **Click** on same memory as above
11. **Verify** that memory is updated with the new content

##### Quill Edit Success Conditions

- Member should be able to edit and save the memory using the quill-and-paper icon

##### Quill Edit Results

##### Quill Edit Additional Observations

---

#### Test Case: Edit Title 01

##### Edit Title 01 Preconditions

- Member is logged into MyLife
- Member has at least one memory saved

##### Edit Title 01 Test Steps

1. **Click** on **Scrapbook**
2. **Click** on **Memory** Bar
3. **Double-Click** on _title_ of the desired memory to enable editing
4. **Blur** field (click outside of the title textbox) or **hit Enter** to submit
5. **Verify** that title has changed in all locations

##### Edit Title 01 Success Conditions

- Member should be able to edit the memory title from the memories list

##### Edit Title 01 Results

##### Edit Title 01 Additional Observations

---

#### Test Case: Edit Title 02

- Member is logged into MyLife
- Member has at least one memory saved

##### Edit Title 02 Test Steps

1. **Click** on **Scrapbook**
2. **Click** on **Memory** Bar
3. **Click** on the desired memory
4. A memory popup window is shown to the member
5. **Double-Click** on _title_ of the popup to enable editing
6. **Blur** field (click outside of the title textbox) or **hit Enter** to submit
7. **Close** popup
8. **Verify** that title has changed in all locations

##### Edit Title 02 Success Conditions

- Member should be able to edit the memory title from the memories list

##### Edit Title 02 Results

##### Edit Title 02 Additional Observations

---

#### Test Case: Edit Title 03

##### Edit Title 03 Preconditions

- Member is logged into MyLife
- Member has at least one memory saved
- Memory is activated [see Activate Memory test case](#test-case-activate-memory)

##### Edit Title 03 Test Steps

1. **Ensure** "Active: \<Memory title>" is displayed just above member entry in chat area
2. **Double-Click** on "Active: \<Memory title>" to enable editing
3. **Modify** title
4. **Blur** field (click outside of the title textbox) or **hit Enter** to submit
5. **Verify** that title has changed in all locations

##### Edit Title 03 Success Conditions

- Member should be able to edit the memory title from the memories list

##### Edit Title 03 Results

##### Edit Title 03 Additional Observations

---

#### Test Case: Edit Title 04

##### Edit Title 04 Preconditions

- Member is logged into MyLife
- Member has at least one memory saved
- Memory is activated [see Activate Memory test case](#test-case-activate-memory)

##### Edit Title 04 Test Steps

1. **Ensure** "Active: \<Memory title>" is displayed just above member entry in chat area
2. **Double-Click** on "Active: \<Memory title>" to enable editing
3. Type in **Chat** area that you would like to change the title, and include the new title
4. **Hit Enter** to submit your text
5. The bot confirms it has changed the title
6. **Verify** that title has changed correctly in all locations

##### Edit Title 04 Success Conditions

- Bot was able to modify the title of a memory on behalf of member

##### Edit Title 04 Results

##### Edit Title 04 Additional Observations

---

### Interactive Edit Memory

#### Test Case: Interactive Edit 01

##### Interactive Edit 01 Preconditions

- Member is logged into MyLife
- Member has at least one memory saved
- Memory popup is open

##### Interactive Edit 01 Test Steps

1. **Click** on the rotating teal box with prompt text you find intriguing
2. The memory popup should auto-close
3. **Ensure** "Active: \<Memory title>" is displayed just above member entry in chat area
4. Text from teal prompts appears in chat area
5. Follow the text's lead and **describe** content around this memory
6. **Click** the **Submit** button
7. Bot should inform member that content is updated

##### Interactive Edit 01 Success Conditions

- Memory is updated in the memory list
- Memory is updated in the MyLife database

##### Interactive Edit 01 Results

##### Interactive Edit 01 Additional Observations

---

#### Test Case: Interactive Edit 02

##### Interactive Edit 02 Preconditions

- Member is logged into MyLife
- Member has at least one memory saved
- Memory is activated [see Activate Memory test case](#test-case-activate-memory)

##### Interactive Edit 02 Test Steps

1. Ask Bot to **delete** specific content from the summary using chat input
2. **Click** the **Submit** button
3. Bot should inform member that content is updated

##### Interactive Edit 02 Success Conditions

- Memory summary is updated in the memory list
- Memory is updated in the MyLife database

##### Interactive Edit 02 Results

#### Interactive Edit 02 Additional Observations

---

#### Test Case: Interactive Edit 03

##### Interactive Edit 03 Preconditions

- Member is logged into MyLife
- Member has at least one memory saved
- Memory is activated [see Activate Memory test case](#test-case-activate-memory)

##### Interactive Edit 03 Test Steps

1. Ask Bot to **add** content to the summary using chat input
2. **Click** the **Submit** button
3. Bot should inform member that content is updated

##### Interactive Edit 03 Success Conditions

- Memory summary is updated in the memory list
- Memory is updated in the MyLife database

##### Interactive Edit 03 Results

##### Interactive Edit 03 Additional Observations

---

#### Test Case: Interactive Edit 04

##### Interactive Edit 04 Preconditions

- Member is logged into MyLife
- Member has at least one memory saved
- Memory is activated [see Activate Memory test case](#test-case-activate-memory)

##### Interactive Edit 04 Test Steps

1. Ask Bot to **modify** content in the summary using chat input
2. **Click** the **Submit** button
3. Bot should inform member that content is updated

##### Interactive Edit 04 Success Conditions

- Memory summary is updated in the memory list
- Memory is updated in the MyLife database

##### Interactive Edit 04 Results

##### Interactive Edit 04 Additional Observations

---

### Relive Memory

#### Test Case: Relive Memory 01

##### Relive Memory 01 Preconditions

- Member is logged into MyLife
- Member has at least one memory saved
- Memory popup is open

##### Relive Memory 01 Test Steps

1. **Click** on the **Relive Memory** button
2. **Verify** that all memory popup windows are auto-closed
3. Bot should return with the beginning of your memory narrated back to you

##### Relive Memory 01 Success Conditions

- All popup memories closed
- Reliving Memory protocol engaged visibly

##### Relive Memory 01 Results

##### Relive Memory 01 Additional Observations

---

#### Test Case: Close Reliving Memory

##### Close Reliving Memory Preconditions

- Member is logged into MyLife
- Member has at least one memory saved
- [**Relive**](#test-case-relive-memory-01) protocol engaged

##### Close Reliving Memory Test Steps

1. Click on the **'X'** to close the reliving memory
2. Open the above memory again
3. Verify that the memory is not modified

##### Close Reliving Memory Success Conditions

- Memory should remain unedited

##### Close Reliving Memory Results

##### Close Reliving Memory Additional Observations

---

#### Test Case: Relive Memory 02

##### Relive Memory 02 Preconditions

- Member is logged into MyLife
- Member has at least one memory saved
- Memory popup is open

##### Relive Memory 02 Test Steps

1. **Click** on the **Relive Memory** button
2. Bot should return with the beginning of your memory narrated back to you
3. In **Relive** protocol, **update** the memory to add new content
4. **Click** update button
5. Bot should return with the next stage of your memory
6. **Click** the **'X'** button to close out of reliving memory
7. **Click** the memory bar **Refresh**
8. **Click** to open the same memory again
9. **Verify** that the memory is updated with the new content

##### Relive Memory 02 Success Conditions

- Member should be able to update the memory during the reliving process
- Memory is updated in the memory list with the updated content

##### Relive Memory 02 Results

##### Relive Memory 02 Additional Observations

---

### Delete a Memory

#### Test Case: Delete Memory

##### Delete Memory Preconditions

- Member is logged into MyLife
- Member has at least one memory saved

##### Delete Memory Test Steps

1. **Click** on **Scrapbook**.
2. **Click** on the **Memory bar**.
3. **Click** the **trash icon** to delete a memory
4. Alert pops up "Are you sure you want to delete this item?"
5. **Click** **Cancel**
6. **Click** the Memory Bar **Refresh**
7. **Verify** the memory is not deleted
8. **Click** the **trash icon** to delete the memory again.
9. Alert pops up "Are you sure you want to delete this item?"
10. Click **OK**
11. **Click** the Memory Bar **Refresh**
12. **Verify** the memory is deleted

##### Delete Memory Success Conditions

- Deleted memory is removed from the memories list

##### Delete Memory Results

##### Delete Memory Additional Observations

---

### Play Experiences

#### Test Case: Tutorial

##### Tutorial Preconditions

- Member is logged into MyLife

##### Tutorial Test Steps

1. **Click** on the **Avatar** Bar to open its options
2. **Verify** that the **Run Tutorial** button is shown (it will only show once per session)
3. **Click** on the **Run Tutorial** button
4. Screen drops and "Welcome to MyLife" message is shown
5. **Click** on the **"click me"** button
6. Member should follow instructions onscreen

**Note:** clicking onscreen will usually advance the action

##### Tutorial Success Conditions

- The incomplete tutorial should show the welcome message along with the Official Pre-Demo Tutorial
- The member should be able to chat during the experience via the tutorial

##### Tutorial Results

##### Tutorial Additional Observations

---

## Known Issues

- **Session timeout**: Upon session timeout the browser does not bring member to login screen, but leaves interface up as if it were working.
- **Updating Memories Issues**: [GitHub Issue #369](https://github.com/MyLife-Services/mylife-maht/issues/369) outlines an instance of the problem, but on occasion the Biographer will fail to run the correct sequence to 1) Retrieve a Summary from MyLife, and b) Update that Summary with its new information. It will now let you know how far it got in the process, and I am actively working on this bug, there are a few different ways to fix it, and I want to make the most scalable decision.
- **General Error Handling**: Altogether this is a mess and needs to be improved. Usually the last thing to get prioritized.

### Issue Prioritization

Please add here, or just above, any other issues or errors or features you deem important to be considered for fixes or incorporation into the platform. Then please use either the rest of this space or some ranking method of your choosing to let us know the importance of these various issues in your mind.

---

## Appendix

- [Original Issue #28](https://github.com/MyLife-Services/mylife-documentation/issues/28)
- [Original Test Sheet](https://docs.google.com/spreadsheets/d/1PHF6q5Bh5LufrtutfYY46PeADGNo6WpLgIQbrdokqUQ/edit?gid=1378114951#gid=1378114951)

The following categories are not currently relevant to the internal member experience unless new.

### Register Test Cases

#### Test Case: Newsletter

##### Newsletter Preconditions

- Visitor (by email address) is not a member of MyLife

##### Newsletter Test Steps

1. Open [MyLife Homepage](https://humanremembranceproject.org/)
2. Use the sidebar to enter the visitor's name and email
3. Click **Submit**
4. Verify that the sidebar changes to reflect receipt of the information

##### Newsletter Success Conditions

- Sidebar changes content to information about membership
- Data is added to the MyLife database

##### Newsletter Results

##### Newsletter Additional Observations

---

#### Test Case: Register

##### Register Preconditions

- Visitor (by email address) is not a member of MyLife

##### Register Test Steps

1. Open [MyLife Homepage](https://humanremembranceproject.org/)
2. Type and submit **"register me"** on the homepage
3. **Verify** that MyLife asks the visitor to enter the following details:
   - Avatar Name (3 to 32 characters)
   - Email Address
   - Your Name (3 to 64 characters)
   - "Once I have this information, I'll proceed with your registration!"
4. Enter the above details in the chat and submit
5. Verify that a message is displayed indicating that MyLife will contact the visitor via email within a week

##### Register Success Conditions

- MyLife confirms that the visitor will receive an email within a week
- Visitor receives an email with the link to confirm registration

##### Register Results

##### Register Additional Observations

---

### Create Account Test Case

#### Test Case: Create Account

##### Create Account Preconditions

- Visitor (by email address) is not a member of MyLife
- Visitor has successfully [registered](#test-case-register)
- Visitor has received identifying url

##### Create Account Test Steps

1. Follow personal url to [MyLife Homepage](https://humanremembranceproject.org/?vld=)
2. **Enter** email address to confirm registration
3. _Q_ should ask for date of birth and passphrase
4. **Provide** date of birth and case-sensitive passphrase
5. _Q_ informs of success
6. [Test Case Login](#test-case-login)

##### Create Account Success Conditions

- Visitor confirmed as registered member
- Member Account created
- Member Avatar created
- Memory Team created

##### Create Account Results

##### Create Account Additional Observations

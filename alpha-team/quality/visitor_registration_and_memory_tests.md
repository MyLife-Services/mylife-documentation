# MyLife Visitor Registration & Memory test cases

## Register
#### Preconditions
- Visitor (by email address) is not a member of MyLife

#### Test steps
- Type and submit "register me" on homepage
- "MyLife asks visitor to enter follwoing details:
- Avatar Name (3 to 32 characters)
- Email Address
- Your Name (3 to 64 characters) Once I have this information, I'll proceed with your registration!"
- Enter above details in the chat and submit.
- **Verify** that a message is displayed indicating that MyLife will contact the visitor via email within a week.
- **Result:**
- **Verify** visitor receives the link to register to MyLife
- **Result:**

#### Success Conditions
- MyLife confirms that the visitor will receive an email within a week.
- Visitor receives an email with the link to confirm registration.

#### Member Actual Result (if result is fail)


## Create Account
#### Preconditions
- Visitor (by email address) is not a member of MyLife
- Visitor has registration in MyLife database
- Visitor has unique link to finalize registration

#### Test steps
- Click on the link to finalise the registration.
- MyLife asks visitor to confirm the email address given while registering.
- Enter the same email address given while registration.
- NOTE: Must be completed in 5 minutes, or page needs to be refreshed
- MyLife asks visitor date of birth and passphrase for the account.
- Enter date of birth and passphrase.
- **Verify** that MyLife indicates visitor about the MyLife membership with congratulations message.
- **Result:**

#### Success Conditions
- Visitor should be enter date of bith and set passphrase.
- MyLIfe indicates visitor about successful registration.

#### Member Actual Result (if result is fail)


## Login
#### Preconditions
- Visitor MyLIfe registration is successful.
- visitor is a member of MyLife
- Visitor has login credentials to login.
- Test steps
- Navigate to https://humanremembranceproject.org/
- Click on Login button
- Select your avatar-id from the dropdown.
- Enter passphrase and login
- **Verify** that visitor is able to login successfully.
- **Result:**

#### Success Conditions
- Member is logged in and routed to member dashboard
- New Member Avatar created
- New Member Memory Team created
- Directed to Member Dashboard

#### Member Actual Result (if result is fail)

## Create a memory from Biographer bot
#### Preconditions
- Login to MyLife

#### Test steps
- Chat window indicates "I am a personal-avatar for visitor."
- Click on the biographer icon that is in green color.
- Verify that the icon color turns into yellow.
- Chat window again indicates "I am a personal-avatar for visitor."
- Share any content with the bot.
- Ensure bot informs the visitor that the memory is documented.
- Navigate to Scrapbook -> Memories.
- Click on the Refresh button.
- **Verify** that above memory is saved under memories.
- **Result:**

#### Success Conditions
- Memory is available in scrapbook

#### Member Actual Result (if result is fail)


## Direct edit Memory
#### Preconditions
- Login to MyLife
- Ensure visitor has at least one memory saved.

#### Test steps:
- Click on scrapbook
- Click on Memory bar
- Click on desired Memory
- Memory popup window is shown to the visitor.
- Double-click the memory message.
- Edit the memory by hand
- Click on disk icon to save the memory.
- Open the updated memory.
- **Verify** that memory is updated with the new content.
- **Result:**
- Click on any Memory.
- Memory popup window is shown to the visitor.
- Click on quill-and-paper icon to edit the message.
- Edit the memory by hand.
- click disk icon to save
- Open the updated memory.
- **Verify** that memory is updated with the new content.
- **Result:**

#### Success Conditions
- Memory is available in scrapbook
- Memory is updated in the memory list

#### Member Actual Result (if result is fail)


## Interactive Edit Memory
#### Preconditions
- Login to MyLife
- Ensure visitor has at least one saved memory.

#### Test steps:
- Click on scrapbook.
- Click on Memory bar.
- Click on desired Memory.
- Memory popup is open.
- Click on rotating teal shadow text.
- Memory popup is closed.
- Ensure Active: "<Memory title>" above the chat is shown to the visitor.
- Update the memory to add new content to the memory.
- Refresh memory bar
- Open the above updated memory.
- **Verify** that memory is updated with the new content.
- **Result:**

#### Success Conditions
- Memory is available in scrapbook
- Memory is updated in the memory list

- Member Actual Result (if result is fail)


## Relive memory
#### Preconditions
- Login to MyLife
- Ensure visitor has multiple saved memories.

#### Test steps:
- Click on Scrapbook.
- Click on the Memory bar.
- Open any memory by clicking on one of the memories.
- Click on the desired memory.
- **Verify** that the desired memory popup is opened.
- **Result:**
- Click on the Relive Memory button.
- **Verify** that all memory popup windows are closed.
- **Result:**
- While in the relive memory state, update the memory to add new content.
- **Verify** that the updated memory is shown to the visitor during the reliving process.
- **Result:**
- Click the 'x' button to close out of reliving memory.
- Refresh the memory bar.
- Open the updated memory again.
- **Verify** that memory is updated with the new content.
- **Result:**

#### Success Conditions
- Updated memory is shown to the visitor during the reliving process.
- Memory is available in scrapbook
- Memory is updated in the memory list

#### Member Actual Result (if result is fail)


## Delete a memory 
#### Preconditions
- Login to MyLife.
- Ensure visitor has multiple saved memories.

#### Test steps:
- Log in to MyLife.
- Ensure multiple memories are saved.
- Click on Scrapbook.
- Click on the Memory bar.
- Click the trash icon to delete a memory.
- **Verify** "Are you sure you want to delete this item?" with OK and Cancel buttons are shown to the visitor.
- **Result:**
- Click Cancel.
- **Verify** the pop-up closes.
- **Result:**
- Refresh the memory bar.
- **Verify** the memory is not deleted.
- **Result:**
- Click the trash icon to delete the memory again.
- **Verify** the confirmation message with OK and Cancel buttons.
- **Result:**
- Click OK.
- **Verify** the pop-up closes.
- **Result:**
- Refresh the memory bar.
- **Verify** the memory is deleted.
- **Result:**

#### Success Conditions
Deleted memory is removed from the memories list.

#### Member Actual Result (if result is fail)
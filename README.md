# Stop-Spam: Techniques to Stop Unsolicited Emails in Exchange
Every morning I wake up to a plethora of unsolicited spam blast. When you have a "C" in your title, you are a marked person. I figured I'd create an Exchange rule to stop, block, unsubscribe and report spam emails.

Note: Filtering in/out emails can break stuff and also block/report legitimate email, so please implement the following with care and **use at your own risk**.


**Step 1: Create an Outlook/Exchange rule**
- Will outsource the introduction/how-to make rules in Outlook to Microsoft: https://support.microsoft.com/en-us/office/set-up-rules-in-outlook-75ab719a-2ce8-49a7-a214-6d62b67cbd41

**Step 2: Add Conditions**
- Generally unsolicited marketing spam is sent directly to you:
  - Choose: "Sent only to me" 
- Unsolicited marketing spam usually have common keywords that will help identify unwanted email
  - I have created a starter list and hope the community will continue to add to this list:
  - Here is a the living list: https://github.com/miraisecurity/stop-spam/blob/main/keywordlist

**Step 3: Add Actions**
- Create an auto respond by selecting "have server reply using a specific message"
- You can create your own or use the templates below:
  - A gentle email: https://github.com/miraisecurity/stop-spam/blob/main/auto-reply-gentle
  - Nightmare email: https://github.com/miraisecurity/stop-spam/blob/main/auto-reply-nightmare
- You also want to move it out of the way, I suggest configuring "move it to a specific folder" such as "Junk"
- **AND** if you want to go to 11, you can also configure "forward it to people or public group" to report it to the Canadian regulator
  - **NOTE**: This is a bit aggressive and should be turned on once you are confident legitimate emails will not be caught
  - Spam Report Inbox: spam@fightspam.gc.ca
  
**Step 4: Add Exceptions**
- There will likely be some legitamate emails that get caught in this, so in the exceptions list add emails that you do not want to bounce
  - ie. *@microsoft.com. *@miraisecurity.com :)
  
**Step 5: Monitor**
- Keep an eye on your "Junk" folder to avoid legitimate emails getting caught in this rule and update the exceptions as required

# Gmail to Telegram: Automate Important Email Alerts Using AI and Google Apps Script

## What It Is

This project is a simple automation that sends instant Telegram notifications when you receive important emails in Gmail, using Google Apps Script and the help of AI tools. It’s ideal for anyone who gets too many emails and wants to focus only on the ones that really matter—without constantly checking their inbox or being distracted by unnecessary notifications.

**Key Features:**
- Instantly alerts you in Telegram for only the emails you care about.
- Lets you control notifications for just one Telegram chat.
- Runs for free and entirely within your own Google account—no paid subscriptions or extra servers.
- Customizable: You can change which emails trigger alerts and how messages are sent.

## How It Works

1. **Google Apps Script Checks Gmail**  
   - The script scans your Gmail for new, unread messages.
   - It looks for emails that match your rules—either from specific senders (like your boss or key team members) or containing certain subject keywords (like "Project Status Update").

2. **Sends Important Alerts to Telegram**  
   - When a matching email arrives, the script sends a notification straight into your chosen Telegram chat (via a custom Telegram bot).
   - Each alert includes a clickable link so you can jump directly to the email.

3. **Organizes Your Inbox**  
   - The script labels and marks those emails as read so you don’t get repeated notifications for the same message.

4. **Runs Automatically, No Extra Hosting**  
   - Everything runs within your Google account, completely free and with no external servers required.
   - You can customize the logic at any time to add more sender addresses or topics, or tweak how the messages appear in Telegram.

## Typical Workflow Example

- **Step 1:** Set up Google Apps Script to monitor Gmail.
- **Step 2:** Define your notification rules (specific senders, keywords, etc.).
- **Step 3:** Connect your Telegram account and set up a bot to receive messages.
- **Step 4:** Whenever a matching email arrives, you get a Telegram alert—including a link to view the email directly.
- **Step 5:** Stay productive! No need to refresh your inbox or get interrupted by every message—only the important ones.

---

Feel free to check out the setup instructions, customize the script, and start focusing on what matters most in your inbox.

# How to Set Up Gmail-to-Telegram Email Alerts

This section explains how to quickly set up a Telegram bot and connect it to your Gmail via Google Apps Script—no coding experience needed!

---

## 🤖 Setting Up a Telegram Bot

1. **Find BotFather:**  
   In the Telegram app, search for [@BotFather](https://core.telegram.org/bots#botfather) (_Bots: An introduction for developers_).

2. **Create Your Bot:**  
   Start a chat with BotFather and use the `/newbot` command.  
   Follow the prompts to give your bot a name and a unique username.

3. **Get Your Bot Token:**  
   After setup, BotFather will provide a **bot token**.  
   _Copy and save this token_ — you’ll enter it in your Google Apps Script.

4. **Find Your Chat ID:**  
   - Send a message to your new bot from your Telegram account.
   - Visit:  
     ```
     https://api.telegram.org/bot<YOUR_BOT_TOKEN>/getUpdates
     ```
   - Look for `"chat":{"id":<your_chat_id>,...}` in the response.  
     Copy your chat ID — your script will need it so it knows where to send alerts.

---

## 🛠️ Making It Work

1. **Paste the Script into Google Apps Script:**  

   - **Grab the script here:** [GmailToTelegram/GoogleAppScript on GitHub](https://github.com/matuyle/GmailToTelegram/blob/main/GoogleAppScript)
   - Open [Apps Script | Google for Developers](https://script.google.com) from your Google Drive.
   - Create a new project and paste the provided script.

3. **Enter Your Bot Token & Chat ID:**  
   - At the top of the script, insert the bot token and chat ID from the previous steps.

4. **Edit the Email Rules:**  
   - Change the subject keyword or sender addresses in the script to match what "important" means for you.

5. **Authorize the Script:**  
   - Save and run the script once manually.
   - Grant permissions when prompted (for Gmail access and sending Telegram messages).

6. **Automate with a Trigger:**  
   - In Google Apps Script, click on the clock icon to set up a time-based trigger.
   - Choose the `checkMail()` function to run at your preferred interval (e.g., every 5 minutes).

---

That's it! Whenever an important email arrives, you'll receive a Telegram alert—never miss a crucial message again!

---


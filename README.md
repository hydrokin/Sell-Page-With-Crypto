
**Telegram Bot API Integration**

After installing Telegram bot. If someone makes a payment, a notification message will be sent to your telegram account and you will send the file you want to give in return for payment to the user's e-mail address.

This guide explains how to integrate Telegram Bot API and obtain the chat ID. Follow the steps below to set up the integration:

1. Creating a Telegram Bot:
   - Find BotFather bot in the Telegram app or on Telegram Web.
   - Send the `/newbot` command to BotFather, and it will provide you with a bot token.
   - Replace `"ENTER_HERE_YOUR_TELEGRAM_BOT"` in the JavaScript code with your bot token.

2. Obtaining the Chat ID:
   - Locate the bot you created in the Telegram app or on Telegram Web.
   - Start a new chat or select an existing chat where you want to interact with the bot.
   - Enter the following API request in your browser's address bar and hit Enter:

     ```
     https://api.telegram.org/bot<bot_token>/getUpdates
     ```

     (Replace `<bot_token>` with your bot token)

   - This API request will return a JSON response containing information about your chat.
   - In the response, find the `"chat"` section and locate the "id" field. Copy its value.
   - Replace `"ENTER_HERE_YOUR_CHAT_ID"` in the JavaScript code with the copied chat ID.

3. Modifying the JavaScript Code:
   - Replace the comment placeholder `"ENTER_HERE_YOUR_TELEGRAM_BOT"` in the JavaScript code with your bot token.
   - Replace the comment placeholder `"ENTER_HERE_YOUR_CHAT_ID"` in the JavaScript code with your chat ID.

For example:

```javascript
var telegramBotToken = "PASTE_YOUR_BOT_TOKEN_HERE";
var chatId = "PASTE_YOUR_CHAT_ID_HERE";
```

By following the above steps, you can add your Telegram bot's API credentials and chat ID to the JavaScript code. This will enable the `sendTelegramMessage()` function to send messages via Telegram.

Please note that the code provided is for demonstration purposes and may require additional modifications and server-side implementation for a complete and secure integration with Telegram.

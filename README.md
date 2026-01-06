# Discord Auto Bot

Discord Auto Bot is an automated bot that can reply to messages on Discord using Google Gemini AI or messages from a text file. This bot supports multiple accounts and channels.

## Features

- ✨ Auto reply using Google Gemini AI (gemini-2.5-flash)
- 🤖 Support multiple Discord accounts
- 📝 Reply from text file (message.txt)
- 🌐 Support Indonesian and English languages
- ⏱️ Slow mode support
- 🔄 Reply mode with message reference
- 🗑️ Auto delete messages with delay or immediate deletion
- 📊 Colored console logging
- 🔄 Multiple channel support

## Requirements

- Python 3.7+
- Python packages:
  - requests
  - colorama
  - pytz

## Installation

1. Clone this repository:
```bash
git clone https://github.com/febriyan9346/Discord-Auto-Bot.git
cd Discord-Auto-Bot
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Create `accounts.txt` file with this format:
```
TOKEN=your_discord_token_1
API_KEY=your_google_api_key_1

TOKEN=your_discord_token_2
API_KEY=your_google_api_key_2
```

4. Create `message.txt` file (optional, for non-AI mode):
```
Message 1
Message 2
Message 3
```

## How to Get Token and API Key

### Discord Token
1. Open Discord in browser
2. Press F12 to open Developer Tools
3. Go to Network tab
4. Perform any activity on Discord (send message, etc.)
5. Look for requests containing "Authorization" header
6. Copy the token value

### Google API Key
1. Visit [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Login with your Google account
3. Click "Create API Key"
4. Copy the provided API key

**⚠️ Warning**: Never share your token or API key with anyone!

## Usage

Run the bot:
```bash
python bot.py
```

### Configuration per Channel

When running the bot, you will be asked to configure each channel:

1. **Use Google Gemini AI**: Use AI to generate automatic replies
   - `y`: Use Gemini AI
   - `n`: Use messages from message.txt

2. **Select prompt language**: Language for AI prompt
   - `en`: English
   - `id`: Indonesian

3. **Enter message read delay**: Delay before reading new messages (seconds)

4. **Enter interval**: Wait time before next iteration (seconds)

5. **Use slow mode**: Respect Discord channel slow mode
   - `y`: Enable
   - `n`: Disable

6. **Send message as reply**: Send as reply to message
   - `y`: Reply mode
   - `n`: Normal message

7. **Delete bot reply**: Delete bot message after sending
   - `y`: Enable auto delete
   - `n`: Don't delete

8. **Delete message immediately**: Delete without delay
   - `y`: Delete immediately
   - `n`: Delete with delay

## File Structure

```
Discord-Auto-Bot/
├── bot.py              # Main bot file
├── accounts.txt        # Discord tokens and API Keys
├── message.txt         # Messages for non-AI mode
├── requirements.txt    # Python dependencies
└── README.md          # Documentation
```

## Usage Examples

### AI Mode (Gemini)
The bot will read the latest message in the channel and reply with a response from Gemini AI in the selected language.

### File Mode
The bot will send random messages from message.txt at specified intervals.

## Troubleshooting

### Bot not replying
- Make sure Discord token is valid
- Ensure bot has permissions in the channel
- Check console for error messages

### API Key error (429)
- Bot will automatically rotate to another API key
- If all keys hit limit, bot will wait 24 hours

### Message not processed
- Make sure message contains text (not just attachments)
- Ensure message is not from the bot itself

## Important Notes

- This bot is for educational purposes
- Use wisely according to Discord Terms of Service
- Don't spam or abuse the bot
- Keep your accounts.txt file secure

## License

This project is licensed under the MIT License.

## Author

Created by FEBRIYAN

## Contributing

Contributions, issues, and feature requests are welcome!

## Support Us with Cryptocurrency

You can make a contribution using any of the following blockchain networks:

| Network | Wallet Address |
|---------|----------------|
| **EVM** | `0x216e9b3a5428543c31e659eb8fea3b4bf770bdfd` |
| **TON** | `UQCEzXLDalfKKySAHuCtBZBARCYnMc0QsTYwN4qda3fE6tto` |
| **SOL** | `9XgbPg8fndBquuYXkGpNYKHHhymdmVhmF6nMkPxhXTki` |
| **SUI** | `0x8c3632ddd46c984571bf28f784f7c7aeca3b8371f146c4024f01add025f993bf` |

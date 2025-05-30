# Maxowntown Selfreact Bot

This is a simple auto-react Discord bot built using `discord.py`.

## Features

- Reacts to messages from a specific user (you)
- Runs in Termux or any Python environment
- Simple to set up and use

## Setup Instructions (Termux)

```bash
# 1. Install dependencies
pkg install python git -y
pip install -U pip
pip install -r requirements.txt

# 2. Run the bot
python bot.py

Configuration

Edit bot.py and replace:
	•	YOUR_BOT_TOKEN_HERE with your bot token
	•	USER_ID with your Discord user ID
	•	EMOJI with the emoji you want the bot to use

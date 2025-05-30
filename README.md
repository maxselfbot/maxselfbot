📁 (Folder structure:)

maxowntown/
├── bot.py
├── requirements.txt
└── README.md

📁 (bot.py)
import discord

TOKEN = 'YOUR_BOT_TOKEN_HERE'  # Replace this with your bot token
USER_ID = 123456789012345678  # Replace with your Discord user ID
EMOJI = '🔥'  # Change to any emoji you want

intents = discord.Intents.default()
intents.message_content = True

client = discord.Client(intents=intents)

@client.event
async def on_ready():
    print(f'Bot connected as {client.user}')

@client.event
async def on_message(message):
    if message.author.id == USER_ID:
        try:
            await message.add_reaction(EMOJI)
            print(f"Reacted to message: {message.content}")
        except Exception as e:
            print(f"Error reacting: {e}")

client.run(TOKEN)

📄 (requirements.txt)

discord.py==2.3.2


📄 (README.md)

# Maxowntown Discord Bot

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

---

### ✅ Steps to create your GitHub repo in Termux:

```bash
# Install git
pkg install git

# Configure git
git config --global user.name "Your Name"
git config --global user.email "you@example.com"

# Create repo
mkdir maxowntown
cd maxowntown

# Add files
# (Use a text editor like nano or vim to copy/paste the above files)
nano bot.py
nano requirements.txt
nano README.md

# Initialize git
git init
git add .
git commit -m "Initial commit"

# Create a GitHub repo at https://github.com (you’ll need to log in)
# Name it: maxowntown

# Then push:
git remote add origin https://github.com/yourusername/maxowntown.git
git branch -M main
git push -u origin main

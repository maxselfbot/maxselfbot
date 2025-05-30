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


<!---
maxselfbot/maxselfbot is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->

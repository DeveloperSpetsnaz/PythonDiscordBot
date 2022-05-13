import discord
import os
import random

client = discord.Client()

@client.event
async def on_ready():
	print("Connected")
	print(client.user)
	print("")

@client.event
async def on_member_join(member):
	await member.create_dm()
	await member.dm_channel.send(
		f'Glad I can count on you to join me ,{member.name}.')

@client.event
async def on_message(message):
	print(message.author)
	print(message.channel)
	print(message.content)
	print("")
	if message.author == client.user:
		return
	albedo_quotes = [
		'If one day, I lose control... destroy Mondstadt... destroy everything...',
		'Can I rely on you to stop me?',
		'Have you ever considered that the world of Teyvat may have a natural hostility to outlanders?',
		'I am Albedo, Chief Alchemist of the Knights of Favonius.',
		'You carry the aura of the stars, interesting...',
		'I would like to study you, if you do not mind.',
		'I\'m certain we will have many opportunities to be alone in the future.',
		'One day, I will uncover it\'s secrets, it\'s only a matter of time.',
		'Genius? ... A number of people call me that. But I don\'t think I\'m any "genius".',
		'The capacity of our brains is limited, so we are bound to forget things.',
		'Would you oblige me by serving as my assistant?',
		'After observing so many experiments, you surely know a good deal about alchemy by now.',
		'I have faith in my ability to instruct you, and even more faith in your exeptional talents.',
		'Your help inspired me to discover the means to make a flower bloom.',
		'Everything you do is an action I wish to observe.',
		'I mean that the time that I\'ve spent traveling with you in the mountains was a valuable journey for me.',
		'In the future... If the need arises... Can I solicit your help again?',
		'Those born of Earth are bound by it\'s imperfections, but those born of chalk are free of impurities... You and I are alike, both composed of a substance that has yet to be fully defined...'
	]
	if 'albedo' in message.content.lower():
		await message.channel.send(random.choice(albedo_quotes))

token = os.environ['TOKEN']
client.run(token)

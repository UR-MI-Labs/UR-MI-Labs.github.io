---
layout: post
title:  "Discord-Bot #01"
date:   2022-09-09 17:37:24 +0200
categories: project update discordbot
---
# Discord-Bot

Im Zuge der [Anforderungsanalyse](/_posts/2022-08-14-Anforderungsanalyse.md) haben wir verschiedene Verbesserungsvorschläge, bzw. Lösungen für das VR4 zusammengefasst. Unter dem Punkt *Community* fassen wir alle Vorschläge für die Verbesserung der Interaktion aller Labornutzenden. Für eine einfachere Kommunikation werden wir auf ein bereits bestehendes System zurückgreifen: einen Discord-Server. 
Zur noch einfacheren Kommunikation ist unsere Idee ein Discord-Bot, der auf sogenannte Befehle eines Nutzers wartet und darauf eine vorgefertigte Nachricht versendet. So können Labornutzende einfach den Betreur:innen bescheid geben, dass z.B. gerade Hilfe an einem Projekt gebraucht wird. 

___

## Implementierung

### Bot Application

Um für Discord einen Bot zu implementieren, muss man diesen erst im [Discord Developer Portal](https://discord.com/developers/applications) über seinen Discord-Account erstellen. Ein Bot läuft hierbei als Applikation. 
Jeder Bot bekommt von Discord einen individuellen Token, den man nur einmal ansehen kann. Wenn man diesen Token vergessen hat, kann man unkompliziert einen neuen erstellen, aber wiederrum nur einmalig ansehen. Durch diesen Token werden die Funktionen des Bots implementiert und sollte deswegen nicht veröffentlicht werden. 

Für die ersten "Gehversuche" des MI-Lab-Bots wird dieser erstmal auf einen Test-Server eingeladen und dort auf alle Funktionen getestet. 

![Bot](/assets/2022-09-09-bot.jpg)

___

### Packages

Der Bot wird in diesem Fall mit JavaScript implementiert. Dafür müssen einige Dinge installiert werden:

- *Node.js* 
    - (mind. Node v16.9.0 oder höher)
- *discord.js*
    - für die Interaktion mit der Discord API 
    - 'npm install discord.js'
- *discordjs/rest* 
    - einfacher REST manager für discord.js
    - 'npm install @discordjs/rest'
- *dotenv* 
    - um '.env'-Files zu nutzen
    -'npm install dotenv'

____

### Files

*.env*
'''
TOKEN="token-here"
'''

*bot.js*
In diesem File loggt sich der Bot ein und solange das Skript läuft, bleibt der Bot online.

''' javascript
// require everything necessary
const { Client, GatewayIntentBits } = require('discord.js');
require('dotenv').config(); 

// client instance
const client = new Client({ intents: [GatewayIntentBits.Guilds] });

// when client is ready, this code runs once
client.once('ready', () => {
	console.log('Ready!');
});

//listening for interactions, e.g. commands
client.on('interactionCreate', async interaction => {
	if (!interaction.isChatInputCommand()) return;

	const { commandName } = interaction;

	if (commandName === 'ping') {
		await interaction.reply('Pong!');
	}
});

// login with token
client.login(process.env.TOKEN);
'''

____

## Funktionsweise

Hinweis: das sind nur erste Testläufe, keine endgültige Funktionsweise des Bots!

Mit 'node bot.js' den Bot online bringen und in einem Discord-Chat den Befehl '/ping' eingeben.

![Ping-Pong](/assets/2022-09-09-bot_ping.gif)
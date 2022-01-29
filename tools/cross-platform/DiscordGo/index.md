---
layout: default
title: DiscordGo
parent: Cross Platform
---

# DiscordGo

![nil](https://img.shields.io/badge/nil-goated-green)
![Version](https://img.shields.io/badge/Version-2.0-brightgreen)
![Language](https://img.shields.io/badge/Language-Go-blue.svg?longCache=true&style=flat-square)
[![Go Report Card](https://goreportcard.com/badge/github.com/emmaunel/DiscordGo)](https://goreportcard.com/report/github.com/emmaunel/DiscordGo)
![nil](https://img.shields.io/badge/nil-goated-green)

> DISCLAIMER: This tool is for educational, competition, and training purposes only. I am in no way responsible for any abuse of this tool

Discord C2 for Redteam engagement

### Github Link: [DiscordGo](https://github.com/emmaunel/DiscordGo)

# Why It was made this

During Blue-Red Team competition, we needed an easy and fast way to keep connected and a way for mutiple redteamer to run commands, hence DiscordGo.
Since Discord is getting popular, why not use the platorm as a c2.
That's what this project is about.

# Installation

To use DiscordGo, you need to create a Discord bot and a Discord server. After that, invite the bot to your server.

Click [here](https://support.discord.com/hc/en-us/articles/204849977-How-do-I-create-a-server-) to learn how to create a server and [here](https://discordjs.guide/preparations/setting-up-a-bot-application.html#creating-your-bot) to create a bot. And finally, learn to invite the bot to your server with [this.](https://discordjs.guide/preparations/adding-your-bot-to-servers.html#bot-invite-links)

When creating the bot, you need it give it some permission. For testing, I gave the bot full `administrative` permission. But the required permission are as follow:

* Send Messages
* Read Messages
* Attach Files
* Manage Server

# Usage

Edit this file `pkg/util/variables.go` with your `BotToken` and `ServerID`. Or create the file if not there

The bot token can be found on discord developer dashboard where you created the bot. To get your server ID, go to your server setting and click on `widget`. On the right pane, you see the your ID.

An example configuration file looks like this:
```
var ServerID = "XXXXXXXXXXX"
var BotToken = "XXXXXXXXXXX"
```

After that is done, all you have to do is run `make`. That will create 3 binaries.

```
- linux-agent
- windows-agent.exe
- macos-agent
```

## Organizer Bot

To use the organizer bot, create a .csv file with the following format(targetIP, teamNum, hostname):
* Note target IP shouldn't have the `.` between them.

```
192168185200,team01,hostname1
192168185201,team02,hostname2
```

To start the organizer bot: `go run cmd/organizer/main.go --target <csv_filename>.csv`

Run `clean` in any channel to organize bots into their respective categories.

# Feature

* Cross-platform
* Organizer bot to put targets in the right category


Logo by @BradHacker(https://github.com/BradHacker)

## Authors

- PabloPotat0 - [PabloPotat0](https://github.com/emmanuel)
- d3adzo - [d3adzo](https://github.com/d3adzo)
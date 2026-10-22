# Slack Bot

A simple Slack bot written in Go. It listens for one command and replies with a calculated age.

## What it does

Send the bot a message:

```
my yob is 2000
```

and it replies:

```
Age is 26
```

(`yob` = year of birth. The age is calculated against 2026.)

The bot also logs every command event (timestamp, command, parameters) to the console.

## Tech stack

- **[Go](https://go.dev/)**
- **[slacker](https://github.com/shomali11/slacker)** — a framework for building Slack bots in Socket Mode

## Requirements

- Go 1.26 or newer
- A Slack app with **Socket Mode** enabled, which gives you two tokens:
  - a **Bot Token** (`xoxb-...`)
  - an **App Token** (`xapp-...`)

## Setup

1. Clone the repository:

   ```bash
   git clone https://github.com/kiril755/slack_bot.git
   cd slack_bot
   ```

2. Set your Slack tokens as environment variables:

   ```bash
   export SLACK_BOT_TOKEN="xoxb-your-bot-token"
   export SLACK_APP_TOKEN="xapp-your-app-token"
   ```

3. Run the bot:

   ```bash
   go run main.go
   ```

Once running, invite the bot to a channel and send it `my yob is <year>`.

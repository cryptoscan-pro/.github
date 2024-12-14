# Telegram Grabber Bot - Cryptoscan

Telegram Grabber Bot is a Telegram bot that allows you to manage multiple Telegram accounts and scrape data from Telegram channels.

**Current Price**: $900

What you get:

- Free setup into your hosting
- Free help to integrate app to your server
- Full access to the codebase and code updates
- Free updates for app, you can request for free updates via access to issues
- Full access to Project Time tracking by developers

## Features

- Add and manage multiple Telegram accounts
- Scrape messages, media, and other data from Telegram channels
- Blacklist specific users or messages
- Logging and error handling

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/your-username/tg-grabber-bot.git
   ```
2. Install dependencies:
   ```
   cd tg-grabber-bot
   bun install
   ```
3. Create a `.env` file in the project root and add your Telegram bot token:
   ```
   BOT_TOKEN=your_telegram_bot_token
   ```
4. Build the project:
   ```
   make build
   ```
5. Start the bot:
   ```
   make run
   ```

## Docker

A Dockerfile is provided to run the bot in a Docker container. You can use the provided Makefile commands to build, run, stop, remove, and clean the Docker image and container:

- Build the Docker image:
  ```
  make build
  ```
- Run the Docker container:
  ```
  make run
  ```
- Stop the Docker container:
  ```
  make stop
  ```
- Remove the Docker container:
  ```
  make remove
  ```
- Clean up the Docker image:
  ```
  make clean
  ```

## Usage

1. Start the bot by sending the `/start` command to your Telegram bot.
2. Use the inline buttons to add a new Telegram session, delete a session, or list all active sessions.
3. When adding a new session, you'll be prompted to enter the session ID, admin string, and channels to parse.
4. The bot will automatically start scraping data from the configured Telegram channels.
5. You can blacklist specific users or messages by sending the `/set_blacklist` command and entering a comma-separated list of blacklisted items.

# Telegram Access Bot

Multi-language Telegram bot for managing access to private channels based on subscription to the main channel. Supports Russian and English languages, automatically detects user's language, and provides appropriate channels.

**Contacts**: [https://t.me/dan_cryptoscan](https://t.me/dan_cryptoscan)

What you get:

- Free setup into your hosting
- Free help to integrate app to your server
- Full access to the codebase and code updates
- Free updates for app, you can request for free updates via access to issues
- Full access to Project Time tracking by developers

## Features

- 🌍 Multi-language support (RU/EN)
- 🔄 Automatic user language detection
- 🔐 Channel subscription verification
- 🎯 Single-use invite link generation
- 📊 User statistics
- 📨 Message broadcasting system
- ⏰ Daily reminders for unsubscribed users

## Requirements

- Node.js 16+
- pnpm
- Telegram Bot Token (get from [@BotFather](https://t.me/BotFather))
- Two channels for each language (public source + private target)

## Installation

1. Clone the repository:
```bash
git clone [repository-url]
cd telegram-access-bot
```

2. Install dependencies:
```bash
pnpm install
```

3. Create configuration file:
```bash
cp config.example.yaml config.yaml
```

4. Configure config.yaml:
```yaml
bot:
  token: "YOUR_BOT_TOKEN"  # Token from @BotFather
  adminIds: [123456789]    # Admin user IDs

channels:
  ru:
    sourceChannelId: "@channel_name_ru"  # Public channel (with @)
    targetChannelId: "-100123456789"     # Private channel (with -100)
    targetChannelLink: "https://t.me/+abcdefghijk"
  en:
    sourceChannelId: "@channel_name_en"
    targetChannelId: "-100987654321"
    targetChannelLink: "https://t.me/+zyxwvutsrqp"
```

## Running

Development:
```bash
pnpm run dev
```

Production:
```bash
pnpm run build
pnpm run start
```

## Bot Commands

### User Commands

- `/start` - Start interaction with the bot
- `/check` - Check subscription status

### Admin Commands

- `/stats` - Show user statistics
- `/broadcast_all [text]` - Send message to all users
- `/broadcast_subscribed [text]` - Send message to subscribed users
- `/broadcast_unsubscribed [text]` - Send message to unsubscribed users

## Channel Setup

1. Create two channels for each language:
   - Public channel (source) - must have a username
   - Private channel (target) - can be private

2. Add the bot as an administrator to both channels

3. Get channel IDs:
   - For public channel, use username with @ (e.g., "@mychannel")
   - For private channel, get ID via [@getidsbot](https://t.me/getidsbot)
   - Private channel ID must start with -100

## Statistics and Data

Bot saves user data in `data/users.json`:
- User ID
- Username
- First and last name
- First interaction date
- Access status
- Selected language

Statistics include:
- Total number of users
- Number of subscribed/unsubscribed users
- Language distribution

## Message Broadcasting

Administrators can send messages to different user groups:
```
/broadcast_all Important announcement for everyone!
/broadcast_subscribed New content in private channel
/broadcast_unsubscribed Don't forget to subscribe to the channel!
```

Broadcasting system includes:
- Anti-spam protection (delay between messages)
- Delivery report (number of successful/failed sends)
- Markdown markup support

## Daily Reminders

Bot automatically sends reminders to unsubscribed users:
- Sent at 12:00 every day
- Different messages for each language
- Message rotation for variety

## Security

- Single-use invite links for private channel
- Admin rights verification for special commands
- Anti-spam protection for broadcasts

## Troubleshooting

If you encounter problems:
1. Check bot permissions in channels
2. Verify channel IDs are correct
3. Ensure public channels have usernames
4. Check error logs in console

## License

MIT

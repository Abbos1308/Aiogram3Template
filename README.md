# Telegram Admin Bot

A Telegram bot built with aiogram 3 featuring an admin panel for user management, advertising, statistics, and forced subscription management.

## Features

- **Admin Panel**: Accessible via inline keyboard with menu navigation
- **Advertising**: Broadcast messages to all users
- **Statistics Dashboard**: 
  - Total users
  - Active users (last 7 days)
  - New users today
  - Blocked users
- **Forced Subscription**: Manage required channels for bot access
- **PostgreSQL Database**: For persistent data storage

## Project Structure

```
.
├── bot/
│   ├── config/
│   │   └── settings.py          # Configuration and environment variables
│   ├── database/
│   │   ├── models.py             # Database schema and connection
│   │   └── queries.py            # Database operations
│   ├── handlers/
│   │   ├── user.py               # User command handlers
│   │   └── admin.py              # Admin panel handlers
│   ├── keyboards/
│   │   ├── admin.py              # Admin inline keyboards
│   │   └── user.py               # User inline keyboards
│   ├── middlewares/
│   │   └── admin.py              # Admin verification middleware
│   └── utils/
│       └── helpers.py            # Helper functions
├── main.py                       # Bot entry point
├── requirements.txt              # Python dependencies
└── .env                          # Environment variables (not in git)
```

## Setup

1. **Get Bot Token**: 
   - Go to [@BotFather](https://t.me/BotFather) on Telegram
   - Create a new bot or use existing one
   - Copy the bot token

2. **Get Your Admin ID**:
   - Send a message to [@userinfobot](https://t.me/userinfobot)
   - Copy your user ID

3. **Set Environment Variables**:
   Create a `.env` file with:
   ```
   BOT_TOKEN=your_bot_token_here
   ADMIN_ID=your_telegram_user_id
   DATABASE_URL=your_database_url
   ```

4. **Run the Bot**:
   ```bash
   python main.py
   ```

## Usage

### For Users
- Send `/start` to the bot
- If forced subscription is enabled, subscribe to required channels
- Click "Check Subscription" to verify

### For Admins
- Send `/start` to see the admin menu
- **Advertising**: Send broadcasts to all users
- **Statistics**: View bot usage statistics  
- **Forced Subscription**: 
  - Add channels (bot must be admin in the channel)
  - Remove channels
  - View list of required channels

## Database Schema

- **users**: Stores user information and activity
- **admins**: Stores admin user IDs
- **channels**: Required channels for forced subscription
- **broadcast_messages**: History of broadcast messages

## Requirements

- Python 3.11+
- aiogram 3.13.1
- asyncpg 0.29.0
- python-dotenv 1.0.0
- PostgreSQL database
# Aiogram3Template
# Aiogram3Template
# Aiogram3Template
# Aiogram3Template

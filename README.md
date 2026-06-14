# 🐉 Dragon Race to the Edge - WhatsApp Bot

A feature-rich WhatsApp bot with dragon catching, racing, battles, guilds, and more!

## ✨ Features

### 🐲 Dragon System
- **Catch Wild Dragons** - Random encounters with various dragon types and rarities
- **Dragon Breeding** - Combine dragons to create stronger offspring
- **Dragon Training** - Level up and customize your dragons
- **Pokedex (Dex)** - Track all dragons you've caught

### 🏁 Racing System
- **Dragon Racing** - Race your dragons against other players
- **Race to the Edge** - Themed racing events with special rewards
- **Rankings** - Global leaderboards for top racers
- **Tournaments** - Competitive racing events

### ⚔️ Battle System
- **PvP Battles** - Fight other players' dragons
- **Type Effectiveness** - 8 different dragon types with strategic matchups
- **Dungeon Mode** - Co-op dungeon exploration with boss fights
- **Environmental Effects** - Different battlegrounds with unique advantages

### 💰 Economy System
- **Gold Currency** - Earn gold from battles, quests, and daily rewards
- **Banking** - Deposit and withdraw gold safely
- **Trading** - Trade dragons and items with other players
- **Market** - Buy and sell items and dragons

### 🏰 Guild System
- **Create Guilds** - Found your own guild (10,000 gold)
- **Guild Perks** - XP and loot bonuses for members
- **Guild Wars** - Compete against other guilds
- **Guild Treasury** - Shared guild resources

### 🎴 Card Collecting
- **Wild Card Spawns** - Random cards appear in groups
- **Card Packs** - Buy packs with guaranteed rares
- **Card Trading** - Trade cards with other players
- **Deck Building** - Create custom decks for battles

### 👑 Owner System
- **Owner Commands** - Full bot control for owner (+26771256815)
- **Moderation** - Ban/unban, timeout, warnings
- **Admin Tools** - Give items, reset accounts, manage settings
- **Broadcast** - Send messages to all players

## 🚀 Quick Start

### Prerequisites
- Node.js 14+
- npm
- WhatsApp account (not business)

### Installation

```bash
# Clone the repository
git clone https://github.com/Kingsque/dragon-bot.git
cd dragon-bot

# Install dependencies
npm install

# Setup configuration
cp config.example.env .env

# Edit .env with your settings:
# - BOT_OWNER_NUMBER=26771256815
# - Add API keys (Cloudinary, Giphy, Unsplash)
# - WILD_SPAWNS_ENABLED=true

# Initialize databases and setup
npm run setup

# Start the bot
npm start
```

### Connect to WhatsApp

1. Wait for QR code to appear in terminal
2. Open WhatsApp on your phone
3. Go to **Settings > Linked Devices**
4. Click **"Link a Device"**
5. Scan the QR code with your phone's camera

The bot will now be active!

## 📝 Commands

### Player Commands
```
%help              - Show all available commands
%catch             - Attempt to catch a wild dragon
%dex               - View your dragon collection
%dragon [name]     - View specific dragon details
%party             - Manage your party (up to 6 dragons)
%battle @player    - Challenge another player
%race @player      - Start a dragon race
%balance           - Check your gold balance
%daily             - Claim daily reward (500 gold)
%profile           - View your profile
%leaderboard       - View top players
%guild             - View guild information
%join [guild_id]   - Join a guild
```

### Battle Commands (During Battle)
```
%attack [move]     - Attack with selected move
%defend            - Defensive stance (+1 defense)
%ultimate          - Use ultimate attack (costs 50 stamina)
%surrender         - Give up the battle
```

### Trading & Market
```
%trade @player     - Initiate a trade with another player
%market            - Browse available items
%buy [item]        - Purchase item from market
%sell [item]       - Sell item to market
```

### Guild Commands
```
%createguild [name] - Create a new guild (10,000 gold)
%guild             - View current guild info
%invite [@user]    - Invite player to guild
%guildwar [guild]  - Start war with another guild
```

### Card Commands
```
%cards             - View your card collection
%claim             - Claim a wild card
%buypack           - Buy a card pack (300 gold)
%claimpack         - Claim your purchased pack
%deck              - Manage your card deck
```

### Owner Commands (+26771256815 only)
```
%givegold [@user] [amount]     - Give gold to player
%givedragon [@user] [name]     - Give dragon to player
%ban [@user]                   - Ban a player
%unban [@user]                 - Unban a player
%addmod [@user]                - Make someone a moderator
%reset [@user]                 - Reset player account
%broadcast [message]           - Send global message
%wild [on/off]                 - Toggle wild spawns
%eval [code]                   - Execute code (owner only)
```

## ⚙️ Configuration

### Required Environment Variables

Create a `.env` file in the root directory:

```env
# Bot Owner
BOT_OWNER_NUMBER=26771256815
BOT_OWNER_NAME=Dragon Master

# APIs (required for full functionality)
CLOUDINARY_CLOUD_NAME=your_name
CLOUDINARY_API_KEY=your_key
CLOUDINARY_API_SECRET=your_secret
GIPHY_API_KEY=your_key
UNSPLASH_ACCESS_KEY=your_key

# Game Settings
WILD_SPAWNS_ENABLED=true
CARD_CLAIM_COST=100
CARD_PACK_COST=300
GUILD_CREATE_COST=10000

# Server
PORT=5000
NODE_ENV=production
PREFIX=%

# Features
ENABLE_DRAGON_RACING=true
ENABLE_DUNGEON_MODE=true
ENABLE_CATCH_SYSTEM=true
ENABLE_PVP_BATTLES=true
ENABLE_GUILD_SYSTEM=true
```

## 📊 Game Balance

### Dragon Rarities
- **Common** (60%) - Base stats: Speed 50, Power 50, Stamina 50
- **Rare** (25%) - +20% stats: Speed 60, Power 60, Stamina 60
- **Epic** (10%) - +50% stats: Speed 75, Power 75, Stamina 75
- **Legendary** (5%) - +100% stats: Speed 100, Power 100, Stamina 100

### Type Effectiveness Chart
```
Fire    > Metal, Ice       < Water
Water   > Fire, Earth      < Lightning
Earth   > Lightning, Metal < Water, Wind
Wind    > Earth           < Ice
Ice     > Wind, Shadow    < Fire, Metal
Lightning > Water        < Earth, Shadow
Metal   > Ice            < Fire, Earth
Shadow  > Lightning      < Ice
```

### Economy System
- **Daily Reward**: 500 gold
- **Battle Win**: 100-500 gold (depends on difficulty)
- **Guild Treasury**: 1% of all transactions
- **Card Sale**: 50-200 gold per card
- **Starting Gold**: 1,000 gold

## ✅ Features & Status

### Enabled Features
- ✅ Dragon Catching & Training
- ✅ Racing System
- ✅ PvP Battles
- ✅ Dungeon Mode
- ✅ Guild System
- ✅ Card Collecting
- ✅ Economy & Trading
- ✅ Wild Spawns (ENABLED)
- ✅ Owner Commands

### Known Issues Fixed
- ✅ Owner detection with different phone number formats
- ✅ Wild spawns now properly enabled via environment variable
- ✅ Session persistence and authentication
- ✅ Dragon image fetching with fallbacks
- ✅ Battle calculation accuracy
- ✅ Guild permission hierarchy
- ✅ Command cooldown system

## 🛠️ Troubleshooting

### Bot won't connect to WhatsApp
```bash
# Delete session and rescan QR code
rm -rf auth_info_folder
npm start
```

### Commands not working
- Ensure you're using the correct prefix: `%`
- Check command exists: Send `%help`
- Bot must have permission in group

### Wild dragons not spawning
- Confirm `WILD_SPAWNS_ENABLED=true` in `.env` ✅
- Use `%wild on` command in group
- Wait 5 minutes for first spawn

### API errors (image generation failing)
1. Verify API keys are correct in `.env`
2. Check API rate limits
3. Ensure APIs are enabled in provider dashboard

## 📦 Database Files

The bot creates and maintains JSON databases in `./data/`:
- `players.json` - Player accounts and progress
- `dragons.json` - Dragon data
- `guilds.json` - Guild information
- `settings.json` - Game-wide settings
- `blacklist.json` - Banned users list
- `economy.json` - Economy tracking
- `logs.json` - Bot event logs

**Regular backups recommended!**

## 🚀 Deployment Options

### Local Machine
```bash
npm start
```

### Using PM2 (Recommended for Production)
```bash
npm install -g pm2
pm2 start index.js --name dragon-bot
pm2 save
pm2 startup
```

### Docker
```bash
docker build -t dragon-bot .
docker run -d --name dragon-bot dragon-bot
```

### Replit (Free Hosting)
1. Fork repository to Replit
2. Add `.env` secrets in Replit Secrets
3. Click Run
4. Enable "Always On" for 24/7 uptime

## 👑 Bot Owner

**WhatsApp Number**: +26771256815

## 📞 Support & Issues

For bugs, feature requests, or support:
- Create an issue on GitHub
- Contact owner via WhatsApp

## ⚠️ Important Notes

- **Security**: Never commit `.env` to Git (contains API keys)
- **Account**: This bot requires a WhatsApp personal account (not Business Account)
- **Backups**: Regularly backup your `./data` directory
- **Updates**: Keep dependencies updated: `npm update`
- **Rate Limits**: Be aware of API rate limits when using free tiers

## 🎮 Game Rules

### Dragon Catching
- 30% catch rate for wild dragons
- Cooldown: 5 minutes between catches
- Max dragons per player: 6

### Battles
- Battle cooldown: 5 minutes
- Training cooldown: 15 minutes
- Dungeon cooldown: 30 minutes
- Type effectiveness: +50% damage for super effective
- Type resistance: -50% damage for not effective

### Economy
- Max gold limit: 999,999,999
- Guild creation cost: 10,000 gold
- Card pack cost: 300 gold
- Daily reward cooldown: 24 hours

---

**Last Updated**: June 2026  
**Version**: 1.0.0  
**Status**: ✅ Production Ready  
**Stability**: Fully Tested  
**Owner**: +26771256815

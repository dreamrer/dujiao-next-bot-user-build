# TG Bot - Telegram Digital Goods Bot

Telegram digital goods selling bot, powered by Dujiao-Next Channel API.

## Download

Go to [Releases](https://github.com/dreamrer/dujiao-bot-bulid/releases) to download the latest version.

## Quick Start

```bash
# 1. Download & extract
tar -xzf tg-bot-v1.0.0-linux-amd64.tar.gz

# 2. Edit config
cp bot-config.yml.example bot-config.yml
nano bot-config.yml

# 3. Run
chmod +x tg-bot-linux-amd64
./tg-bot-linux-amd64 --config bot-config.yml
```

## Configuration

Edit `bot-config.yml`:

```yaml
license:
  key: "your-license-key"
  auth_server: "https://auth.example.com"

bot:
  token: "your-telegram-bot-token"

channel:
  base_url: "https://your-dujiao-api.com"
  channel_key: "your-channel-key"
  channel_secret: "your-channel-secret"
```

## Docker

```bash
docker compose -f docker-compose.bot.yml up -d
```

# TG Bot - Telegram Digital Goods Bot

Telegram digital goods selling bot, powered by Dujiao-Next Channel API.

## Download

Go to [Releases](https://github.com/dreamrer/dujiao-next-bot-user-build/releases) to download the latest version.

- `tg-bot-linux-amd64.tar.gz` — Linux 64 位（大多数服务器）
- `tg-bot-linux-arm64.tar.gz` — Linux ARM64

## Quick Start

```bash
# 1. 解压
tar -xzf tg-bot-v1.0.0-linux-amd64.tar.gz

# 2. 编辑配置
cp bot-config.yml.example bot-config.yml
nano bot-config.yml

# 3. 运行
chmod +x tg-bot-linux-amd64
./tg-bot-linux-amd64
```

## Configuration

编辑 `bot-config.yml`：

```yaml
# 授权
license:
  key: "your-license-key"
  data_dir: "./data"

# Telegram Bot
bot:
  token: "your-telegram-bot-token"

# Dujiao-Next 对接
channel:
  base_url: "https://your-dujiao-next.com"
  channel_key: "your-channel-key"
  channel_secret: "your-channel-secret"

# 通知回调（推荐开启）
notify:
  listen: ":8444"
```

## Docker

```bash
docker compose -f docker-compose.bot.yml up -d
```

## Documentation

解压后包含完整部署教程 `DEPLOY.md`，涵盖：

- 创建 Telegram Bot
- 独角后台配置（Bot 客户端、菜单、帮助中心）
- 直接运行 / Docker / systemd / 宝塔部署
- 通知回调配置
- Webhook 模式（可选）
- 常见问题排查

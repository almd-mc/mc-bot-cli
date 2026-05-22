# mc-bot-cli

CLI for the Almide Minecraft bot.

## Usage

```bash
mc-bot-cli [host] [port]
mc-bot-cli --help
```

Defaults to `localhost:25565`. On first run, opens Microsoft device code auth in browser. Token is cached for subsequent runs.

## Build

```bash
almide build src/mod.almd -o mc-bot
```

## Performance

- Startup: 13ms
- Crypto (SHA-1 + AES): <1ms (hardware-accelerated via AES-NI)
- Login → Play: ~4s (dominated by Mojang API latency)

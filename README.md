<p align="center"><img src="https://raw.githubusercontent.com/akilibots/.github/main/assets/akilibots-icon.svg" width="144" alt="Akilibots"></p>

# Welcome to akilibots-strategies!

[![Python 3.15.2](https://img.shields.io/badge/Python-3.15.2-6966FF?logo=python&logoColor=white)](https://www.python.org/downloads/)
[![Telegram](https://img.shields.io/badge/Telegram-community-6966FF?logo=telegram&logoColor=white)](https://t.me/+9F0CZj8emLc2YTY0)

> **Updated 22 November 2026:** configuration guidance now matches the dYdX Chain and Binance Spot bots, with Python 3.15.2 Docker runtimes.

Jambo! This is the place to share that extra tweak. **akilibots-strategies** is
for community configuration examples for the [Akilibots](https://github.com/akilibots)
family. No strategy files or backtesting engine are included yet.

## Pick your bot

| Bot | What you configure |
| --- | --- |
| [Grid](https://github.com/akilibots/akili-grid) | Bounds, spacing and orders above and below the centre |
| [Martingale](https://github.com/akilibots/akili-martingale) | Averaging entries, quantities and take-profit targets |
| [OTO](https://github.com/akilibots/akili-oto) | Order groups, successor groups and loops |
| [DCA](https://github.com/akilibots/akili-dca) | A fixed quantity and interval |
| [TradingView](https://github.com/akilibots/akili-tradingview) | Alerts that trigger authenticated order requests |
| [Binance grid](https://github.com/akilibots/akili-binance-grid) | A Spot market, grid spacing and inventory quantity |

## Use a configuration

1. Clone the matching bot and start with its supplied example.
2. For a dYdX bot, edit `data/strategy.json` and configure the Chain wallet in
   `.env`. The Binance bot uses environment variables instead.
3. Follow that bot's README for Docker setup and offline regression tests.
4. Check the market, quantity units and order sequence before running it.

Configurations belong to a particular bot. Do not copy one into another bot
without checking its fields. Legacy v3 credentials and state are incompatible
with the Chain versions.

## Share your own

Send a [pull request](https://github.com/akilibots/akilibots-strategies/pulls) or
open an [issue](https://github.com/akilibots/akilibots-strategies/issues/new).
Include the bot, market, network, quantity units and an explanation of what should
happen when an order fills. Leave out wallet mnemonics, API keys, webhook secrets
and runtime state.

The bots' Docker tests verify program behaviour. They do not measure historical
strategy returns, and this repository does not supply a backtesting system.

## The usual bit

This software is for educational purposes only. Do not risk money you are afraid
to lose. **USE THE SOFTWARE AT YOUR OWN RISK. THE AUTHORS AND ALL AFFILIATES ASSUME
NO RESPONSIBILITY FOR YOUR TRADING RESULTS.**

See [LICENSE](LICENSE) for the full terms.

Come say jambo in [Telegram](https://t.me/+9F0CZj8emLc2YTY0).

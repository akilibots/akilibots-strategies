# Akilibots strategies

A repository for contributed configuration examples for
[Akilibots](https://github.com/akilibots). No strategy files or backtest engine
are currently included here.

The bots are independent Python applications:

- [Grid](https://github.com/akilibots/akili-grid): moving orders on a bounded grid.
- [Martingale](https://github.com/akilibots/akili-martingale): explicit averaging entries and weighted take profit.
- [OTO](https://github.com/akilibots/akili-oto): conditional order groups and loops.
- [DCA](https://github.com/akilibots/akili-dca): fixed-quantity interval execution.
- [TradingView](https://github.com/akilibots/akili-tradingview): authenticated webhook-driven orders.
- [Binance grid](https://github.com/akilibots/akili-binance-grid): a moving two-order Spot grid.

The dYdX bots now target dYdX Chain. v3 credentials and state are incompatible.
The Binance bot uses the supported modular Spot SDK and a configurable symbol.
Docker runtimes use Python 3.15.2.

## Using a configuration

Start from the configuration shipped with the matching bot. For dYdX bots, edit
`data/strategy.json` and set wallet credentials in `.env`, following that bot's
README. The Binance grid is configured through environment variables. Do not copy
one bot's configuration into a different bot without checking its schema.

## Contributing

Submit configuration examples by pull request. Include the bot, network, market,
quantity units and an explanation of the order sequence. Keep wallet mnemonics,
API keys, webhook secrets and runtime state out of contributions.

Each executable bot contains Docker regression tests using simulated exchanges.
These verify program behaviour, not historical strategy returns. Evaluate market
behaviour separately; there is no supplied backtesting system.

Software and examples are supplied as is under the repository licence.

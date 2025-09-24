BTC Liquidation Heatmap (Binance + Discord Alerts)

This project provides a Jupyter Notebook that generates BTCUSDT liquidation-style heatmaps using Binance market data.
It analyzes wick intensity, volume, EMA crossovers, and proximity to price, then highlights high-liquidity zones.
The script also demonstrates how to send annotated charts and top liquidity levels to a Discord channel.

Features

Fetches historical candlestick (OHLCV) data for BTCUSDT from Binance

Calculates liquidation intensity (wick size × volume)

Detects Golden Cross / Death Cross events near liquidity spikes

Scores and ranks liquidity levels by strength, volume, and proximity to price

Generates annotated charts with:

Price candles and EMAs (50 & 200)

Volume histogram

Highlighted liquidity levels

Optionally posts charts and liquidity levels directly to Discord

Requirements

Install dependencies before running the notebook:

pip install -r requirements.txt


requirements.txt should include:

binance
pandas
matplotlib
numpy
requests

Setup

Get Binance API keys from Binance
.

Create a Discord webhook (Server Settings → Integrations → Webhooks).

Update the notebook with your keys:

api_key = "your_api_key"
api_secret = "your_api_secret"
DISCORD_WEBHOOK = "your_discord_webhook_url"

Usage

Open the notebook in Jupyter or VS Code.

Run all cells.

The notebook will:

Fetch BTCUSDT data

Generate heatmaps for multiple timeframes (1m, 5m, 15m, 1h)

Optionally post results to Discord every 15 minutes

Example Output

Top levels (price | volume | score):

63120.50 | vol 4500 | score 0.82 | Golden Cross
63580.00 | vol 3900 | score 0.67
62940.25 | vol 3700 | score 0.60 | Death Cross


Example chart:

Disclaimer

This tool is for educational and research purposes only.
It does not provide financial advice. Use at your own risk.

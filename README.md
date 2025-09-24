# BTC Liquidation Heatmap (Binance + Discord Alerts)

This project provides a Jupyter Notebook that generates **BTCUSDT liquidation-style heatmaps** using Binance market data.  
It analyzes wick intensity, volume, EMA crossovers, and proximity to price, then highlights high-liquidity zones.  
The script also demonstrates how to send annotated charts and top liquidity levels to a Discord channel.

---

## Features
- Fetches historical candlestick (OHLCV) data for BTCUSDT from Binance  
- Calculates liquidation intensity (wick size × volume)  
- Detects Golden Cross / Death Cross events near liquidity spikes  
- Scores and ranks liquidity levels by strength, volume, and proximity to price  
- Generates annotated charts with:  
  - Price candles and EMAs (50 & 200)  
  - Volume histogram  
  - Highlighted liquidity levels  
- Optionally posts charts and liquidity levels directly to Discord

---

## Requirements
Install dependencies before running the notebook:  

```bash
pip install -r requirements.txt


## Example Chart
![BTC Heatmap Example]
<img width="1500" height="800" alt="BTCUSDT_1h_heatmap" src="https://github.com/user-attachments/assets/8dfa35e7-a52e-4723-a9b6-3017c44a6a78" />

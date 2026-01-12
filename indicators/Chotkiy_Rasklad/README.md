# Chotkiy Rasklad

![License: MPL 2.0](https://img.shields.io/badge/License-MPL%202.0-brightgreen.svg)
![Language: Pine Script](https://img.shields.io/badge/Language-Pine%20Script%20v6-blue.svg)

**Chotkiy Rasklad** is a comprehensive Multi-Timeframe (MTF) trend scanner and strategy indicator for TradingView. It combines Heikin Ashi candle analysis, classical trend filters (SMA, EMA, VWAP), and momentum indicators (HARSI) to provide high-probability entry and exit signals.

Designed to filter out market noise and identify strong trend alignments across multiple timeframes (from 1 minute to Daily).

---
![Dashboard Preview](scr2.png)
---

## 🚀 Features

* **Multi-Timeframe Dashboard:** A customizable on-screen dashboard monitoring trends across 6 timeframes simultaneously (1m, 5m, 15m, 1h, 4h, 1D).
* **Trend Confluence System:** Checks for alignment between:
    * Heikin Ashi Candle structure (3-candle sequence).
    * Simple Moving Average (SMA 200).
    * Exponential Moving Average (EMA 200).
    * VWAP (Volume Weighted Average Price).
* **Momentum Filtering:** Uses HARSI (Heikin Ashi RSI) to validate trend strength.
* **Session Filtering:** Highlights signals occurring during specific trading sessions (Morning/Evening) to avoid low-volatility "choppiness."
* **Visual & Audio Alerts:**
    * Chart labels for Entries (Long/Short) and Exits.
    * Configurable alerts for automated trading or notifications.

## 📊 Strategy Logic

The indicator generates signals based on a strict confluence of factors:

### Bullish Signal (Long)
1.  **Candle Structure:** 3 consecutive Green Heikin Ashi candles with consecutive Higher Lows.
2.  **Trend Filters:** Price is **above** SMA 200, EMA 200, and VWAP.
3.  **Momentum:** HARSI (RSI based) is > 50.

### Bearish Signal (Short)
1.  **Candle Structure:** 3 consecutive Red Heikin Ashi candles with consecutive Lower Highs.
2.  **Trend Filters:** Price is **below** SMA 200, EMA 200, and VWAP.
3.  **Momentum:** HARSI (RSI based) is < 50.

---

## ⚙️ Configuration

You can customize the indicator settings via the TradingView inputs menu:

### Global Filters
* **SMA Length:** Length of the Simple Moving Average (Default: 200).
* **EMA Length:** Length of the Exponential Moving Average (Default: 200).

### HARSI Settings
* **RSI Length / Smoothing:** Adjust sensitivity of the momentum filter.

### Time Settings
* Define your specific session times (Opening, Morning, Evening) to color-code signals based on market activity.

### Dashboard
* **Show Dashboard:** Toggle the MTF table on/off.
* **Size:** Change table size (Tiny, Small, Normal).
* **Offset:** Adjust the vertical and horizontal position of the dashboard on your chart.

---

## 📥 Installation

1.  Copy the code from the `.pine` file in this repository.
2.  Open **TradingView**.
3.  Click on **Pine Editor** at the bottom of the screen.
4.  Paste the code and click **Save**.
5.  Click **Add to Chart**.

## ⚠️ Disclaimer

This tool is for educational and informational purposes only. It does not constitute financial advice. Trading financial markets involves risk, and past performance is not indicative of future results. Always manage your risk appropriately.

## 📄 License

This project is licensed under the **Mozilla Public License 2.0**.  
See the [LICENSE](LICENSE) file for details.

---

**© 2026 Sergei Seivach**
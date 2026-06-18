---
title: Opening a Trade
parent: Perpetuals Trading
nav_order: 2
---

# Opening a Perpetuals Trade

SureSwap lets you go long or short on any Hyperliquid market directly from Telegram.

---

## How to open a trade

1. From the dashboard tap **Perps Trading**
2. Browse the market list or tap **🔍 Search Ticker** and type a symbol (e.g. `BTC`, `ETH`, `SOL`)
3. Select the market
4. Choose **Long** or **Short**
5. Select your leverage (e.g. 5×, 10×, 20×)
6. Enter your USDC notional size — this is the dollar value of your position *before* leverage

### Trade preview

Before confirming, a **live preview card** is shown with:

- Position size (notional × leverage)
- Entry price (current mid-market)
- Estimated liquidation price
- Fees

The preview **auto-refreshes every 30 seconds** while you're reviewing, so the figures stay current.

You can also adjust your size using **presets** (configurable percentage buttons). To edit your presets, tap **Edit Presets** and enter values as a comma-separated list (e.g. `25,75,200,500,2000`).

7. Tap **Confirm Trade** to execute

---

## Setting TP / SL

Immediately after opening a trade (or from an existing position), you can set:

- **Take Profit (TP)** — the price at which your position automatically closes in profit
- **Stop Loss (SL)** — the price at which your position automatically closes to limit loss

You can set one or both. The bot provides preset percentage buttons (e.g. +5%, +10%, -3%, -5%) relative to your entry price, or you can type an exact price.

---

## Closing a position

From the **Perps Trading** menu, select your open position and tap **Close Position**. You'll see a confirmation with the current P&L before the close executes.

---

## Managing positions

Open positions are shown in the Perps dashboard with:

- Current mark price
- Unrealised P&L
- Liquidation price
- Current TP/SL levels (if set)

---

## Risk warning

{: .warning }
Perpetual futures are leveraged products. You can lose more than your initial margin. Only trade with funds you can afford to lose. Hyperliquid positions are subject to funding rates which may be positive or negative.

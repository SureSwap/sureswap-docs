---
title: Creating a Limit Order
parent: Limit Orders
nav_order: 1
---

# Creating a Limit Order

Limit orders execute a swap automatically when a token's price crosses your target. You set the terms once — SureSwap does the rest.

---

## How to create a limit order

From the dashboard tap **Limit Orders** → **New Order**.

### Step 1: Choose side

Select whether you want to **Buy** or **Sell**.

### Step 2: Select source chain and token

Pick the chain you'll be spending from, then select the token you want to spend (the "sell" leg of your order).

### Step 3: Select destination chain and token

Pick where you want the output to land, then select the token you want to receive (the "buy" leg).

Cross-chain limit orders are fully supported — you can trigger a Solana → Base swap from a Solana price condition, for example.

### Step 4: Enter amount

Type how much of the source token to spend when the order triggers.

### Step 5: Set target price

Enter the price at which you want the order to execute. Prices are denominated in the destination token per unit of source token.

### Step 6: Set condition

Choose when the order should trigger:

| Condition | Meaning |
|-----------|---------|
| **Price rises above target** | Order fires when market price ≥ your target (good for selling into strength, or buying a breakout) |
| **Price falls below target** | Order fires when market price ≤ your target (classic limit buy at a dip, or stop-loss sell) |

### Step 7: Review and confirm

A summary shows your full order: which tokens, the amount, the target price, and the condition. Tap **Confirm** to place it.

---

## Viewing active orders

Tap **Limit Orders** from the dashboard to see all your active orders, their status, and the current price vs target.

---

## Cancelling an order

Tap the order from the list → **Cancel Order**. Your funds are returned to your wallet immediately — nothing is locked while an order is pending.

---

## How execution works

SureSwap runs a background price monitor. When the market price crosses your target:

1. The bot fetches a live quote for your order
2. If the quote is within acceptable slippage, the swap executes automatically
3. You receive a Telegram notification confirming the fill

{: .note }
Execution is not guaranteed if the market moves rapidly through your target price or if there is insufficient liquidity at the time of execution. In that case the order remains open and will try again on the next price check.

---

## Fees

Limit orders use the same swap routing as regular swaps — fees are the standard protocol and bridge fees for your chosen route. There is no additional fee for placing or holding a limit order.

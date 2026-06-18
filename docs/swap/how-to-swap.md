---
title: How to Swap
parent: Swapping
nav_order: 1
---

# How to Swap

Swaps let you exchange one token for another — either on the same chain, or across different chains in one step.

---

## Starting a swap

From the dashboard, tap **Swapping** → **Unified Swap / Buy**.

---

## Step-by-step

### 1. Select the token you want to sell

You'll see a paginated list of all tokens in your wallet. Tap the one you want to spend.

### 2. Select the token you want to buy

You'll see a menu of popular tokens. You can also:

- **Paste a contract address** — type any EVM `0x…` or Solana Base58 mint address. If the token exists on multiple chains, you'll be asked to pick the destination chain.
- **Natives** — tap to see the native gas tokens (ETH, SOL, BNB, etc.) across chains.
- **Multi-chain tokens** (e.g. ETH, USDC) — a chain picker is shown so you choose exactly where the output lands.

### 3. Enter the amount

Type the amount of your source token to sell. Tap **Max** to use your full available balance.

### 4. Review and confirm

The quote screen shows:

- **Expected output** — how much of the destination token you'll receive
- **Price impact** — how much your trade moves the market (highlighted in red if significant)
- **Route** — which DEXs or bridges are used
- **Fees** — protocol and gas fees

Tap **Confirm Swap** to execute, or **Cancel** to go back.

---

## Same-chain vs cross-chain swaps

| Type | How it works |
|------|-------------|
| **Same-chain** | Swapped instantly on a single DEX/aggregator (Jupiter on Solana, 0x aggregation on EVM) |
| **Cross-chain** | Routed through a bridge (Mayan, Relay, or LayerZero) in a single transaction from your side — the bridge handles the cross-chain transfer |
| **Consolidated** | If you hold the same token on multiple chains, SureSwap can consolidate them into a single balance before swapping |

---

## Privacy Mode swaps

When **Privacy Mode** is enabled, the swap flow changes:

- Your source funds are drawn from the shared **Privacy Pool** instead of your personal wallet
- The output is delivered to the Pool, not to your on-chain address
- To access your output, [withdraw from the Privacy Pool](../privacy-mode/withdrawing)

See [Privacy Mode](../privacy-mode/) for a full explanation of how this works.

---

## Supported swap routes

| Source | Destination | Provider |
|--------|-------------|----------|
| Solana token | Solana token | Jupiter |
| EVM token | EVM token (same chain) | 0x / DEX aggregation |
| EVM → Solana | Any | Mayan, Relay |
| Solana → EVM | Any | Mayan, Relay |
| EVM → EVM (cross-chain) | Any | Mayan, Relay, LayerZero |

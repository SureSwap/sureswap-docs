---
title: Bridging
nav_order: 5
has_children: true
---

# Bridging Assets

Bridging moves assets from one network to another **without swapping** — you keep the same token, just on a different chain.

---

## When to bridge vs swap

- **Bridge** when you want to move USDC from Base to Arbitrum without changing the asset
- **Swap** when you also want to change the token (e.g. ETH on Ethereum → SOL on Solana) — SureSwap handles this as a cross-chain swap in one step

---

## How to bridge

1. From the dashboard tap **Swapping** (the bridge is accessed from the swap menu)
2. Select **Bridge** to begin a pure bridge (no token change)
3. Select your source token
4. Select the destination chain
5. Enter the amount
6. Review and confirm

---

## Bridge providers

SureSwap routes bridge transactions through the most favourable provider:

| Provider | Best for |
|----------|----------|
| **Mayan** | EVM ↔ Solana, fast finality |
| **Relay** | EVM ↔ EVM, low fees |
| **LayerZero** | Wide chain coverage including Abstract, Plasma |

You don't need to select a provider manually — SureSwap picks the best route automatically.

---

## Supported bridge routes

All chains in the [Supported Networks](../supported-networks/) table can bridge to each other, subject to liquidity. Cross-chain routes that aren't directly supported by one provider may be routed through an intermediate step automatically.

{: .note }
Bridge transactions are not instant. Depending on the source chain's finality and the provider, transfers can take anywhere from 30 seconds to a few minutes.

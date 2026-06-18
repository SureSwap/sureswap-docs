---
title: Wrap / Unwrap
parent: Your Wallet
nav_order: 4
---

# Wrapping and Unwrapping Tokens

Some DeFi protocols and bridges require the **wrapped** version of a native asset (e.g. WETH instead of ETH). SureSwap lets you wrap and unwrap in a single tap.

---

## How to wrap

1. From the dashboard tap **Tools** → **Wrap Native**
2. Select the chain you want to wrap on
3. Enter the amount of native asset to wrap
4. Review and confirm

Your native token (e.g. ETH) is deposited into the WETH contract and you receive an equivalent amount of WETH in return.

---

## How to unwrap

1. From the dashboard tap **Tools** → **Unwrap Native**
2. Select the chain and amount
3. Review and confirm

Your wrapped token is burned and you receive native ETH/BNB/etc. back.

---

## Supported wrap pairs

| Chain | Wrap | Unwrap |
|-------|------|--------|
| Ethereum | ETH → WETH | WETH → ETH |
| Base | ETH → WETH | WETH → ETH |
| BSC | BNB → WBNB | WBNB → BNB |
| Arbitrum | ETH → WETH | WETH → ETH |
| HyperEVM | HYPE → WHYPE | WHYPE → HYPE |

{: .note }
Wrap/Unwrap is currently available on EVM chains only. Solana uses native SOL wrapping transparently during swaps — you don't need to manually wrap SOL before swapping.

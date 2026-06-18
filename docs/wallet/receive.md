---
title: Receiving Tokens
parent: Your Wallet
nav_order: 1
---

# Receiving Tokens

Your addresses are displayed on the **SureSwap Dashboard** — the main screen you see each time you open the bot.

---

## Your addresses

| Network | Address format | Shown on dashboard |
|---------|---------------|-------------------|
| All EVM chains | `0x…` (40 hex chars) | ✓ |
| Solana | Base58 string | ✓ |
| TON | `UQ…` (friendly, non-bounceable) | ✓ |
| Tron | `T…` (Base58Check) | ✓ |

{: .note }
Your EVM address works on **every** EVM chain simultaneously — Ethereum, Base, BSC, Arbitrum, HyperEVM, Plasma, and Abstract all share the same `0x…` address.

---

## Receiving on EVM chains

Send any ERC-20 token or native ETH/BNB/etc. to your displayed `0x…` address on the correct network. SureSwap will detect the incoming balance the next time you open your token list.

{: .tip }
If you've received a token that isn't showing in your list, use **Import Token** to add it manually. See [Importing Tokens](./import-token).

---

## Receiving on Solana

Send SOL, USDC, or any SPL / Token-2022 token to your Solana address. The bot will display balances when you open the token list.

---

## Receiving on TON

Send native TON or any Jetton to your `UQ…` address. The bot always displays the non-bounceable (UQ) form to prevent accidental bounces when receiving from centralised exchanges.

---

## Receiving on Tron

Send native TRX or any TRC-20 token to your `T…` address.

---

## Token list

Tap **Token List** from the dashboard to see all balances across all chains. Balances are fetched live each time you view the list.

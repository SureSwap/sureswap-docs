---
title: Withdrawing from the Pool
parent: Privacy Mode
nav_order: 2
---

# Withdrawing from the Privacy Pool

Withdrawing moves USDC from the shared privacy pool to any address you choose — your own wallet, a fresh address, or a centralised exchange deposit address.

---

## How to withdraw

1. From the dashboard tap **Swapping** → **Withdraw from Pool**
2. Enter the USDC amount you want to withdraw
3. Choose a destination:
   - **My SureSwap Wallet** — sends to your own EVM or Solana address within SureSwap
   - **Custom Address** — paste any destination address on any supported chain
4. If you enter an EVM address, select which chain you want to receive on
5. Review the confirmation screen and tap **Confirm**

---

## Destination options

### My SureSwap Wallet

The fastest option. USDC lands in your personal on-chain wallet address — note that this creates an on-chain link between the pool and your SureSwap wallet.

### Custom Address

Paste any address:
- **Solana address** — USDC is sent on Solana (auto-detected from the Base58 format)
- **EVM address** — you'll be asked which EVM chain to receive on

For the strongest privacy, withdraw to a **fresh address** that has never been used before.

---

## Cross-chain withdrawals

You can withdraw from the pool's Solana balance to an EVM chain, or from an EVM chain pool to Solana or another EVM chain. SureSwap uses **CCTP (Circle's Cross-Chain Transfer Protocol)** to move USDC cross-chain during withdrawals.

Cross-chain withdrawals take slightly longer than same-chain withdrawals — typically 1–3 minutes for CCTP to settle.

---

## Fees

Privacy Mode withdrawals incur the standard CCTP bridging fee when crossing chains. Same-chain withdrawals have minimal fees (standard gas cost).

---

## Balance after withdrawal

Your pool balance is reduced by the withdrawn amount. If you withdraw more than your balance, the transaction will be rejected.

{: .warning }
Do not attempt to withdraw your full balance and re-deposit immediately in a tight loop — the pool holds real on-chain USDC and the sweeper needs a small amount of time to reconcile balances.

---
title: Depositing into the Pool
parent: Privacy Mode
nav_order: 1
---

# Depositing into the Privacy Pool

There are two ways to put funds into your Privacy Mode balance:

1. **External deposit** — send funds from outside SureSwap to a one-time address
2. **Internal deposit** — move USDC from your own SureSwap wallet into the pool

---

## External deposit (recommended for privacy)

This method breaks the on-chain link most effectively because the deposit address is freshly generated and used exactly once.

### How it works

1. From the dashboard tap **Swapping** → **Deposit to Pool**
2. Select the chain you'll be sending from (Solana, Ethereum, Base, BSC, or Arbitrum)
3. SureSwap generates a **one-time disposable deposit address** backed by a Vault key
4. Send USDC (or the chain's native token) to that address from anywhere — your exchange, another wallet, a friend
5. The bot detects the incoming funds automatically and sweeps them into the privacy pool

{: .tip }
For maximum privacy, send funds from an address that has no prior connection to your main wallet — for example, funds withdrawn from a centralised exchange directly to the deposit address.

### What happens to the deposit address

The disposable address is **single-use**. After funds are swept:
- The address is marked as completed in the database
- The Vault key remains stored but the address is retired
- Your pool balance is credited

You can generate a new address for each deposit — there is no limit on the number of deposit addresses.

### Supported chains for external deposit

| Chain | Accepted tokens |
|-------|----------------|
| Solana | USDC, SOL, any SPL token |
| Ethereum | USDC |
| Base | USDC |
| BSC | USDC |
| Arbitrum | USDC |

Non-USDC tokens (e.g. native SOL or ETH) are automatically swapped to USDC upon sweeping before being added to your pool balance.

---

## Internal deposit

This moves USDC from your own SureSwap wallet (your personal on-chain balance) directly into the pool.

{: .note }
Internal deposits do not break the on-chain link between your personal wallet and the pool — they are visible on-chain. Use external deposits for maximum privacy.

### How to make an internal deposit

1. From the dashboard tap **Swapping** → **Deposit to Pool**
2. Select **Deposit from my wallet**
3. Choose which chain's USDC balance to move
4. Enter the amount
5. Confirm

Your USDC is sent from your personal wallet address to the omnibus pool on that chain.

---

## Checking your pool balance

Tap **Privacy Dashboard** from the dashboard to see your current pool balance broken down by chain, along with recent deposit and withdrawal history.

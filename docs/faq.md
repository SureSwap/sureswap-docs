---
title: FAQ
nav_order: 11
---

# Frequently Asked Questions

---

## General

### Do I need a seed phrase?

No. SureSwap uses HashiCorp Vault to generate and store your keys server-side. There is no seed phrase to write down. Your Telegram account is your authentication factor.

### What if I lose access to my Telegram account?

Contact SureSwap support as soon as possible. Since authentication is tied to your Telegram account, recovery requires verifying your identity through the support process. This is why protecting your Telegram account with 2FA is strongly recommended.

### Is SureSwap non-custodial?

For standard wallet operations — sending, receiving, swapping — your keys are held in HashiCorp Vault and only used to sign transactions you authorise. The keys are never exported.

Privacy Mode is an exception: funds in the Privacy Pool are held in a shared omnibus wallet operated by SureSwap. See [Privacy Mode](./privacy-mode/) for details.

### Can I import an existing wallet?

Yes. Tap **Tools** → **Import** to import an existing private key. Imported wallets are stored in Vault in the same way as generated ones.

---

## Swapping

### Why do I see "price impact" warnings?

Price impact reflects how much your trade moves the market price of a token. High impact (> 2–3%) means you're trading a large size relative to available liquidity and you may get a worse rate than displayed. Consider splitting large trades.

### My swap failed — what happened?

Common reasons:
- **Slippage exceeded**: The price moved between the time you confirmed and when the transaction hit the chain. Try again with a slightly wider slippage tolerance.
- **Insufficient gas**: Rare on EVM chains since SureSwap covers gas, but possible on Solana if your SOL balance is very low.
- **Bridge timeout**: Cross-chain swaps have a timeout window. If the bridge provider doesn't fill within the window, funds are returned automatically.

### How long do cross-chain swaps take?

| Route | Typical time |
|-------|-------------|
| EVM → EVM (same provider) | 30 seconds – 2 minutes |
| EVM → Solana (Mayan) | 1 – 3 minutes |
| Solana → EVM (Mayan) | 1 – 3 minutes |
| CCTP cross-chain | 1 – 3 minutes |

---

## Privacy Mode

### Is Privacy Mode completely anonymous?

Privacy Mode significantly reduces on-chain traceability but is not a guarantee of complete anonymity. SureSwap knows which deposits and withdrawals are yours (we operate the pool). On-chain, your deposit address is a single-use address with no history, and withdrawals come from the shared pool — but timing correlation attacks are still theoretically possible for a sophisticated observer.

### Can I withdraw to a centralised exchange from Privacy Mode?

Yes. On the withdrawal screen, paste your exchange deposit address and select the matching chain. SureSwap will send USDC directly there.

### What tokens can I deposit?

Currently only USDC is counted as Privacy Pool balance. If you deposit other tokens (e.g. native SOL or ETH), they are automatically swapped to USDC before being added to your balance. The swap happens inside the sweeper before your balance is credited.

---

## Perps

### Which exchange powers perps?

Hyperliquid — a decentralised perpetuals exchange settled on its own L1.

### Do I need a Hyperliquid account?

No separate account creation is needed. SureSwap manages the Hyperliquid account associated with your wallet address automatically.

### What is the minimum trade size?

This depends on Hyperliquid's per-market minimum notional. Typically $10 USDC or more.

---

## Profiles

### Do profiles share a balance?

No. Each profile has entirely separate addresses and on-chain balances. Switching profiles does not combine or share funds.

### What happens to funds on an archived profile?

Nothing — they stay on-chain at those addresses. The profile is just hidden from your active list. Restore the profile to access those funds again.

---

## Security

### How are my keys protected?

Keys live inside a HashiCorp Vault server. All signing happens inside Vault using the Transit secrets engine — the raw key material is never exposed to SureSwap's application code.

### What is the "gasless" EVM mechanism?

On EVM chains, SureSwap uses EIP-7702 delegation. Your wallet authorises a SureSwap delegate contract to execute transactions on your behalf. This means you don't need to hold ETH for gas — SureSwap sponsors the gas. You retain full control: only signed transactions from you can instruct the delegate to act.

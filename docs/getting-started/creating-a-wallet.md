---
title: Creating a Wallet
parent: Getting Started
nav_order: 1
---

# Creating a Unified Wallet

When you first open SureSwap, you'll be greeted with a welcome message and a single button: **Create Unified Wallet**. Tap it, and within a few seconds you have a fully functional multichain wallet.

---

## What happens when you create a wallet

SureSwap generates **three independent cryptographic keys** for you, all stored securely inside a HashiCorp Vault server — your private keys never leave the server in raw form.

| Key type | Chains it covers |
|----------|-----------------|
| **secp256k1 (EVM)** | Ethereum, Base, BSC, Arbitrum, HyperEVM, Plasma, Abstract, and all future EVM chains |
| **ed25519 (Solana)** | Solana — also re-used to derive your TON address |
| *(EVM key re-used)* | Tron — derived from the same secp256k1 key as EVM |

### Addresses you get

After creation, your dashboard shows:

- **EVM Address** — one `0x…` address valid on every EVM network
- **Solana Address** — your Base58 Solana public key
- **TON Address** — a `UQ…` v4R2 wallet address, derived from your Solana ed25519 key
- **Tron Address** — a `T…` Base58Check address, derived from your EVM secp256k1 key

{: .note }
Because your TON and Tron addresses are **derived** (not independently generated), you only ever need to back up two keys — your EVM key and your Solana key. All four addresses are recoverable from those two.

---

## Profiles

Every wallet starts with a **"Default" profile**. Profiles let you maintain multiple isolated wallets under a single Telegram account — useful for separating trading funds, holding different portfolios, or keeping a clean wallet for DeFi.

You can create up to **10 active profiles** and switch between them at any time. See [Profiles](../wallet/profiles) for more.

---

## Key security

- Keys are generated **inside HashiCorp Vault** and never exported
- All signing operations happen server-side using the Vault Transit engine
- Your Telegram account is the authentication factor — no seed phrases, no password to lose
- Keys are isolated per-profile so a compromised profile doesn't affect the others

{: .warning }
SureSwap does **not** give you a seed phrase. Access is tied to your Telegram account. If you lose access to your Telegram account, contact support immediately.

---

## Next steps

- [Receiving tokens](../wallet/receive) — find your addresses and QR codes
- [Sending tokens](../wallet/send) — transfer to any address on any supported chain
- [Swapping](../swap/) — swap tokens same-chain or cross-chain

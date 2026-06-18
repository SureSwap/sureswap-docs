---
title: Importing Tokens
parent: Your Wallet
nav_order: 3
---

# Importing Tokens

SureSwap only shows tokens you've explicitly added to your list. If you've received a token that isn't appearing, import it by pasting the contract address.

---

## How to import

1. From the dashboard tap **Tools** → **Import Token**
2. Paste the token contract address
3. The bot fetches the token name, symbol, and decimals automatically
4. Confirm to add it to your list

---

## Address formats by chain

| Chain | Format | Example |
|-------|--------|---------|
| EVM (any) | `0x…` 40-character hex | `0xA0b86991c6218b36c1d19D4...` |
| Solana | Base58 mint address | `EPjFWdd5AufqSSqeM2qN1xzybapC8G4wEGGkZwyTDt1v` |
| TON | `EQ…` or `UQ…` Jetton master | `EQB-MPwrd1G6WKNkLz_VnV6Wj...` |
| Tron | `T…` 34-character Base58 | `TR7NHqjeKQxGTCi8q8ZY4pL8otSzgjLj6t` |

---

## What gets fetched automatically

### EVM tokens
- Token name and symbol (from the ERC-20 `name()` / `symbol()` calls)
- Decimal places
- Current balance

### Solana tokens
- Name and symbol from on-chain metadata (Metaplex standard) or Token-2022 extensions
- Decimal places
- Current balance

### TON Jettons
- Jetton metadata (name, symbol) from the Jetton master contract
- If metadata isn't available on-chain, the symbol falls back to `JETTON`

### Tron TRC-20
- Name and symbol from the TRC-20 contract
- Decimal places and current balance

---

## Token list management

Once imported, tokens appear in your **Token List** and are available to select in Send, Swap, and Limit Order flows.

{: .tip }
Tokens are stored per-profile. If you switch profiles, you'll need to import your tokens again on the new profile.

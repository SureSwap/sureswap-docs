---
title: Supported Networks
nav_order: 10
---

# Supported Networks

SureSwap supports the following networks. Your EVM address is valid on all EVM chains simultaneously — you don't need a separate address per chain.

---

## Full support

These chains support the complete feature set.

| Network | Type | Send | Receive | Swap | Bridge | Privacy Mode |
|---------|------|:----:|:-------:|:----:|:------:|:------------:|
| **Solana** | Solana | ✓ | ✓ | ✓ | ✓ | ✓ |
| **Ethereum** | EVM | ✓ | ✓ | ✓ | ✓ | ✓ |
| **Base** | EVM | ✓ | ✓ | ✓ | ✓ | ✓ |
| **BSC** | EVM | ✓ | ✓ | ✓ | ✓ | ✓ |
| **Arbitrum** | EVM | ✓ | ✓ | ✓ | ✓ | ✓ |
| **Optimism** | EVM | ✓ | ✓ | ✓ | ✓ | — |
| **Unichain** | EVM | ✓ | ✓ | ✓ | ✓ | — |
| **HyperEVM** | EVM | ✓ | ✓ | ✓ | ✓ | — |
| **Plasma** | EVM | ✓ | ✓ | ✓ | ✓ | — |
| **Abstract** | EVM | ✓ | ✓ | ✓ | ✓ | — |

**Arbitrum** is also used for Hyperliquid Perps funding.

---

## Send / Receive only

Full swap and bridge support is coming soon for these networks.

| Network | Type | Send | Receive | Swap | Bridge |
|---------|------|:----:|:-------:|:----:|:------:|
| **TON** | TON | ✓ | ✓ | Coming soon | Coming soon |
| **Tron** | Tron | ✓ | ✓ | Coming soon | Coming soon |

---

## Notes

- **EVM address**: one `0x…` address works on Ethereum, Base, BSC, Arbitrum, Optimism, Unichain, HyperEVM, Plasma, and Abstract
- **Gas**: EVM transactions are gasless — SureSwap covers gas fees on all EVM chains
- **CCTP**: Privacy Mode cross-chain withdrawals use Circle's CCTP, which supports Ethereum, Base, BSC, Arbitrum, and Solana

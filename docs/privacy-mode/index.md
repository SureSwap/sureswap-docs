---
title: Privacy Mode
nav_order: 7
has_children: true
---

# Privacy Mode

Privacy Mode routes your swaps through a shared liquidity pool — breaking the on-chain link between your incoming funds and your outgoing tokens.

When you use Privacy Mode, an observer watching the blockchain cannot easily connect a deposit to a withdrawal, because many users' funds are pooled together and swaps are executed from the pool's shared balance rather than your personal wallet.

---

## How it works at a high level

```
You deposit USDC → Shared Pool → Pool executes your swap → You withdraw output
```

The key insight: many users deposit into and withdraw from the same pool. There is no direct on-chain transaction linking your specific deposit to your specific withdrawal.

---

## The omnibus model

SureSwap operates an **omnibus wallet** — a shared wallet that holds pooled USDC on each supported chain. When you deposit into Privacy Mode, your funds go into this shared pool. When you withdraw, funds come out of the pool to your destination address.

{: .important }
Privacy Mode is **custodial**. While your deposit is in the pool, SureSwap holds the funds on your behalf. Your balance is tracked internally. Only you can initiate a withdrawal.

---

## Privacy Mode vs standard swaps

| | Standard Swap | Privacy Mode Swap |
|--|--------------|------------------|
| Source of funds | Your wallet | Shared pool |
| Output goes to | Your wallet | Shared pool |
| On-chain link | Visible | Broken |
| Custody | Self-custody | Custodial (pool) |
| Cross-chain | ✓ | ✓ (CCTP) |

---

## Sections

- [Depositing into the Pool](./depositing) — how to add funds to your Privacy Mode balance
- [Privacy Swaps](../swap/how-to-swap#privacy-mode-swaps) — trading from your pool balance
- [Withdrawing from the Pool](./withdrawing) — moving funds back to any address

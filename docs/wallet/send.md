---
title: Sending Tokens
parent: Your Wallet
nav_order: 2
---

# Sending Tokens

Use the **Withdraw / Send** option in the Tools menu to transfer tokens to any address on any supported network.

---

## How to send

1. From the dashboard tap **Tools** → **Withdraw / Send**
2. Select the token you want to send from your list
3. Enter the destination address
4. Enter the amount (or tap **Max** to send the full balance)
5. Review the confirmation screen and tap **Approve** to send

{: .warning }
Always double-check the destination address. Blockchain transactions are irreversible.

---

## Supported token types

### EVM chains (Ethereum, Base, BSC, Arbitrum, HyperEVM, Plasma, Abstract)

- Native gas tokens (ETH, BNB, etc.)
- Any ERC-20 token in your token list

Transactions on EVM chains are **gasless** — SureSwap covers gas fees via a delegated signing mechanism (EIP-7702). You don't need to hold ETH or BNB for gas.

{: .note }
Gasless execution means SureSwap submits the transaction on your behalf through a delegate contract. Your keys remain in Vault; only you can authorise the spend.

### Solana

- Native SOL
- Any SPL token (standard or Token-2022)

### TON

- Native TON
- TON Jettons

### Tron

- Native TRX
- TRC-20 tokens (e.g. USDT on Tron)

---

## Confirmation flow

Every send goes through a **three-step confirm** pattern:

1. **Select token** from your list
2. **Enter destination** — paste the recipient address
3. **Enter amount** — or tap Max
4. **Review & Approve** — final screen shows token, amount, destination, and estimated fee before anything is sent

Tap **Deny** on the confirmation screen to cancel at any time without sending.

---

## Fees

| Network | How fees are paid |
|---------|-----------------|
| EVM chains | Gasless — SureSwap covers gas |
| Solana | Small SOL fee deducted from your balance |
| TON | Small TON fee deducted from your balance |
| Tron | Small TRX fee deducted from your balance |

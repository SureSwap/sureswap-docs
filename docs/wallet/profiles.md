---
title: Profiles
parent: Your Wallet
nav_order: 5
---

# Wallet Profiles

Profiles let you run **multiple isolated wallets** from a single Telegram account. Each profile has its own EVM and Solana addresses, its own token list, and its own transaction history.

---

## What profiles are for

- **Separating funds** — keep a trading wallet separate from long-term holdings
- **Privacy** — use different addresses for different activities
- **Organisation** — name each profile to match its purpose (e.g. "DeFi", "NFTs", "Cold")

---

## Managing profiles

Access profiles via **Profiles** in the main menu.

### Creating a profile

1. Tap **Profiles** → **New Profile**
2. Enter a name (e.g. "Trading")
3. New EVM and Solana keys are generated inside Vault for this profile
4. Your active profile switches to the new one automatically

### Switching profiles

Tap any profile name in the list to make it active. The dashboard immediately updates to show that profile's addresses and balances.

### Renaming a profile

Tap a profile → **Rename** → enter the new name.

### Archiving a profile

Tap a profile → **Archive**. The profile is hidden from the active list but **not deleted** — keys are preserved. You can restore it at any time.

{: .warning }
Archiving does not delete your keys or funds. Tokens on an archived profile remain on-chain and are still accessible after restoring.

### Restoring a profile

Tap **Archived Profiles** → tap the profile to restore → **Restore**.

If you're already at the 10-profile cap, you'll need to archive another active profile first.

---

## Limits

| Limit | Value |
|-------|-------|
| Active profiles at once | 10 |
| Archived profiles | Unlimited |
| Profile name length | Up to 32 characters |

---

## Profile isolation

Each profile has its own:
- EVM address (and therefore its own address on every EVM chain)
- Solana address
- TON and Tron addresses (derived from the profile's keys)
- Token import list
- Privacy Mode balance

Profiles do **not** share funds or keys. A transaction on Profile A has no relation to Profile B.

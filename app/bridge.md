---
description: Move Vetro assets across chains using the Bridge tab.
---

# Bridge

The Bridge tab lets you transfer supported Vetro assets across connected networks using LayerZero's Omnichain Fungible Token (OFT) standard. VUSD and vetBTC are natively present on 100+ chains — bridging moves the same canonical token, not a wrapped version.

## How to Bridge

1. Open [beta.vetro.org](https://beta.vetro.org) and connect your wallet
2. Click the **Bridge** tab in the top navigation
3. Select the asset to bridge (e.g. VUSD)
4. Select the **destination network**
5. Enter the amount to send
6. Review the **estimated received amount** and **network fee**
7. Click **Approve** (first time only for this asset on this network)
8. Click **Bridge** and confirm the transaction in your wallet

> You are bridging from your currently connected network. Switch networks in your wallet before starting if needed.

## Fees

| Fee | Amount |
|-----|--------|
| LayerZero relayer fee | Small fee in source chain native gas token |
| Vetro protocol fee | Zero — no additional protocol fee for bridging |

## What to Expect

- Bridge transactions typically settle in **under 2 minutes**
- Your balance updates on the destination network once the cross-chain message is relayed
- No liquidity pools or intermediaries — the OFT standard burns on source and mints on destination against the same canonical supply

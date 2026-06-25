---
description: How to use the Vetro app to mint, earn, borrow, bridge, and monitor positions.
---

# Using the App

The Vetro app at [app.vetro.org](https://app.vetro.org) is the main interface for interacting with protocol contracts. It organizes user actions into five primary workflows accessible from the top navigation bar: **Swap**, **Earn**, **Borrow**, **Bridge**, and **Analytics**.

## Workflow Summary

| Tab | What you do | Protocol action behind it |
|-----|-------------|--------------------------|
| **Swap** | Swap supported assets, receive VUSD or vetBTC | Gateway mint / swap-in |
| **Earn** | Stake VUSD into sVUSD for variable yield | ERC-4626 StakingVault deposit |
| **Borrow** | Add collateral, borrow VUSD | AMO CDP via Morpho Blue |
| **Bridge** | Move assets across connected chains | LayerZero OFT transfer |
| **Analytics** | Monitor peg, reserves, and positions | Read-only protocol state |

> **Connect your wallet first.** All actions require a connected wallet. Click **Connect Wallet** in the top-right corner of the app before attempting any transaction.

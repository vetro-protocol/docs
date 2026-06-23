---
description: sVUSD is the protocol's variable yield product, implemented as an ERC-4626 vault.
---

# sVUSD

sVUSD is the protocol's variable yield product. Users stake VUSD into the sVUSD ERC-4626 vault and opt into yield generation in exchange for a cooldown period before withdrawal.

## How It Works

The sVUSD vault's price-per-share (PPS) increases over time as yield is distributed. sVUSD holders redeem more VUSD than they deposited as PPS appreciates.

Yield is delivered through the **YieldDistributor** contract, which linearly drips rewards over a governance-configurable period. This drip mechanism prevents yield sniping — without it, an attacker could deposit immediately before a large yield distribution, capture a disproportionate share, and exit.

## Cooldown Period

Exiting sVUSD requires a mandatory cooldown period:

| Stage | Duration |
|-------|----------|
| Initial config | 7 days |
| After drip proven | Target 3 days |
| Minimum | 1 day |

During cooldown, the user's shares are burned and the underlying VUSD is locked. Cooldown positions earn **zero yield** and are non-transferable. Users may cancel an active cooldown at any time before claiming, returning their shares to the vault and resuming yield accrual immediately.

Multiple withdrawal requests create independent cooldown tickets, each with its own timer.

## Protocol Rationale

sVUSD provides three structural advantages to the protocol:

- **Predictable Liquidity Horizon**: The Treasury can accurately forecast outflow velocity, enabling more aggressive yield deployment into longer-term strategies
- **Structural Depeg Resistance**: Every VUSD staked into sVUSD is removed from circulating supply on external markets, creating a structural floor for peg defense
- **Systemic Recovery Window**: The time-lock mechanism prevents reflexive panic-selling during market stress, giving the AMO and arbitrageurs time to re-equilibrate the peg

## Contract

| Network | Address |
|---------|---------|
| Ethereum Mainnet | [0x476310E34D2810f7d79C43A74E4D79405bd7a925](https://etherscan.io/address/0x476310E34D2810f7d79C43A74E4D79405bd7a925) |

---
description: The VETRO (V) governance token and its distribution.
---

# VETRO Token

VETRO (V) is the protocol's governance token, deployed as an ERC-20 on Hemi with LayerZero OFT for multi-chain presence on Ethereum and other networks. VETRO is burnable and serves as the entry point to governance participation.

## Token Distribution

The token distribution is structured to incentivize long-term alignment, with allocations for:

- Core team
- Investors
- Ecosystem development
- Community distribution via a claim drop mechanism targeting veHEMI stakers, VSP holders, and early VUSD minters

The community distribution targets existing aligned communities with the goal of absorbing them into the VETRO ecosystem and aligning them with long-term protocol success through locked governance positions.

## Locking VETRO

VETRO can be locked to receive **veVETRO** — a time-weighted governance position that grants:

- Voting power over protocol parameters
- A share of protocol revenue
- Participation in incentive allocation (gauge voting)

Longer lock durations produce proportionally more veVETRO. Voting power decays toward expiry.

## Early Exit Mechanism

Unlike traditional vote-escrow systems where locked tokens are completely illiquid, veVETRO implements a feature that allows early exit with a penalty:

| Time Locked | Time Remaining | Haircut Penalty | User Receives |
|-------------|----------------|-----------------|---------------|
| e.g., 1 year | e.g., 3 years | 80% | 20% |
| e.g., 2 years | e.g., 2 years | 50% | 50% |
| e.g., 3 years | e.g., 1 year | 20% | 80% |

All slashed tokens are **burned**, permanently reducing total VETRO supply.

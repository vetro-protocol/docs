---
description: veVETRO is the vote-escrowed governance and revenue-sharing mechanism.
---

# veVETRO

veVETRO is the vote-escrowed form of VETRO, represented as a transferable NFT following the Aerodrome model. Users lock VETRO for a chosen duration to receive veVETRO.

## Governance Powers

veVETRO holders govern the following protocol parameters:

- **Protocol Proposals**: Vote on protocol upgrades, parameter changes, and strategic decisions
- **Incentive Allocation**: Direct where incentives and rewards flow across yield strategies via gauge voting (similar to the veCRV model)
- **Revenue Distribution**: Vote on allocation parameters for yield, stability fees, and AMO revenue
- **Economic Parameters**: Set configurable parameters including treasury allocation ratios, cooldown durations, redemption delays, CDP debt ceilings, and approved CDP collateral assets

## Revenue Distribution

Protocol revenue flows from 6 sources into veVETRO stakers:

1. Lazy yield from unstaked VUSD backing
2. Stability fees from CDP positions
3. AMO arbitrage profits
4. Gateway mint and redeem fees
5. Keeper token revenue
6. Bridged revenue from cross-chain operations

Revenue is collected on Ethereum through Treasury operations and bridged to Hemi via LayerZero for distribution. The Revenue Splitter contract on Hemi allocates funds per governance-approved parameters.

## Delegate Incentives

Recognizing that most token holders do not actively participate in governance, VETRO implements a delegate incentive system:

| Recipient | Share |
|-----------|-------|
| veVETRO stakers | 95% |
| Active delegates | 5% |

The 5% delegate share is governance-adjustable. Professional delegates who actively vote on behalf of others receive a share of protocol revenue allocated to their delegated voting power.

## Guardian Veto

The protocol maintains a Guardian system with veto authority over veVETRO governance decisions:

- **Collective Veto**: Guardians cannot initiate or implement changes independently — changes must originate from veVETRO holders. A veto of a passed governance decision requires a threshold of consensus among the Guardian whitelist
- **Emergency Intervention**: A single Guardian can unilaterally activate specific time-sensitive safety controls (e.g., pausing a depegged stablecoin) without waiting for a full governance cycle
- **Guardian Whitelist**: Guardian membership is itself governed by veVETRO holders — the community retains ultimate authority over who holds veto power

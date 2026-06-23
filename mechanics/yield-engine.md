---
description: How the Agentic Yield Engine sources, manages, and distributes yield.
---

# Yield Engine

## The Agentic Yield Engine

To achieve institutional-grade capital efficiency at AI speed, the protocol uses a multi-agent autonomous system to oversee the selection, monitoring, and rebalancing of yield-bearing assets.

### Agent Roles

| Agent | Responsibility |
|-------|---------------|
| **Protocol Analyst Agent** | Evaluates top-tier protocols (Aave, Compound, Morpho) and emerging platforms based on verifiable TVL, historical bug bounties, and audit depth |
| **Curator Intelligence Agent** | Monitors curated lending vaults, evaluating curator reputation, historical performance, and risk mandates |
| **Strategy Forensic Agent** | Look-through analysis of final capital deployment — assesses underlying strategy risk, MEV-protected liquidation bots, and oracle reliability |
| **Red-Team Agent** | Adversarial validator looking for edge case risks: oracle lag, incentive-driven liquidity bloating, and previous exploit patterns |

### Human-in-the-Loop

Despite the high level of automation, the protocol maintains a man-machine teaming requirement:

- **Guardian/Keeper Review**: All significant capital reallocations suggested by agents require final verification by human Guardians or Keepers before funds are moved
- **Veto Authority**: Guardians retain the power to veto any agent-initiated proposal that deviates from the protocol's core safety parameters

## Yield Generation Pipeline

```
1. Users swap approved stablecoins → Gateway → receive VUSD
2. Treasury allocates swapped-in assets (80% to yield strategies)
3. Yield vaults deploy assets into DeFi strategies via Vesper Finance private vaults
   (Morpho, Compound, Aave)
4. Strategy yields are harvested by keepers and aggregated at Treasury level
5. YieldDistributor receives yield and drips it linearly into sVUSD StakingVault
6. VUSDx holders receive fixed-rate yield via Pendle PT purchasing at epoch init
7. Lazy yield (unstaked VUSD) flows to Treasury → reserves + veVETRO distributions
```

## Strategy Universe

| Category | Description |
|----------|-------------|
| **Lending Protocols** | Supplying stablecoins to Morpho, Aave, Compound — diversified counterparty risk |
| **Stablecoin LP** | Providing liquidity in stablecoin-to-stablecoin pools on Curve — low impermanent loss |
| **Direct Aggregators** | Integration with yield aggregators beyond the initial vault provider |
| **Multi-Chain Yield** | V3 roadmap: deploy assets across multiple L1/L2 networks, route yields back to Ethereum |
| **Delta-Neutral** | V3/V4: basis trades (long spot, short perps) — consistent yields independent of market direction |
| **RWA Strategies** | V4 roadmap: T-bills, credit funds, private credit |

## Revenue Sources

Protocol revenue flows from 6 sources into veVETRO stakers:

1. Lazy yield from unstaked VUSD backing
2. Stability fees from CDP positions
3. AMO arbitrage profits
4. Gateway mint and redeem fees
5. Keeper token revenue
6. Bridged revenue from cross-chain operations

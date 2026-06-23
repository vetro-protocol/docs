---
description: The AMO maintains the VUSD peg on decentralized exchanges.
---

# AMO (Automated Monetary Operations)

The AMO controller maintains the VUSD peg on decentralized exchanges — initially Curve Finance — by executing algorithmic interventions when the market price deviates from parity.

The AMO draws design influence from established peg stability mechanisms such as the FRAX AMO and msUSD, adapted to Vetro's over-collateralized reserve structure.

## Protocol-Owned Liquidity (POL)

POL refers to VUSD and paired assets that the protocol itself deploys into DEX liquidity pools, rather than relying solely on external liquidity providers. This liquidity is sourced from protocol treasury reserves and forms the operational foundation for all AMO peg defense activities.

POL is established through the protocol's excess collateralization. When treasury reserves exceed the minimum required backing ratio — often driven by accumulated strategy yield — the protocol can deploy this surplus into DEX pools.

## Peg Mechanics

### Peg-Up Operation (VUSD Below Peg)

When VUSD trades below $1.00, the AMO:
1. Withdraws VUSD from the Curve liquidity pool
2. Burns the withdrawn tokens
3. This reduces circulating supply in the DEX, creating upward price pressure

> Burning VUSD frees the underlying collateral backing those tokens, increasing the protocol's overcollateralization ratio — creating a self-reinforcing dynamic where peg defense simultaneously strengthens reserves.

### Peg-Down Operation (VUSD Above Peg)

When VUSD trades above $1.00, the AMO:
1. Mints new VUSD within its authorized budget
2. Deposits it into the Curve pool
3. This increases supply, creating downward price pressure
4. The protocol captures arbitrage profits from the spread, flowing to the Treasury

## AMO Safety Constraints

| Constraint | Description |
|-----------|-------------|
| **Maximum Mint Limit** | The Gateway enforces an AMO mint limit capping total VUSD the AMO can create — governed by veVETRO |
| **Collateralization Floor** | The AMO cannot reduce the protocol's backing ratio below a governance-defined minimum |
| **Circuit Breakers** | Automatic pause triggers activate if oracle feeds become stale, price deviations exceed thresholds, or DEX conditions become anomalous |
| **Recursive Loop Protection** | AMO is explicitly prevented from scenarios creating self-referential collateral loops; all AMO supply is tracked separately |

## AMO-Created Supply

On V1, AMO-created VUSD is minted into Morpho Blue markets and is economically backed by overcollateralized positions in hemiBTC and WETH. Each unit of AMO VUSD corresponds to a Morpho lending receipt representing a claim on borrower debt secured by collateral exceeding the borrowed VUSD value.

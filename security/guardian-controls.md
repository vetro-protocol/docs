---
description: Emergency controls available to protocol Guardians.
---

# Guardian Controls

The protocol is overseen by Guardians with emergency powers. Guardian whitelist membership is governed by veVETRO holders — the community retains ultimate authority over who holds these powers.

## Emergency Powers

| Control | Description |
|---------|-------------|
| **Global Bot Kill-Switch** | Revokes all automated bot permissions in one transaction across all modules |
| **CDP Budget Freeze** | Sets any Morpho market debt budget to zero, instantly halting new minting against that market |
| **Arb Path Circuit Breaker** | Pauses specific swap paths if underlying DEX pools become volatile or compromised |
| **Drip Freeze** | Pauses the linear release of rewards from the YieldDistributor during security incidents |

## Smart Contract Bot Guardrails

All keeper bots operate under the Principle of Least Privilege:

- **RBAC**: Bots restricted to specific functions with zero admin or withdrawal rights. Treasury keeper and UMM roles are strictly separated from administrative functions
- **Slippage Circuit Breaker**: Hard-coded revert if any arbitrage operation results in slippage exceeding a governance-defined threshold
- **Velocity Limits**: Caps on total volume a single bot address can liquidate within a rolling time window
- **Pre-Action Health Check**: Contracts verify target positions are liquidatable at the moment of execution using fresh oracle data
- **Post-Action Solvency Check (No-Worse-Off Rule)**: Reverts transactions if the protocol's overall collateral ratio does not improve after liquidation

## Oracle Safety

Automated, state-based oracle protections trigger without human intervention:

| Protection | Behavior |
|-----------|---------|
| **Deviation Trigger** | If the primary price feed deviates beyond a configurable threshold from a secondary source, the affected market enters Safety Pause mode |
| **Staleness Check** | Transactions revert automatically if oracle data exceeds the configured staleness period |
| **Repay-Only Mode** | During any security pause, new positions and liquidations are frozen, but debt repayment and position closing remain functional so users can always exit |

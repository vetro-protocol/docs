---
description: Monitor protocol state, peg health, reserves, and your positions.
---

# Analytics

The Analytics tab provides a real-time view of protocol-level metrics including peg stability, reserve composition, and TVL. No wallet connection is required to view analytics.

## Key Metrics

| Metric | What it shows |
|--------|--------------|
| **Current Peg Stability** | Live VUSD price relative to $1.00 |
| **Peg Stability Chart** | Historical peg price over selectable time ranges (week / month / year) |
| **Total VUSD Staked** | Total VUSD currently deposited in sVUSD |
| **Total VUSD on Withdrawal Cooldown** | VUSD currently in active cooldown exit positions |
| **Collateralization Ratio** | Total backing value divided by total VUSD supply |
| **Total Value Locked (TVL)** | Total collateral assets held in the protocol Treasury |

## Peg Stability Chart

The peg chart shows VUSD price over time. A healthy protocol maintains a price tightly clustered around 1.0000. Use the time range selector (week / months / years) to view short-term or long-term peg behavior.

## Reserve Verification

Reserve data in Analytics is sourced directly from on-chain state. For independent verification, view the core contracts on Etherscan:

| Contract | Address |
|----------|---------|
| Treasury | [0xC8317A10385BE07901A4c9ee3d06E1D83AE378c9](https://etherscan.io/address/0xC8317A10385BE07901A4c9ee3d06E1D83AE378c9) |
| VUSD | [0xCa83DDE9c22254f58e771bE5E157773212AcBAc3](https://etherscan.io/address/0xCa83DDE9c22254f58e771bE5E157773212AcBAc3) |
| sVUSD | [0x476310E34D2810f7d79C43A74E4D79405bd7a925](https://etherscan.io/address/0x476310E34D2810f7d79C43A74E4D79405bd7a925) |

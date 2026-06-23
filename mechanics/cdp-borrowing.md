---
description: Over-collateralized borrowing of VUSD against crypto collateral.
---

# CDP Borrowing

Beyond the swap-and-mint pathway for VUSD, the protocol supports over-collateralized borrowing. Users deposit crypto assets as collateral and borrow VUSD against them, creating dollar liquidity without selling their underlying position.

## How It Works

The VETRO Treasury acts as the direct lender. The AMO mints VUSD within its authorized budget and supplies it as borrowable liquidity to the collateralized market. Borrowed VUSD enters circulation like any other VUSD and is burned upon repayment.

## Borrowing Flow

```
1. Add supported collateral (hemiBTC, WETH) into the designated Morpho Blue market
2. Borrow VUSD up to the governance-defined LTV ratio
3. Stability fee accrues on outstanding debt balance
4. Manage position: add collateral, repay debt, or close at any time
5. Repay VUSD → VUSD is burned → collateral released
```

If the collateral value drops below the liquidation threshold, the position is permissionlessly liquidatable. Liquidators seize the necessary collateral, repay the borrowed VUSD (which is burned), and keep the liquidation bonus.

## Protocol Architecture — Morpho Blue

Collateralized borrowing markets are deployed through Morpho Blue for several reasons:

- **Permissionless Market Creation**: Deploy isolated lending markets for any collateral pair without requiring governance approval from the underlying platform
- **Existing Infrastructure**: Battle-tested liquidation infrastructure with established MEV bot networks
- **Out-of-the-Box CDP Functionality**: Morpho Blue's market design functions as a CDP mechanism where the Treasury supplies borrow-side liquidity

## Risk Parameters

| Parameter | Description | Governance |
|-----------|-------------|------------|
| **Global Debt Ceiling** | Maximum total VUSD the AMO can supply to all CDP markets | veVETRO |
| **LTV Ratio** | Per-market loan-to-value ratio (how much VUSD can be borrowed per $1 of collateral) | veVETRO |
| **Liquidation Threshold** | LTV at which a position becomes liquidatable | veVETRO |
| **Stability Fee** | Annual fee on outstanding debt | veVETRO |
| **Oracle Config** | Deviation and staleness thresholds per collateral market | Keeper |

## Supported Collateral

| Asset | Status |
|-------|--------|
| hemiBTC | Live (V1) |
| WETH | Live (V1) |
| cbBTC, tBTC, wSOL, wBNB | Planned (V2) |
| Real-world assets | Planned (V4) |

## Use Cases

- **Real-World Payments**: Miners and long-term holders access dollar liquidity for operational expenses without selling crypto or triggering taxable events
- **Leverage**: Add collateral, borrow VUSD, purchase more crypto — create leveraged long exposure
- **Yield Arbitrage**: Borrow VUSD at the stability fee rate and deploy into yield strategies with a higher return, capturing the spread

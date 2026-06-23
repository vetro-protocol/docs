---
description: Deposit crypto collateral and borrow VUSD through the Borrow tab.
---

# Borrow

The Borrow tab lets you open a Collateralized Debt Position (CDP) by depositing supported crypto assets as collateral and borrowing VUSD against them. This lets you access dollar liquidity without selling your crypto.

## Supported Collateral (Live)

| Collateral | Borrow Asset | Status |
|------------|-------------|--------|
| hemiBTC | VUSD | ✅ Live |
| WETH | VUSD | ✅ Live |

## Key Concepts

| Term | What it means |
|------|--------------|
| **Collateral** | The crypto asset you deposit to back your loan |
| **Loan Size** | The amount of VUSD you can borrow, determined by your LTV ratio |
| **Health Factor** | Ratio of your collateral value to your debt — must stay above 1.0 to avoid liquidation |
| **Liquidation Price** | The collateral price at which your position becomes liquidatable |

## How to Borrow

1. Open [beta.vetro.org](https://beta.vetro.org) and connect your wallet
2. Click the **Borrow** tab in the top navigation
3. Select a borrow market (e.g. hemiBTC / VUSD or WETH / VUSD)
4. Click **Supply Collateral** and enter the amount to deposit
5. Approve the collateral deposit transaction in your wallet
6. Enter the amount of VUSD you want to borrow
7. Click **Borrow** and approve the transaction
8. VUSD will appear in your wallet

> Keep an eye on your **Health Factor**. If it approaches 1.0, your position is at risk of liquidation. Add more collateral or repay debt to stay safe.

## How to Repay

1. In the Borrow tab, find your open position under **Your Borrow Positions**
2. Click **Repay**
3. Enter the amount of VUSD to repay
4. Approve the transaction — VUSD is burned and your collateral ratio improves
5. To fully close: repay all outstanding debt, then click **Withdraw Collateral**

## Liquidation

If your health factor falls below 1.0, any address can liquidate your position:

- The liquidator repays your VUSD debt
- They receive your collateral plus a liquidation bonus
- The repaid VUSD is burned

To avoid liquidation: add more collateral or repay part of your debt before the health factor reaches 1.0.

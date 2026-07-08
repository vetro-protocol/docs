---
description: How VUSD is minted, held, and redeemed.
---

# Minting & Redemption

## Minting Flow

```
Step 1: Swap any approved stablecoin (USDC, USDT) → Gateway
Step 2: Gateway mints VUSD at 1:1 minus a nominal minting fee
Step 3: Treasury allocates collateral → Redemption Buffer (20%) + Yield Strategies (80%)
```

Accepted collateral at launch: USDC, USDT. Planned additions: DAI, USDS, USDf, USD1.

Each whitelisted token is configured with:
- A dedicated yield vault
- A decentralized price oracle with configurable staleness period
- Independent swap-in/swap-out toggles

## Standard Redemption (Multi-Step)

Standard users follow a security-delay flow to prevent flash loan attacks and MEV manipulation:

1. **Initiate** — submit a redemption request for the amount of VUSD to redeem
2. **Wait** — governance-configurable security delay (~6 blocks / 60–90 seconds)
3. **Finalize** — submit a second transaction specifying the desired stablecoin to claim funds

Funds are pulled first from the Treasury's redemption buffer, then from deployed strategy assets if necessary. If combined liquidity cannot fulfill 100% of the request, the transaction fulfills the maximum available amount rather than reverting.

## Instant Redemption (Whitelisted Market Makers)

Whitelisted addresses bypass the security delay and execute instant, single-transaction redemptions. Instant redemptions are strictly limited to the current Treasury buffer balance — the protocol will not pull from yield strategies to fulfill instant requests.

## Treasury Allocation

| Destination | Target Allocation | Purpose |
|-------------|------------------|---------|
| Redemption Buffer | 20% | Instant redemptions, peg arbitrage support |
| Yield Strategies | 80% | Revenue generation via lending protocols |

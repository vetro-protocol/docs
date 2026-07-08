---
description: VUSD is the protocol's primary dollar-referenced settlement asset.
---

# VUSD

VUSD is a protocol-generated dollar-referenced settlement asset, targeting a 1:1 value relationship with the US dollar. It is over-collateralized by a diversified basket of USDC, USDT, frxUSD and additional stablecoins approved by the protocol team and governance.

## Key Properties

- **Settlement-grade**: designed for high-velocity cross-chain settlement and institutional use
- **Over-collateralized**: backed by a diversified basket of approved stablecoins
- **Omnichain**: natively present on 100+ chains via LayerZero OFT — no wrapping required
- **Redeemable**: on a best-efforts basis subject to liquidity and strategy performance
- **Yield-separated**: VUSD holders do not take on yield strategy risk by default

## Minting VUSD

Users deposit approved stablecoins (USDC, USDT, frxUSD) through the Gateway contract and receive VUSD at a 1:1 rate minus a nominal minting fee. There is no lockup on the base asset.

## Holding VUSD

VUSD held without staking continues to function as a settlement-grade dollar token. The yield generated on its backing collateral flows to the protocol treasury to fund reserves, operations, and governance revenue distribution — this is called **Lazy Yield**.

## Redeeming VUSD

Standard users follow a multi-step redemption flow:

1. Initiate a redemption request specifying the desired stablecoin
2. Wait for the governance-configurable security delay (~6 blocks / 60–90 seconds)
3. Finalize with a second confirmation

Whitelisted market makers bypass the security delay and execute instant single-transaction redemptions, limited to the current Treasury buffer balance.

## Reserve Protections

VUSD holders benefit from four layers of protection:

1. A diversified strategy universe targeting 30 independent yield sources at maturity
2. A liquid redemption buffer held outside yield deployment
3. Priority-first redemption rights relative to sVUSD and VUSDx holders
4. Protocol-maintained self-insurance buffers

## Contract

| Network | Address |
|---------|---------|
| Ethereum Mainnet | [0xCa83DDE9c22254f58e771bE5E157773212AcBAc3](https://etherscan.io/address/0xCa83DDE9c22254f58e771bE5E157773212AcBAc3) |

## Want to Integrate with VUSD?

If you represent a project and want to discuss integrating VUSD or adding a new minting input asset:
[Speak to the team →](https://vetro.org/speak-to-the-team)

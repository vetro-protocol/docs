---
description: Vetro protocol liquidity pools on Curve Finance (Ethereum mainnet).
---

# Curve Pools

Vetro maintains protocol-owned liquidity on Curve Finance across several pools for VUSD, sVUSD, vetBTC, and svetBTC. All pools are on Ethereum mainnet.

## VUSD Pools

| Pool | Pool Address | Gauge Address | Curve UI |
|------|-------------|---------------|----------|
| VUSD / crvUSD | [0xafba5800...f3d](https://etherscan.io/address/0xafba5800252530ce71b03ba2bca2dd5ae44a7f3d) | [0x737e7700...57a](https://etherscan.io/address/0x737e7700e03a8c451c9b72103554a40760f1b57a) | [Swap](https://www.curve.finance/dex/ethereum/pools/0xafba5800252530ce71b03ba2bca2dd5ae44a7f3d/swap) |
| VUSD / msUSD | [0x8bEA2a46...d2](https://etherscan.io/address/0x8bEA2a46D56c321A216F97Ab6b61C34098B819d2) | [0x28a72343...Cc](https://etherscan.io/address/0x28a72343bFf5e10b36E72d86b1041ED2447Dc0Cc) | [Deposit](https://www.curve.finance/dex/ethereum/pools/0x8bea2a46d56c321a216f97ab6b61c34098b819d2/deposit) |
| frxUSD / VUSD | [0xdE057696...96](https://etherscan.io/address/0xdE0576968C898bbE7bf13d79862F252c58443F96) | [0x766752eF...CF](https://etherscan.io/address/0x766752eFbE71Ba7897B205B53EfBd34EC85CA0Cf) | [Deposit](https://www.curve.finance/dex/ethereum/pools/0xde0576968c898bbe7bf13d79862f252c58443f96/deposit) |
| VUSD / hemiBTC | [0xc4ff0e84...4f](https://etherscan.io/address/0xc4ff0e84ec219581092e5660c74a2da8de6aee4f) | [0x5B933Fc4...83](https://etherscan.io/address/0x5B933Fc47431795a0c2eb8D183BEAE9722e1fD83) | [Deposit](https://www.curve.finance/dex/ethereum/pools/0xc4ff0e84ec219581092e5660c74a2da8de6aee4f/deposit) |

## sVUSD Pools

| Pool | Pool Address | Gauge Address | Curve UI |
|------|-------------|---------------|----------|
| crvUSD / sVUSD | [0x659b7b5d...d3](https://etherscan.io/address/0x659b7b5dd7936bf2f2d198a87c1583049d1d91d3) | [0x543c88e9...ed](https://etherscan.io/address/0x543c88e9b7bd90a4c14a31bdbf41dd509ab666ed) | [Swap](https://www.curve.finance/dex/ethereum/pools/0x659b7b5dd7936bf2f2d198a87c1583049d1d91d3/swap) |

## vetBTC & svetBTC Pools

| Pool | Pool Address | Gauge Address |
|------|-------------|---------------|
| vetBTC / WBTC | [0xf2e47b9b...65](https://etherscan.io/address/0xf2e47b9bcb26463a12b1409be06fdaa1c308aa65) | [0x6e5c4601...6e](https://etherscan.io/address/0x6e5c4601d45a7c21d3a839639a0ae500226c735e) |
| WBTC / svetBTC | [0x90343fc2...6d](https://etherscan.io/address/0x90343fc2e9449e9cd001be955fad9727c815ec6d) | [0x3324a9B0...ee](https://etherscan.io/address/0x3324a9B0a8e15A24Cb66A93E033329340E3afdEe) |

## Full Addresses Reference

<details>
<summary>Show all full addresses</summary>

**VUSD / crvUSD**
- Pool: `0xafba5800252530ce71b03ba2bca2dd5ae44a7f3d`
- Gauge: `0x737e7700e03a8c451c9b72103554a40760f1b57a`

**VUSD / msUSD**
- Pool: `0x8bEA2a46D56c321A216F97Ab6b61C34098B819d2`
- Gauge: `0x28a72343bFf5e10b36E72d86b1041ED2447Dc0Cc`

**frxUSD / VUSD**
- Pool: `0xdE0576968C898bbE7bf13d79862F252c58443F96`
- Gauge: `0x766752eFbE71Ba7897B205B53EfBd34EC85CA0Cf`

**VUSD / hemiBTC**
- Pool: `0xc4ff0e84ec219581092e5660c74a2da8de6aee4f`
- Gauge: `0x5B933Fc47431795a0c2eb8D183BEAE9722e1fD83`

**crvUSD / sVUSD**
- Pool: `0x659b7b5dd7936bf2f2d198a87c1583049d1d91d3`
- Gauge: `0x543c88e9b7bd90a4c14a31bdbf41dd509ab666ed`

**vetBTC / WBTC**
- Pool: `0xf2e47b9bcb26463a12b1409be06fdaa1c308aa65`
- Gauge: `0x6e5c4601d45a7c21d3a839639a0ae500226c735e`

**WBTC / svetBTC**
- Pool: `0x90343fc2e9449e9cd001be955fad9727c815ec6d`
- Gauge: `0x3324a9B0a8e15A24Cb66A93E033329340E3afdEe`

</details>

## StakeDAO Incentivized Vaults

StakeDAO offers boosted yield strategies on top of the Vetro Curve pools. Depositing via StakeDAO auto-compounds CRV and SDT rewards on top of base Curve APR.

| Pool | StakeDAO Vault |
|------|---------------|
| VUSD / hemiBTC | [View strategy](https://www.stakedao.org/strategy?protocol=curve&vault=1-0xDE69194903dA2c2099Bb3029d9eac6df45e6AcA8) |
| VUSD / crvUSD | [View strategy](https://www.stakedao.org/strategy?protocol=curve&vault=1-0x102A475c8d660fDe678D108DCc6D4A2227661AF2) |
| frxUSD / VUSD | [View strategy](https://www.stakedao.org/strategy?protocol=curve&vault=1-0xE3F03e175bf43356eaB231c9Fd05494434651e36) |
| VUSD / msUSD | [View strategy](https://www.stakedao.org/strategy?protocol=curve&vault=1-0x757360820728819953937B752f6B83AeB11090c7) |
| crvUSD / sVUSD | [View strategy](https://www.stakedao.org/strategy?protocol=curve&vault=1-0x0931E5C4e9C49e7158E13e57ddfff83b5FEC6c2c) |

> APRs on StakeDAO vaults are variable and typically higher than base Curve APR due to additional SDT and CRV boost. Check the strategy page for current rates before depositing.

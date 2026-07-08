---
description: All deployed contract addresses. Source of truth is GitHub Issue #111.
---

# Deployed Addresses

> Source of truth: [GitHub Issue #111](https://github.com/vetro-protocol/vetro-contracts/issues/111)

## VUSD — Ethereum Mainnet

| Contract | Address |
|----------|---------|
| VUSD (PeggedToken) | [0xCa83DDE9c22254f58e771bE5E157773212AcBAc3](https://etherscan.io/address/0xCa83DDE9c22254f58e771bE5E157773212AcBAc3) |
| sVUSD (StakingVault) | [0x476310E34D2810f7d79C43A74E4D79405bd7a925](https://etherscan.io/address/0x476310E34D2810f7d79C43A74E4D79405bd7a925) |
| Gateway | [0xDaD503f8B9d42bb7af3AfC588358D30163e4416F](https://etherscan.io/address/0xDaD503f8B9d42bb7af3AfC588358D30163e4416F) |
| Treasury | [0xC8317A10385BE07901A4c9ee3d06E1D83AE378c9](https://etherscan.io/address/0xC8317A10385BE07901A4c9ee3d06E1D83AE378c9) |
| YieldDistributor | [0x55745265Ba172378cf45d224F09F0673cB470cef](https://etherscan.io/address/0x55745265Ba172378cf45d224F09F0673cB470cef) |
| Deployer | [0xE173b056eF552c7322040703dDfC1e0638A575d3](https://etherscan.io/address/0xE173b056eF552c7322040703dDfC1e0638A575d3) |
| Multisig (Safe) | [0x6649Ddb5c7e52348b73c8bBdD2A1cbA630b7AaEA](https://app.safe.global/home?safe=eth:0x6649Ddb5c7e52348b73c8bBdD2A1cbA630b7AaEA) |

### Gateway Proxy Details
| Field | Address |
|-------|---------|
| Proxy | `0xDaD503f8B9d42bb7af3AfC588358D30163e4416F` |
| Implementation | `0x7AFcFcC9619272B4610dDB1E98e6f0cF8E765C81` |
| Proxy Admin | `0x83B2435d9A30b7463B3Ba997ba47a14B73149e2A` |

### StakingVault Proxy Details
| Field | Address |
|-------|---------|
| Proxy | `0x476310E34D2810f7d79C43A74E4D79405bd7a925` |
| Implementation | `0xFBe09b404E50193237D7c9777585a27eB927fF25` |
| Proxy Admin | `0x3912505880b9b8F0Ac2531cde9428994a7728aa3` |

### YieldDistributor Proxy Details
| Field | Address |
|-------|---------|
| Proxy | `0x55745265Ba172378cf45d224F09F0673cB470cef` |
| Implementation | `0xe8Ac98555f8815F4c125C871F803DFCaD2101886` |
| Proxy Admin | `0xDd751f2B4FA3445C7befa39cf981b6bEc1FeB1B1` |

## vetBTC — Ethereum Mainnet

| Contract | Address |
|----------|---------|
| vetBTC (VetBTC) | [0xf196C68233464A16CFDa319a47c21f4cECa62001](https://etherscan.io/address/0xf196C68233464A16CFDa319a47c21f4cECa62001) |
| svetBTC (SVetBTC) | [0x0cB9D84d4bcEc8d3D5B2d99a6F07f4605325987e](https://etherscan.io/address/0x0cB9D84d4bcEc8d3D5B2d99a6F07f4605325987e) |
| VetBTCGateway | [0xCBA2Ffa0AC52d7871a4221a871793Eb788013faB](https://etherscan.io/address/0xCBA2Ffa0AC52d7871a4221a871793Eb788013faB) |
| VetBTCTreasury | [0xd25a7b0b817fD816d0995eC67fb70e75EE65Bd7F](https://etherscan.io/address/0xd25a7b0b817fD816d0995eC67fb70e75EE65Bd7F) |
| VetBTCYieldDistributor | [0xd74bcf1299176E98899bA2e86dD2C9aE089F5276](https://etherscan.io/address/0xd74bcf1299176E98899bA2e86dD2C9aE089F5276) |

## VUSD OFT — Multichain

| Network | Address |
|---------|---------|
| Ethereum (OFT Adapter) | [0xFc8Acf5ef1E8839Ec94151740CfEd95D7E579Afb](https://etherscan.io/address/0xFc8Acf5ef1E8839Ec94151740CfEd95D7E579Afb) |
| Hemi | `0xD3599AE62EE280709A22268a46d23164214e345B` |
| Arbitrum | `0xCE2c108fB49551f6d27BBb529Ad1938835ac3574` |
| Base | `0x8a654093e21703afc8d038FF253A3c974C5C2957` |
| Optimism | `0xb591169E6508983CC6618738cC73c9F09c38dE14` |
| BNB | `0x10061d0593441Ff74536158592e1Be3F4C7B180C` |

## sVUSD OFT — Multichain

| Network | Address |
|---------|---------|
| Ethereum (OFT Adapter) | [0x968563eeD04e0289ccC79d7029bFc79F040605f0](https://etherscan.io/address/0x968563eeD04e0289ccC79d7029bFc79F040605f0) |
| Hemi | `0xfe875CC86cC6BC2E93ab330D6b2c408C3Cd79710` |
| Arbitrum | `0x50c580227764b621c0433bB6Ab756C781c495ce7` |
| Base | `0xb174750002068862Dfe7DF38F974a950F189386a` |
| Optimism | `0x92273Ca3356379C2fe870FE3805cc5e7aB6d19c6` |
| BNB | `0xC141B66eE4262Ba46Ea29578955C274fD4A96515` |

## Whitelisted Collateral Tokens

### VUSD Gateway
| Token | Address | Vault | Oracle |
|-------|---------|-------|--------|
| USDC | `0xA0b86991c6218b36c1d19D4a2e9Eb0cE3606eB48` | `0xe3DA4B83C9dd4c4D185ecE42077462b3F35c454a` | `0x8fFfFfd4AfB6115b954Bd326cbe7B4BA576818f6` |
| USDT | `0xdAC17F958D2ee523a2206206994597C13D831ec7` | `0x6d134cAAD0CA29Cd6ea145f6C0DC766076690547` | `0x3E7d1eAB13ad0104d2750B8863b489D65364e32D` |
| frxUSD | `0xCAcd6fd266aF91b8AeD52aCCc382b4e165586E29` | `0xBd44B65cE2b7c736724E0AE7e008CE3Fb00697d8` | `0x9B4a96210bc8D9D55b1908B465D8B0de68B7fF83` |


### vetBTC Gateway
| Token | Address | Vault | Oracle |
|-------|---------|-------|--------|
| WBTC | `0x2260FAC5E5542a773Aa44fBCfeDf7C193bc2C599` | `0x30c410D92e54B2b492D725D6CEBed98891817C91` | `0x032A35daDA672B394525881f789a3B4E7734C76C` |
| cbBTC | `0xcbB7C0000aB88B473b1f5aFd9ef808440eed33Bf` | `0xD954d72D885f8409bCBe3f15ad2fc3EcA4a5Ba33` | `0x33F1E44DB47400C9BD6221962712D882Adb8fFA6` |

---
description: Vetro's VUSD Meta Vault and Morpho Blue markets on Ethereum mainnet.
---

# Morpho

Vetro operates a **VUSD Meta Vault** on Morpho, enabling third parties to supply VUSD and earn yield across underlying Morpho Blue markets. The vault is curated by the Vetro protocol.

## VUSD Meta Vault

| Field | Value |
|-------|-------|
| **Vault Contract (VUSDmeta)** | [0x6283C405...1E7](https://etherscan.io/token/0x6283c40558521515595cbcc573f8a0489ab4d1e7) |
| **Curator** | [0xAF27289d...c2](https://etherscan.io/address/0xaf27289d8612574a2bf58f30ad1835ba9d56bfc2) |
| **Underlying Asset** | VUSD `0xCa83DDE9c22254f58e771bE5E157773212AcBAc3` |
| **Morpho Curator UI** | [View allocation](https://curator.morpho.org/vaults/1/0x6283C40558521515595cbCc573f8A0489Ab4d1E7/allocation) |

## Underlying Morpho Blue Markets

These are the CDP borrow markets that the Meta Vault allocates VUSD liquidity into. Borrowers deposit collateral and borrow VUSD; the Meta Vault earns the interest.

| Market | Collateral | Borrow Asset | Market ID |
|--------|-----------|-------------|-----------|
| hemiBTC / VUSD | hemiBTC | VUSD | `0x55609be6...2e5` |
| WETH / VUSD | WETH | VUSD | `0x7d1306d2...561` |

<details>
<summary>Show full market IDs</summary>

**hemiBTC / VUSD**
`0x55609be688a4d96e715bfe39969133bd4e7f83db4f77bb06216109189a11f2e5`

**WETH / VUSD**
`0x7d1306d23f9f1e419697b8275001db9ea74b3c75190a7db8f5d81fed2fb94561`

</details>

## Full Addresses Reference

<details>
<summary>Show all full addresses</summary>

**VUSD Meta Vault**
- Vault: `0x6283C40558521515595cbCc573f8A0489Ab4d1E7`
- Curator: `0xAF27289d8612574a2bf58f30ad1835ba9d56bfc2`

</details>

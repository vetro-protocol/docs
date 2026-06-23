---
description: How the Vetro protocol stack is structured across chains.
---

# Architecture

## The VETRO Stack

The protocol operates as a decentralized, multi-chain system where core functions are distributed to optimize for security, cost, and liquidity.

### 1. Settlement & Stability Hub — Ethereum

Ethereum serves as the primary custody and settlement layer. This hub hosts the core PeggedToken contracts, the Treasury for asset custody, and manages the high-value issuance and redemption logic for the protocol's reserves.

### 2. Governance Logic Hub — Hemi

All protocol governance and high-frequency parameter decisions take place on the Hemi blockchain. This layer hosts veVETRO positions and gauge controllers, utilizing Hemi's efficiency to relay decisions to Ethereum via LayerZero messaging.

### 3. Omnichain Connectivity — LayerZero OFT

Every VETRO asset is an Omnichain Fungible Token (OFT). This ensures native representation on 100+ chains, allowing VUSD, vetBTC, and vetETH to circulate without the risks associated with traditional wrapping or bridging.

### 4. Universal Entry & Yield Sourcing

While the protocol initially anchors minting inputs and yield strategies on Ethereum for maximum liquidity, the architecture is designed for universal expansion. Future phases will enable users to mint VUSD or vet primitives from any supported chain.

## The Full Asset Suite

| Category | USD Assets | BTC Assets | ETH Assets |
|----------|-----------|-----------|-----------|
| Base Settlement | VUSD | vetBTC | vetETH |
| Variable Yield | sVUSD | svetBTC | svetETH |
| Fixed Term | VUSDx | vetBTCx | vetETHx |
| Governance | veVETRO | veVETRO | veVETRO |

## Smart Contract Design Principles

The core Ethereum contracts are implemented in Solidity 0.8.30 with the following design principles:

- **Upgradeable proxy patterns** using ERC-7201 namespaced storage for safe upgrade paths
- **OpenZeppelin AccessControlDefaultAdminRules** for role-based permissioning with delayed admin transfers in the Treasury and YieldDistributor
- **Ownable2Step** for the PeggedToken and StakingVault for streamlined single-owner management

---
description: Core Ethereum smart contract architecture.
---

# Smart Contracts

The core Ethereum contracts are implemented in **Solidity 0.8.30**.

## Core Contracts

### PeggedToken

ERC-20 with ERC-20Permit (gasless approvals), ERC-20Burnable, Ownable2Step ownership, address blacklisting, and designated Gateway/Treasury integration points. This contract serves as the template for VUSD, vetBTC, and vetETH.

### Gateway

Handles swap-ins, minting, redemption, and swap-outs with:
- Configurable fees and mint limits
- Slippage protection
- Multi-step redemption process with a governance-configurable security delay for standard users
- Instant redemption for whitelisted market makers against the Treasury buffer
- AMO mint limit enforcement

### Treasury

Manages collateral custody with:
- Per-token configuration (vault, oracle, staleness period, swap-in/swap-out toggles)
- Decentralized price feed integration with configurable tolerance bounds
- Keeper and UMM (Universal Mint Module) role separation
- Swapper integration for internal rebalancing
- OpenZeppelin AccessControlDefaultAdminRules for role-based permissioning

### StakingVault

ERC-4626 compliant vault implementing the sVUSD variable yield product. Features:
- Governance-configurable cooldown period for withdrawals (7 days → 1 day)
- Instant withdrawal whitelist for approved addresses
- Integration with the YieldDistributor for drip-based reward delivery

### YieldDistributor

Linearly drips yield to the StakingVault over a configurable duration to prevent yield sniping. When new yield is added, remaining undistributed yield is combined with the new amount and redistributed linearly — ensuring smooth price-per-share appreciation.

## Source Code

| Resource | Link |
|----------|------|
| GitHub Repository | [vetro-protocol/vetro-contracts](https://github.com/vetro-protocol/vetro-contracts) |
| Contract Source | [/src](https://github.com/vetro-protocol/vetro-contracts/tree/main/src) |
| Documentation | [/docs](https://github.com/vetro-protocol/vetro-contracts/tree/main/docs) |
| Operations Runbook | [OPERATIONS.md](https://github.com/vetro-protocol/vetro-contracts/blob/main/docs/OPERATIONS.md) |
| StakingVault & YieldDistributor Spec | [StakingVault-YieldDistributor-Spec.md](https://github.com/vetro-protocol/vetro-contracts/blob/main/docs/StakingVault-YieldDistributor-Spec.md) |

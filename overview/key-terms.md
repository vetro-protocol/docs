---
description: Definitions for protocol-specific terminology used throughout this documentation.
---

# Key Terms

| Term | Definition |
|------|-----------|
| **VUSD** | The protocol's primary settlement asset. A dollar-referenced, over-collateralized protocol-generated asset targeting a 1:1 value relationship with the US dollar. |
| **sVUSD** | The protocol's variable yield product. Users stake VUSD into sVUSD and receive yield in exchange for a cooldown period before withdrawal. |
| **VUSDx** | The protocol's fixed-term, fixed-rate product. Users lock VUSD for an epoch duration and receive a guaranteed yield at maturity. |
| **VETRO (V)** | The protocol's governance token. Can be locked to receive veVETRO. |
| **veVETRO** | Vote-escrowed VETRO. Locking V for a chosen duration produces veVETRO, which grants voting power and a share of protocol revenue. Longer locks produce more voting power. |
| **AMO** | Automated Monetary Operations. An algorithmic controller that maintains the VUSD peg on DEXs by adjusting protocol-owned liquidity in response to price deviations. |
| **CDP** | Collateralized Debt Position. A borrowing mechanism where users deposit crypto assets as collateral and borrow VUSD against them. |
| **Agentic Yield Engine** | The protocol's proprietary multi-agent autonomous system. Specialized AI agents evaluate, curate, and recommend risk-adjusted capital allocation across DeFi protocols, subject to human-in-the-loop authorization. |
| **Lazy Yield** | The surplus yield created when VUSD circulates for settlement or payments rather than being staked into sVUSD or VUSDx. Revenue flows to the protocol treasury. |
| **LayerZero OFT** | Omnichain Fungible Token. The cross-chain standard used by VUSD to enable native representation across 100+ blockchain networks without wrapping or bridging intermediaries. |
| **Redemption Buffer** | A liquid reserve held within the Treasury, outside of yield strategies, to fulfill instant redemption requests and support peg stability. |
| **StableFi** | Vetro's product framework for yield-bearing digital asset infrastructure built on top of settlement-grade base assets. |
| **vet Primitive** | The extensible template that powers all Vetro assets (vetBTC, vetETH, etc.) — a base settlement token paired with optional yield variants. |
| **Guardians** | Protocol overseers with emergency powers including a global bot kill-switch, CDP budget freeze, and drip freeze capabilities. |

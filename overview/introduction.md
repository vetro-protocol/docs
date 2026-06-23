---
description: Why Vetro was built and the problem it solves.
---

# Introduction

## The Problem

The digital dollar settlement market has grown from a niche DeFi tool to a $300B+ asset class, yet the infrastructure supporting this growth remains fragmented, opaque, and poorly suited for institutional adoption.

Institutions managing protocol-generated dollar asset positions face compounding operational challenges:

- Assets scattered across dozens of blockchains with different bridging mechanisms and risk models
- Reserve backing that varies wildly between issuers
- Yield opportunities that require manual coordination across multiple protocols
- A false trade-off between safety (holding non-productive assets) and yield (deploying into opaque DeFi protocols)

The result is billions of dollars in **lazy capital** that earns nothing for its holders while the underlying collateral generates yields captured entirely by the issuer.

## The Core Thesis

Vetro begins from a different premise: the future of programmable money does not require inventing new financial instruments — it requires restoring settlement discipline to new rails.

A protocol-generated dollar asset should function as a settlement-grade instrument: predictable, transparent, and honest about its risk profile. Yield is valuable, but it must be a **conscious choice**, not an embedded default.

## Three Architectural Commitments

### 1. Separation of Stability and Yield

The yield-bearing products (sVUSD and VUSDx) operate as a distinct layer on top of the base settlement asset. That layer can be paused or disabled without affecting VUSD's core issuance, redemption, or peg mechanics.

### 2. Transparency as Infrastructure

All reserve allocations, yield distributions, and governance decisions are verifiable on-chain in real time. The Vetro Trust Center provides continuous evidence of backing ratios.

### 3. Omnichain by Default

VUSD is architected for cross-chain settlement from inception using LayerZero's Omnichain Fungible Token (OFT) standard, enabling transfers across 100+ networks without fragmented liquidity.

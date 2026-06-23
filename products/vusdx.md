---
description: VUSDx is the protocol's fixed-term, fixed-rate yield product.
---

# VUSDx

VUSDx provides predictable, fixed-rate yields through an epoch-based design. Users lock VUSD for the epoch duration and receive a guaranteed yield at maturity.

## Epoch Lifecycle

Each epoch follows this structure:

| Phase | Day |
|-------|-----|
| Deposit window open | Day 0 |
| Locked — yield accrues | Days 1–23 |
| Exit window (7 days) | Days 23–29 |
| Payout / auto-rollover | Day 30 |

Each epoch has a published fixed rate, a deposit cap (with a "sold out" state), and automatic rollover enabled by default. Exit requires user action during the exit window.

## Yield Sourcing

Fixed yield is sourced through forward yield rate locking mechanisms at epoch initialization — specifically via purchasing Pendle Protocol's Principal Tokens (PT). A safety buffer is maintained between the locked rate and the advertised VUSDx rate to absorb market movements.

Mid-epoch deposits receive a reduced "gap rate" to prevent late-entry arbitrage.

## Protocol Rationale

VUSDx provides the strongest stability primitive in the protocol:

- **Deterministic Deployment Horizon**: Fixed-term locks give the Treasury absolute certainty over reserve asset commitments, enabling access to the longest-duration, highest-yielding institutional strategies
- **Peg Integrity Floor**: Aggregating a significant portion of VUSD into fixed epochs creates an enduring "sticky TVL" floor that absorbs broader market shocks

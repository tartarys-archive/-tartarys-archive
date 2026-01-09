# Corvina Ledger — Entry 0003

## Title
Smart Contract Scope Defined (v1)

## Date
2026-01-09

## Summary
The functional and ethical scope of the first Corvina Sigil Jeton smart contract (v1) has been defined.
The contract is intentionally minimal, demonstrative, and auditable.

## Contract Purpose
- Demonstrate Corvina Sigil minting through physical archive-backed proof
- Enable a single, controlled minting event
- Preserve full transparency and reversibility at the governance layer (not on-chain)

## Core Principles
- Simplicity over feature-completeness
- One-time minting demonstration
- Human accountability over automated complexity
- Pause-enabled to prevent unintended actions

## Functional Scope (v1)

### Included
- Token deployment (ERC-20 compatible on BNB Smart Chain)
- Fixed initial supply (369,000 CSJ)
- Minting authority restricted to Founder wallet
- Ability to pause minting permanently after first mint
- Transfer functionality enabled (post-mint distribution)

### Explicitly Excluded
- No automated future minting
- No burn mechanism
- No on-chain rarity logic
- No oracle integrations
- No governance voting
- No upgradeability proxy

## Governance Alignment
- All standards (CK WP v1, CST, Y-B, Corvina Sigil Standard) are custodially governed off-chain
- Smart contract enforces rules, but does not replace human oversight
- Ledger entries serve as ethical and historical anchor

## Status
Scope frozen for v1 implementation

## Ledger Integrity
This entry is immutable and recorded as part of the Corvina Ledger.

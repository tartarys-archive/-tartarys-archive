# Corvina Ledger — Entry 0006

## Title
Wallet Roles and Key Separation

## Date
2026-01-09

## Purpose
This entry defines the wallet architecture and key separation principles
used in Corvina Keepers v1, ensuring operational clarity, security,
and future auditability.

The objective is to minimize trust assumptions while preserving
founder-led responsibility during the initial phase.

## Core Principle

**One role — one wallet — one responsibility.**

No wallet shall serve multiple logical roles.

## Defined Wallet Roles (v1)

### 1. Founder / Minter Wallet

**Purpose**
- Deploy the CSJ smart contract
- Execute the single authorized minting event
- Initiate the pause function after minting

**Properties**
- Human-controlled
- High responsibility
- Temporarily privileged

**Restrictions**
- No treasury custody
- No long-term asset accumulation role

This wallet represents *intent*, not storage.

---

### 2. Treasury Wallet

**Purpose**
- Receive minted Corvina Sigil Jetons
- Hold community and founder allocations
- Act as the distribution source to early Keepers

**Properties**
- Separate address from Founder
- Publicly known
- Ledger-documented inflows and outflows

**Restrictions**
- No minting authority
- No contract upgrade rights

This wallet represents *custody*, not authority.

---

### 3. Personal / Participant Wallets (Future)

**Purpose**
- Receive CSJ allocations
- Hold or transfer tokens
- Represent individual Keepers

**Properties**
- Controlled by participants
- Not trusted with protocol-level actions

These wallets represent *ownership*, not governance.

## Key Separation Rules

- No private key is shared between roles
- No role is accessed from multiple wallets
- Seed phrases are stored offline
- Wallet creation events are logged

## Rationale

### Security
Compromise of one wallet does not imply compromise of the system.

### Transparency
Observers can distinguish:
- who acted
- in what capacity
- using which authority

### Governance Readiness
This separation allows future transition to:
- multisig
- role reassignment
- Keeper-elected controls

without rewriting history.

## Explicit Non-Goals (v1)

- No multisig enforcement
- No DAO mechanics
- No automated governance

These are deferred intentionally to v2+.

## Forward Compatibility

The defined roles are designed to be:
- mapped into multisig wallets
- delegated by Keeper consensus
- partially or fully revoked

with minimal disruption.

## Status
Wallet role separation is mandatory and active for v1.

## Ledger Integrity
This architecture forms a foundational invariant
for all future Corvina Keepers operations.

# Corvina Ledger — Entry 0007

## Title
Smart Contract Functional Scope (CSJ v1)

## Date
2026-01-09

## Purpose
This entry defines the exact functional scope of the
Corvina Sigil Jeton (CSJ) smart contract v1.

The goal is to keep the contract:
- minimal
- auditable
- demonstrative
- resistant to misuse

v1 is intentionally limited to establish trust through clarity.

## Design Philosophy

**Do less, but do it perfectly.**

The v1 smart contract exists to:
- prove the minting model
- demonstrate allocation logic
- anchor the ledgered process on-chain

It is not designed to optimize, automate, or scale.

## Core Contract Properties

### Token Standard
- ERC-20 compatible (BNB Chain)
- Decimals: 0
- Symbol: CSJ
- Name: Corvina Sigil Jeton

### Supply Model
- Single mint event
- Total supply defined at deployment or mint
- No inflation after mint

Supply is finite by contract design.

## Functional Capabilities (Enabled)

### 1. Mint (Single-Use)

**Description**
- One authorized minting transaction
- Executed by Founder / Minter wallet
- Tokens minted to Treasury wallet

**Constraints**
- Minting callable only once
- Subsequent calls are rejected

This models the first archival + minting ceremony.

---

### 2. Transfer

**Description**
- Standard ERC-20 transfers enabled
- Allows distribution to early Keepers

**Constraints**
- No restrictions on recipient type
- No whitelist in v1

This enables real-world testing of circulation.

---

### 3. Pause (Partial)

**Description**
- Pause functionality enabled
- Affects minting only

**Important**
- Transfers remain active
- Balances remain accessible

Pause is a *minting brake*, not a system freeze.

---

### 4. Ownership / Admin

**Description**
- Contract has an owner role
- Owner controls pause
- Owner cannot mint after mint event

Ownership exists for responsibility, not control.

## Functional Capabilities (Explicitly Disabled)

The following are **not present** in v1:

- ❌ Burn
- ❌ Multi-mint
- ❌ Upgradeability
- ❌ Role delegation
- ❌ Fee mechanics
- ❌ On-chain governance
- ❌ Blacklists / freezes
- ❌ Multisig enforcement

Absence is intentional.

## Security Considerations

### Reduced Attack Surface
Fewer functions → fewer vectors.

### Predictability
Every possible state change is known in advance.

### Audit Simplicity
The contract can be reviewed line-by-line
by non-specialist observers.

## Relationship to Ledger

Each on-chain action must correspond to:
- a prior ledger entry
- a documented intention
- a timestamped commit

No contract action stands alone.

## Forward Compatibility

This contract is designed to be:
- referenced, not replaced
- archived, not modified
- used as a template for future versions

v2+ contracts may introduce:
- multisig
- multiple mint events
- differentiated allocations

but v1 remains immutable.

## Status
Functional scope finalized for CSJ v1.

## Ledger Integrity
This entry locks the functional boundaries
of the first Corvina Sigil smart contract.

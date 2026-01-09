# Corvina Ledger — Entry 0005b

## Title
Testnet vs Mainnet Decision — Controlled Mainnet Deployment

## Date
2026-01-09

## Purpose
This entry records the decision regarding the deployment environment
for the first Corvina Sigil Jeton (CSJ) smart contract.

The goal is to balance safety, clarity, and real-world demonstrability.

## Definitions

- Testnet:
  A public blockchain environment using valueless test tokens,
  intended for development and experimentation.

- Mainnet:
  A production blockchain where transactions have real economic cost
  and permanent consequences.

## Decision

The Corvina Sigil Jeton v1 smart contract SHALL be deployed directly
to the BNB Smart Chain **mainnet**, with strict functional limitations.

## Rationale

### 1. Demonstrability Over Simulation
- Corvina Keepers is built around physical custody, real archives,
  and irreversible commitments.
- A testnet simulation does not adequately reflect these realities.

### 2. Controlled Scope Reduces Risk
- CSJ v1 supports:
  - a single, intentional minting event
  - transfer functionality
  - emergency pause (minting only)
- No automated loops, no external dependencies.

### 3. Economic Signal Integrity
- Mainnet deployment ensures that:
  - every transaction carries intent
  - every action has cost
  - no action is “just a test”

### 4. Auditability and Trust
- Observers, contributors, and future Keepers
  can verify actions on a public, permanent ledger.

## Risk Mitigation Measures

- Minimal contract surface
- Single mint authority
- Immediate pause after minting
- Separate treasury address
- Public Corvina Ledger documentation

## What This Decision Is NOT

- Not a rejection of testing best practices
- Not a shortcut
- Not an encouragement of reckless deployment

Testnet experimentation MAY be used for future versions,
but the founding act requires reality, not rehearsal.

## Forward Policy

Future contracts MAY:
- be tested on testnets first
- use formal audits
- expand functionality incrementally

Each step must be logged in the Corvina Ledger.

## Status
Mainnet deployment approved for CSJ v1 under controlled conditions.

## Ledger Integrity
This decision is final for v1 and recorded immutably.

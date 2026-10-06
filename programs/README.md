# Solana Programs

## Status: In Development

SYNAPZ is actively developing Solana programs (Anchor framework) for the following use cases. Source code will be published here when ready for public review.

---

## Planned Programs

### 1. Governed Execution Registry
**Purpose:** On-chain immutable record of governed AI decisions made by the SYNAPZ GCL (Governed Capability Layer).

**Function:**
- Log approved AI actions with policy version, approver signature, and outcome hash
- Provide a verifiable on-chain audit trail for autonomous AI operations
- Enable third-party verification of SYNAPZ AI governance compliance

**Status:** Architecture complete. Anchor implementation planned Q4 2026.

---

### 2. KYRO Release Registry
**Purpose:** On-chain registry of KYRO autonomous artist releases.

**Function:**
- Record each KYRO release with metadata hash, mint address, and governance gate proof
- Link SPL token-gated access to specific KYRO release tiers
- Support compressed NFT (cNFT) edition drops at scale

**Status:** Design stage. Dependent on KYRO Solana migration (Q4 2026).

---

### 3. SPL Token Launcher (Governed)
**Purpose:** Governed SPL token deployment with policy gating before any on-chain action.

**Function:**
- Deploy SPL tokens with configurable authority, supply, and metadata
- All deployments require GCL approval gate before execution
- Integrated with SYNAPZ governance dashboard

**Status:** In active development.

---

## Shared Project Repository

For existing public Solana utility code from the SYNAPZ team, see:

**[github.com/Synapz-group/solana-wire-codec](https://github.com/Synapz-group/solana-wire-codec)**

> Solana address/signature Base58 encoding and exact integer decoding utilities (MIT licensed)

---

*Anchor programs will be published here under a proprietary licence when ready for review.*

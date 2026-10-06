# SYNAPZ Platform Architecture Overview

> This is a high-level public overview. Production infrastructure details are not disclosed here.

---

## Core Layers

```
┌─────────────────────────────────────────────────────────────┐
│                    SYNAPZ AI Platform                        │
├─────────────────────────────────────────────────────────────┤
│  Governed Capability Layer (GCL)                            │
│  ├── Policy Engine          — evaluates action contracts     │
│  ├── Approval Controller    — human-in-the-loop gates        │
│  ├── Research Broker        — intelligence gathering         │
│  └── Audit Logger           — immutable decision record      │
├─────────────────────────────────────────────────────────────┤
│  Solana Execution Layer                                      │
│  ├── Flywheel v3            — 4-state trading strategy       │
│  ├── MMV2                   — isolated market-maker stack    │
│  ├── MEV Copy Executor      — sniper/copy-trade executor     │
│  ├── Holder Intel Service   — wallet classification + KOL    │
│  └── Baby PURK (BPURK)     — Solana market-maker pressure   │
├─────────────────────────────────────────────────────────────┤
│  Creative AI Layer                                           │
│  ├── KYRO Genesis Engine    — autonomous artist pipeline     │
│  ├── Creative Director      — governed multi-gate creative   │
│  └── NFT Engine             — mint, royalty, collection mgmt │
├─────────────────────────────────────────────────────────────┤
│  Infrastructure                                              │
│  ├── synapz-ai-01           — dedicated production server    │
│  ├── Governance Dashboard   — real-time approval UI          │
│  └── ANGEL                  — health monitoring agent        │
└─────────────────────────────────────────────────────────────┘
```

---

## Governance Model

All autonomous actions taken by SYNAPZ systems pass through the **Governed Capability Layer (GCL)** before execution:

1. **Action Contract** — agent proposes an action with typed parameters
2. **Policy Evaluation** — GCL evaluates against configured policy rules
3. **Approval Gate** — human approver (Lee / Dathan Eldridge) reviews and approves/rejects
4. **Execution** — action executes only after gate passes
5. **Audit Log** — outcome written to immutable audit trail

This governance pattern applies to trading decisions, creative releases, token operations, and all production deployments.

---

## Solana Integration Points

| Component | Integration |
|-----------|-------------|
| Flywheel v3 | Solana mainnet RPC, SPL token ops, DEX routing |
| MMV2 | Solana mainnet, liquidity provision |
| MEV Copy Executor | Solana transaction monitoring, mempool-aware execution |
| Holder Intel | On-chain wallet analysis, token holder classification |
| KYRO NFT releases | EVM today; Solana migration planned Q4 2026 |
| SPL Token Launcher | Governed SPL launch with policy gate (in progress) |

---

## Technology Stack (Public)

- **Runtimes:** Node.js, Python 3
- **Solana:** `@solana/web3.js`, Anchor framework (planned), Jito MEV SDK
- **Governance:** Custom policy engine (TypeScript)
- **Infra:** Dedicated Linux server, systemd-managed services
- **Monitoring:** Custom health agent (SYNAPZ ANGEL)

---

*Architecture details are indicative. Production specifics are confidential.*

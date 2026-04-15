# zivana-core

On-chain smart contract layer for the Zivana Protocol, written in 
[Aiken](https://aiken-lang.org/) and deployed on the Cardano blockchain.

This repository contains the validators and minting policies that make 
the Zivana Protocol's economic guarantees enforceable at the protocol 
level — not by policy, not by a company's server, but by mathematics 
that runs the same way for everyone.

---

## What lives here

| Contract | Purpose |
|---|---|
| Distribution validator | Executes atomic 4-output value splits triggered by oracle-attested revenue events |
| $ZVN minting policy | One-time fixed supply mint — no inflation, no additional issuance ever |
| Vesting contract | Time-locked release of team and contributor token allocations |
| Treasury contract | Receives protocol fees, manages Community Access Fund sub-allocation |
| Staking contract | Enforces $ZVN stake requirements for sequencer and oracle node operators |
| Governance contract | On-chain proposal submission, voting, and parameter change execution |

---

## Protocol Context

`zivana-core` is one layer of the Zivana Protocol stack:

Cardano (zivana-core)     ← settlement, distribution, token

Midnight (zivana-midnight) ← shielded state, ZK proofs, covenants

Identus (zivana-identity)  ← DID credentials, verifiable attestations

Full protocol documentation: [zivana-docs](https://github.com/zivana-labs/zivana-docs)

---

## Development Status

> Phase 0 — Environment verification and primitive prototyping

This repository is under active early development. No production 
contracts have been deployed. All validators are being built and 
tested on Cardano preprod testnet before any mainnet deployment.

---

## Getting Started

Prerequisites:
- [Aiken](https://aiken-lang.org/) — install via the official guide
- [Blockfrost API key](https://blockfrost.io/) — preprod network

```bash
# Clone the repository
git clone https://github.com/zivana-labs/zivana-core.git
cd zivana-core

# Build contracts
aiken build

# Run tests
aiken check
```

Full setup guide: coming in Phase 0 documentation.

---

## Contributing

Read the [contributing guidelines](https://github.com/zivana-labs/.github/blob/main/CONTRIBUTING.md) 
before opening a pull request. All PRs target the `develop` branch.

## Licence

MIT — see [LICENSE](./LICENSE)

---

*Part of [Zivana Labs](https://github.com/zivana-labs) — 
built for Africans, open to the world.*

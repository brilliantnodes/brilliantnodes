# Brilliant Nodes

We mine new proof-of-work and useful-work networks from their first block, and we build the nodes and tools those networks need early on.

## What we run
- **A rented mining fleet** of GPUs and CPUs across Vast.ai, Clore.ai, Salad and OctaSpace, plus rented hashrate where an algorithm allows it. The fleet has passed 100 machines.
- **Our own launch tooling**: a radar that watches upcoming launches, release checks with pinned and hash-verified miner builds, and launch-day automation that starts machines from block 0.
- **Network infrastructure**: Stratum hub nodes on Zycord; seed nodes and a hardened pool on Tenero's test network.
- **Contract work**: hash time-locked swap contracts for trustless ZCD ↔ USDT trades, tested on Zycord's testnet (216 tests). Not yet public; they will be published with their review reports before any real use.

## Built on GenLayer
Intelligent contracts where validators read real-world sources and code decides, each with a live site, public repo and testnet evidence:
- **[PrivateCreditGate](https://privatecredit.brilliantnodes.com)**: a covenant-gated credit facility. Validators read the borrower's published compliance report; code applies leverage, cover and cash tests, margin grid, equity cure, events of default and payouts. Run end to end on Studio and Testnet Bradbury. [Repo](https://github.com/brilliantnodes/privatecredit-gate)
- **[RigSettle](https://rigsettle.brilliantnodes.com)**: settles GPU rental disputes from the pool's own hashrate page. [Repo](https://github.com/brilliantnodes/rigsettle)
- **[Launch Claim Checker](https://checker.brilliantnodes.com)**: checks a coin launch's public claims. [Repo](https://github.com/brilliantnodes/launch-claim-checker)
- **[genlayer-patterns](https://github.com/brilliantnodes/genlayer-patterns)**: reusable contracts (MeterReader, RuleCheck) with exact-agreement validators.

## What we are building next
**QUBO Bench** (planned) — open tools for miners on [QMS Network](https://qms.finance), whose miners solve optimisation (QUBO) problems:
1. a GPU benchmark and a reference solver, so miners can test hardware before mining opens;
2. a public network monitor: block times, difficulty, solver mix, node count;
3. seed nodes in three regions.

The tools will be free and open source.

## How we work
- Miners and clients run only on rented, isolated machines.
- We use only documented public endpoints.
- Keys and seed phrases are kept offline.
- We publish what we have tested, and say what we have not.

## Contact
- E-mail: brilliantnodes@proton.me
- Bitcointalk: brilliantnodes
- Founder: Petros Mylonas

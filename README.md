# Brilliant Nodes

We mine new proof-of-work and useful-work networks from their first block, and we build the nodes and tools those networks need early on.

## What we run
- **A rented mining fleet** of GPUs and CPUs across Vast.ai, Clore.ai, Salad and OctaSpace, plus rented hashrate where an algorithm allows it. The fleet has passed 100 machines.
- **Our own launch tooling**: a radar that watches upcoming launches, release checks with pinned and hash-verified miner builds, and launch-day automation that starts machines from block 0.
- **Network infrastructure**: Stratum hub nodes on Zycord; seed nodes and a hardened pool on Tenero's test network.
- **Contract work**: hash time-locked swap contracts for trustless ZCD ↔ USDT trades, tested on Zycord's testnet (216 tests). Not yet public; they will be published with their review reports before any real use.

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

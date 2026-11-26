# Brilliant Nodes

**Website: [www.brilliantnodes.com](https://www.brilliantnodes.com)**

We mine new proof-of-work and useful-work networks from their first block, and we build the nodes and tools those networks need early on.

## What we run
- **A rented mining fleet** of GPUs and CPUs across Vast.ai, Clore.ai, Salad and OctaSpace, plus rented hashrate where an algorithm allows it. The fleet has passed 100 machines.
- **Our own launch tooling**: a radar that watches upcoming launches, release checks with pinned and hash-verified miner builds, and launch-day automation that starts machines from block 0.
- **Network infrastructure**: Stratum hub nodes on Zycord; seed nodes and a hardened pool on Tenero's test network.
- **Contract work**: hash time-locked swap contracts for trustless ZCD ↔ USDT trades, tested on Zycord's testnet (216 tests). Not yet public; they will be published with their review reports before any real use.

## Built on GenLayer
Intelligent contracts where validators read real-world sources and code decides, each with a live site, public repo and testnet evidence:
- **[AuctionDeposit](https://brilliantnodes.github.io/auction-deposit/)**: a safe way to put down a bid deposit at a property auction. Every bidder's deposit waits in one escrow and moves only on what validators read on the official auction record: unsuccessful bidders are refunded, the winner's deposit goes to the creditor as part of the price or as the penalty, and a cancelled or suspended auction refunds everyone. Nearly 300,000 property auctions are waiting in Greece, and only about 1 in 5 succeeds. Ten fictional auctions ran live on GenLayer Studio and Testnet Bradbury (78 transactions on Bradbury, all finalized). [Try it yourself](https://brilliantnodes.github.io/auction-deposit/app/), [article](https://brilliantnodes.github.io/auction-deposit/article.html), [repo](https://github.com/brilliantnodes/auction-deposit), [video](https://youtu.be/1UPPTYSIinM)
- **[PrivateCreditGate](https://privatecredit.brilliantnodes.com)**: a covenant-gated credit facility. Validators read the borrower's published compliance report; code applies leverage, cover and cash tests, margin grid, equity cure, events of default and payouts. Five fictional borrowers run end to end on Studio and Testnet Bradbury: 129 live transactions, identical readings on both. [Repo](https://github.com/brilliantnodes/privatecredit-gate), [video](https://youtu.be/d7g2sU8bzn0)
- **[ClaimEscrow](https://claims.brilliantnodes.com)**: a safe way to buy and sell bankruptcy claims. When a company goes bust, the people it owes can sell their right to be paid; ClaimEscrow holds the buyer's money and pays the seller only when the public list of the company's debts shows the sale went through. Bankruptcy claims are one part of litigation funding, about $25bn in 2025. Nine fictional deals ran live on GenLayer Studio (67 calls) and Testnet Bradbury (70 transactions), all finalized. [Try it yourself](https://claims.brilliantnodes.com/app/), [repo](https://github.com/brilliantnodes/claim-escrow), [video](https://www.youtube.com/watch?v=MFiW9LkCT1s)
- **[RigSettle](https://rigsettle.brilliantnodes.com)**: settles GPU rental disputes from the pool's own hashrate page. [Repo](https://github.com/brilliantnodes/rigsettle)
- **[Launch Claim Checker](https://checker.brilliantnodes.com)**: checks a coin launch's public claims. New: [claim bounties](https://checker.brilliantnodes.com/bounties.html), GEN held behind a claim that pays the first person who shows, on the pinned explorer pages, that the claim is false. [Repo](https://github.com/brilliantnodes/launch-claim-checker)
- **[genlayer-patterns](https://github.com/brilliantnodes/genlayer-patterns)**: reusable contracts with exact-agreement validators: MeterReader, RuleCheck and, new, **[ReportReader](https://github.com/brilliantnodes/genlayer-patterns/tree/main/report-reader)**: company report figures that contracts can trust. It turns a company's published report into exact on-chain figures, with an earn-out escrow that pays only on readings the network has finalized.

## Validator tooling
- **[gno-node-tools](https://github.com/brilliantnodes/gno-node-tools)**: keeps a gno.land validator running through every coordinated upgrade. gno.land mainnet stopped for an upgrade 5 times between 14 September and 18 November 2026, and its testnet Onyx 3 times since 28 September; at each stop every validator must switch to the new release at exactly the right block. The tool makes the switch, checks the node before an upgrade, and alerts only when something is really wrong. Python standard library only, MIT licence, 70 automated tests, three independent reviews. Since 25 November 2026 it runs our own Onyx node in Tokyo; it has not yet taken a node through a real coordinated halt, and Onyx's next upgrade will be the first.

## Contributions to the networks we validate
- **gno.land, [pull request #6533](https://github.com/gnolang/gno/pull/6533)** (in review): adds a section on coordinated upgrades to the gno.land mainnet and Onyx testnet validator guides, so every operator can take a node through an upgrade cleanly. Before the chain stops at the agreed block: install the new release and check it against its published checksums, and make sure no leftover stop height sits in the node's settings. At the stop: recognise it from the log, then switch versions with only one copy of the validator ever running. The chain restarts only once validators holding more than two thirds of the voting power have switched, so every validator that switches promptly helps it restart sooner. Written from running our own Onyx node through the 17 November upgrade; [gno-node-tools](https://github.com/brilliantnodes/gno-node-tools) automates the same steps.

## What we are building next
**QUBO Bench** (planned) — open tools for miners on [QMS Network](https://qms.finance), whose miners solve optimisation (QUBO) problems:
1. a GPU benchmark and a reference solver, so miners can test hardware before mining opens;
2. a public network monitor: block times, difficulty, solver mix, node count;
3. seed nodes in three regions.

The tools will be free and open source.

**Canton Network**: validator application submitted on 25 November 2026. DevNet onboarding in progress on a dedicated server.

## How we work
- Miners and clients run only on rented, isolated machines.
- We use only documented public endpoints.
- Keys and seed phrases are kept offline.
- We publish what we have tested, and say what we have not.

## Contact
- E-mail: brilliantnodes@proton.me
- Bitcointalk: brilliantnodes
- Founder: Petros Mylonas

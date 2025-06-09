# Blockchain Fundamentals

## What is Blockchain?

A blockchain is a distributed, tamper-resistant ledger that records transactions in a sequence of linked blocks. Each block contains:
- A list of transactions or data entries
- A timestamp of block creation
- A cryptographic hash of the block contents
- A reference to the previous block's hash

Because all nodes store the same data, and any modification breaks the hash chain, blockchains ensure data integrity without a central authority. This enables trustless collaboration, where all participants can independently verify the ledger's consistency.

## Real-Life Use Cases

### Supply Chain Management

Track goods from manufacturer to distributor to retailer with verified authenticity and origin at every stage.

### Digital Identity

Enable self-sovereign identities by allowing users to manage and share verifiable credentials without centralized control.

## Merkle Root and Data Integrity

A Merkle Root is a hash summarizing all transactions in a block:
- Hash individual transactions
- Pair the hashes and rehash until a single root hash remains

If any transaction changes, its hash and the resulting Merkle root will change. Merkle proofs allow fast verification of a transaction’s inclusion using only a few hashes, making the process efficient and scalable.

## Consensus Mechanisms

### Proof of Work (PoW)

Miners solve a cryptographic puzzle by finding a nonce such that:


Key features:
- High energy consumption
- Secures the network through computational cost
- Example: Bitcoin

Bitcoin miners consume hundreds of terawatt-hours annually to secure the network.

### Proof of Stake (PoS)

Validators stake funds to earn the right to propose the next block. A validator is selected based on stake amount and lock-up duration. Malicious behavior can result in loss of staked funds (slashing).

Key features:
- Low energy usage
- Uses economic penalty instead of computation
- Example: Ethereum after The Merge

Ethereum reduced its energy usage by over 99% after transitioning to PoS.

### Delegated Proof of Stake (DPoS)

Token holders vote to elect a small set of validators. These elected delegates take turns creating blocks.

Key features:
- Fast block times and high throughput
- Fewer validators increases centralization
- Example: EOS

EOS uses 21 elected block producers, achieving block times of 0.5 seconds.

## Summary

| Consensus | Energy Usage | Decentralization | Finality Speed | Example  |
|-----------|--------------|------------------|----------------|----------|
| PoW       | High         | High             | Slow           | Bitcoin  |
| PoS       | Low          | Moderate         | Moderate       | Ethereum |
| DPoS      | Very Low     | Lower            | Fast           | EOS      |


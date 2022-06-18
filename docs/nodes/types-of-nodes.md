---
id: 'Types of Nodes'
---

# Telos Block Producer Nodes
### Getting Started with Telos Nodes
This section discusses Telos Nodes and the role they play in the Telos blockchain network.

Telos Blockchain Network is an EOSIO-based blockchain network. Therefore, everything that is required to run EOSIO-based blockchain nodes, applies to Telos. Telos makes use of EOSIO platform spesific components and libraries (`nodeos`, `cleos`, `keosd`, `EOSIO.CDT`, and `EOSJS`) to operate blockchain nodes, collect blockchain data, interact with nodes, and to build smart contracts.

The main component of the Telos blockchain network is `nodeos` (node + EOSIO). `nodeos` is the core node daemon installed on all the hardware that wants to become a node in the network. Each node can be configured (with spesific functional plugins) to function as a:
1. Producing node, or
2. Non-producing node.

## Producing nodes
Prducing nodes are configured for block production. They connect to the Telos peer-to-peer network and activly produce new blocks. Producing nodes produce blocks on the mainnet if they are an assigned producer as part of the active block producing schedule.

## Non-producing nodes
Non-producing nodes also connect to the Telos peer-to-peer network, but they do not actively produce blocks. Non-producing nodes are useful to act a proxy nodes, relaying API calls (API endpoints), validating transactions, and broadcasting information to other nodes. Non-producing nodes are also useful for monitoring the blockchain state. Nodeos enables you to set up a device for local development as a single node blockchain network.





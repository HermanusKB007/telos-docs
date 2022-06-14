---
id: Installing client software
---
# Getting strarted with 🚀 Telos Nodes!
This section have been adopted from [EOSIO developer documentation].(https://developers.eos.io/manuals/eos/latest/index).

Teelos blockchain network is build on the EOSIO platform. The EOSIO platform provides the components required to operate a Telos node, to collect blockchain data, to interact with nodes, and to build smart contracts.

The main components of the EOSIO platform is:
1. `nodeos` (node + EOSIO) that is configured to run a node (as a block producer, as dedicated API endpoints and local development)
2. `cleos` (CLI + EOSIO) is a command line interface used to interact with `nodeos`, allowing you the send commands and actions to a blockchain.
3. `keos` (key + EOSIO) is a local component that stores and manages EOSIO keys in wallets and provides a secrure enclave for digital signing.





## Nodeos, Cleos, and Keosd
### Nodeos
Nodeos is the core EOSIO node daemon. Nodeos handles the blockchain data persistence layer, peer-to-peer networking, and contract code scheduling. For development environments, nodeos enables you to set up a single node blockchain network.


Nodeos is the core service daemon that runs on every Telos Node. Nodeos can be configured to process smart contracs, validate transactions, produce blocks and confirm blocks to record them on the blockchain.

Nodeos is distributed as part of the EOSIO software suite. You can download [Nodeos](https://developers.eos.io/manuals/eos/latest/install/index) here. We recommend installing the EOSIO Prebuilt Binares is you are new to EOSIO-based blockchain networks like Telos.

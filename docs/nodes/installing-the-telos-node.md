---
id: Installing client software
---
# Installing `nodeos` 🚀 - Telos Nodes!
This section have been adopted from [EOSIO developer documentation](https://developers.eos.io/manuals/eos/latest/index).

In the previous section we introduced the two different modes `nodeos` can be configured to operate as:
1. Block producing node, and
2. Non-producing node.

In this section, instructions will be provided to help you get started as a producing node or non-producing node.

Telos blockchain network is build on the EOSIO platform. The EOSIO platform provides the components required to operate a Telos node, to collect blockchain data, to interact with nodes, and to build smart contracts.

The main components required to run the Telos blockchain network (or any EOSIO-based blockchain) is:
1. `nodeos` (node + EOSIO) that is configured to run a node (as a block producer, as dedicated API endpoints and local development)
2. `cleos` (CLI + EOSIO) is a command line interface used to interact with `nodeos`, allowing you the send commands and actions to a blockchain.
3. `keos` (key + EOSIO) is a local component that stores and manages EOSIO keys in wallets and provides a secrure enclave for digital signing.

As a developer, to build smart contracts you need `EOSIO.CDT`. `EOSIO.CDT` generates `WebAssembly` binary instructions or `bytecode` into `wasm` files. The generated `wasm` files are the smart contracts which can be deployed to Telos blockchains. EOSIO provides a frontend library for Javascript development called `EOSJS`. `EOSJS` API SDK integrates with EOSIO-based blockchains using the EOSIO RPC API. EOSIO also provides Swift and Java SDKs for native mobile application development.

To get started as a developer, you need to [prepare your development environment](https://developers.eos.io/welcome/latest/getting-started-guide/local-development-environment/index).

## Configuring Nodeos for Development Environment

The following list provides instructions to prepare your local development environment:
1. Check [system requirements](https://developers.eos.io/welcome/v2.0/getting-started-guide/local-development-environment/system_requirements).
2. Install [EOSIO Binaries](https://developers.eos.io/manuals/eos/latest/install/index).
3. Install the [CDT](https://developers.eos.io/welcome/latest/getting-started-guide/local-development-environment/index).
4. Create a [Development Wallet](https://developers.eos.io/welcome/latest/getting-started-guide/local-development-environment/index) to store keys.
5. Start [Keosd and Nodeos](https://developers.eos.io/welcome/latest/getting-started-guide/local-development-environment/index)
6. Create a [Telos Development Account](https://help.telos.net/en_US/getting-started/how-to-create-a-free-telos-account)

> Nodeos is distributed as part of the EOSIO software suite. You can download [Nodeos](https://developers.eos.io/manuals/eos/latest/install/index) here. We recommend installing the EOSIO Prebuilt Binares is you are new to EOSIO-based blockchain networks like Telos.

There are several ways to configure a `nodeos` environment for development and testing. Which option to use largely depends on what the project goals are. 
1. Local Single-Node Testnet
2. Local Single-Node Testnet with Consensus Protocol
3. Local Multi-Node Testnet
4. Official Testnet

> Go to [Development Environment](https://developers.eos.io/manuals/eos/latest/nodeos/usage/development-environment/index) for an in-depth discussion on configuring your `nodeos` setup for development and testing.

## Configuring Nodeos for Producing and Non-producing environments
Follow the [link](https://developers.eos.io/manuals/eos/latest/nodeos/usage/node-setups/index) for an in-depth discussion on how to configure `nodeos` (with the applicable plugins) to operate as a block producing node or non-producing node.



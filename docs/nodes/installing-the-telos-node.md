---
id: Installing client software
---
# Installing `nodeos` 🚀 - Telos Nodes!
This section have been adopted from [EOSIO developer documentation].(https://developers.eos.io/manuals/eos/latest/index).

Teelos blockchain network is build on the EOSIO platform. The EOSIO platform provides the components required to operate a Telos node, to collect blockchain data, to interact with nodes, and to build smart contracts.

The main components required to run the Telos blockchain network (or any EOSIO-based blockchain) is:
1. `nodeos` (node + EOSIO) that is configured to run a node (as a block producer, as dedicated API endpoints and local development)
2. `cleos` (CLI + EOSIO) is a command line interface used to interact with `nodeos`, allowing you the send commands and actions to a blockchain.
3. `keos` (key + EOSIO) is a local component that stores and manages EOSIO keys in wallets and provides a secrure enclave for digital signing.

To build smart contracts you need `EOSIO.CDT`. `EOSIO.CDT` generates `WebAssembly` binary instructions or `bytecode` into `wasm` files. The generated `wasm` files are the smart contracts which can be deployed to Telos blockchains.

EOSIO provides a frontend library for Javascript development called `EOSJS`. `EOSJS` API SDK integrates with EOSIO-based blockchains using the EOSIO RPC API. EOSIO also provides Swift and Java SDKs for native mobile application development.

To get started, you need to [prepare your development environment](https://developers.eos.io/welcome/latest/getting-started-guide/local-development-environment/index).

## Development Environment

The following list provides instructions to prepare your local development environment:
1. Check [system requirements](https://developers.eos.io/welcome/v2.0/getting-started-guide/local-development-environment/system_requirements).
2. Install [EOSIO Binaries](https://developers.eos.io/manuals/eos/latest/install/index).
3. Install the [CDT](https://developers.eos.io/welcome/latest/getting-started-guide/local-development-environment/index).
4. Create a [Development Wallet](https://developers.eos.io/welcome/latest/getting-started-guide/local-development-environment/index) to store keys.
5. Start [Keosd and Nodeos](https://developers.eos.io/welcome/latest/getting-started-guide/local-development-environment/index)
6. Create a [Telos Development Account](https://help.telos.net/en_US/getting-started/how-to-create-a-free-telos-account)

> Nodeos is distributed as part of the EOSIO software suite. You can download [Nodeos](https://developers.eos.io/manuals/eos/latest/install/index) here. We recommend installing the EOSIO Prebuilt Binares is you are new to EOSIO-based blockchain networks like Telos.

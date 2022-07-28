---
id: 'Types of Nodes'
---

# Telos Nodes
## Getting Started with Telos Nodes
### This section discusses Telos Nodes and the role they play in the Telos blockchain network.

Telos Blockchain Network is an EOSIO-based blockchain network. Therefore, everything that is required to run EOSIO-based blockchain nodes, applies to Telos. Telos makes use of EOSIO platform specific components and libraries (`nodeos`, `cleos`, `keosd`, `EOSIO.CDT`, and `EOSJS`) to operate blockchain nodes, collect blockchain data, interact with nodes, and to build smart contracts.

The main component of the Telos blockchain network is nodeos (node + EOSIO). nodeos is the core node daemon that runs on every Telos node in the network. Nodeos can be configured to process smart contracts, validate transactions, produce blocks containing valid transactions, and confirm blocks to record them on the blockchain.

`nodeos` is distributed as part of the EOSIO software suite. Each node can be configured (with specific functional plugins) to function as a:
1. Block Producing node; or as 
2. Non-producing node.

The behaviour of nodeos is determined mainly by which plugins are loaded and which plugin options are used. Some plugins are mandatory (`chain_plugin`, `net_plugin`, and `producer_plugin`) while others are optional. For a full list of plugins, please visit [Nodeos Plugins](https://developers.eos.io/manuals/eos/latest/nodeos/plugins/index) for more details.

`cleos` (CLI + EOS) is a command line interface with REST APIs exposed by `nodeos`. `cleos` is required to interact with the blockchain (via `nodeos`) and manages wallets (via `keosd`). Developers can also use cleos to deploy and test Telos smart contracts.

`keosd` (Key + EOS)  is a key manager service daemon for storing private keys and signing digital messages. It provides a secure key storage medium for keys to be encrypted at rest in the associated wallet file. `keosd` also defines a secure enclave for signing transaction created by cleos or a third part library.

All these components and libraries play a very important role in the Telos network.
In the following section, we will explore the difference between producing and non-producing nodes and how to configure each node.

## Producing nodes
Producing nodes are configured for block production. They connect to the Telos peer-to-peer network and actively produce new blocks. Producing nodes produce blocks on the mainnet, if they are an assigned block producer as part of the active block producing schedule.
Each producer node (active/producing/top-21 only) validates all blocks and transactions it receives. The nodes of elected (active/producing/top-21 only) producers take turns in bundling new transactions into blocks and broadcasting them to the network.

> Please follow the [link](https://developers.eos.io/manuals/eos/latest/nodeos/usage/node-setups/producing-node) to the general steps provided to set up a producing node.

## Non-producing nodes
Non-producing nodes also connect to the Telos peer-to-peer network, but they are not actively producing blocks. Instead, they are connected and synchronised with other peers from the Telos network.  Non-producing nodes are useful to act as:
- proxy nodes, 
- relaying API calls (API endpoints), 
- validating transactions, 
- monitoring the blockchain state history, and 
- broadcasting information to other nodes.

`nodeos` enables you to set up a device for local development as a single node blockchain network.
Non-producing nodes exposes one or more services publicly or privately by enabling one or more `nodeos` plugins, except the `producer_plugin`.

> Please follow the [link](https://developers.eos.io/manuals/eos/latest/nodeos/usage/node-setups/non-producing-node) to the general steps provided to set up a non-producing node.

For configuring Producing and Non-producing nodes, navigate to Setting up a [Node](https://developers.eos.io/manuals/eos/latest/nodeos/usage/node-setups/index).

# Telos Blockchain Network
In the Telos blockchain network, you might find the slightly different naming of nodes, such as an API node, Producer node, State History node, and Seed node. 

All nodes keep updating an internal database by applying the transactions as they arrive in incoming blocks. The difference between the node types lies in the amount of history they keep track of and in the functionality they provide.

After proper installation of released EOSIO core software, each type of node is implemented by the same executable, however, each node would need to set up different configurations to start the node. Although a block producing node can have full state history or run as an API endpoint, that would be a waste of resources. Block producing nodes should run with minimal plugins. 
Also, producing nodes should not have open network ports. We strongly recommend all node service providers to run and maintain their own nodes for reliability and security reasons.

## An API-node
API nodes provide network services to client applications. They usually have account transaction histories accessible though API calls, but can vary in the amount of available history.

## A History API-node (State History node)
State History (or History API) nodes are API nodes with a complete transaction history of all accounts that are used for querying transaction and account data from. There are various types of history, Hyperion being the most common on Telos.



## A Seed-node
A seed node is a special node that allows the incorporation of new nodes to the network and maintains the strength of the network at all times, by allowing them to synchronize and obtain a copy of the data from the blockchain, replicating it and adding resistance and security to it.

Seed nodes are nodes that accept incoming P2P connections. They are the first nodes contacted by a freshly started node. In that sense they serve as an entry point into the network. Once a node has entered the network it will receive additional node addresses from its peers, so all nodes can connect to each other. A seed node can also be an API node. The seed nodes are used only to locate or find complete nodes that are running the Telos Blockchain client.

So, when a new node wants to gain access to the network, it must connect with a seed node, which is a Telos client that is always active and has a static IP address. This client operates as a gateway to the Telos network, being one of the first connections that Telos clients make at the beginning.

Thus, seed nodes play an important role within the network, operating from highly trusted servers. Allowing new clients to connect to the Telos network automatically and without the need for manual intervention by a user. Although it may be the case that some of these nodes can become dishonest, causing a negative impact within the network. So it is not recommended to place trust in a single seed node.

A seed node can also be an API node, and the P2P list for mainnet and testnet can be found at the [node-template repo](https://github.com/telosnetwork/node-template), the genesis.json is also available there.

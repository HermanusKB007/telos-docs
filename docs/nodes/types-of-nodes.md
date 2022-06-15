---
id: 'Types of Nodes'
---

# Telos Block Producer Nodes
### Getting Started with Telos Nodes
This section describes everything you need to know about Telos Nodes, and all the requirements needed to become a Telos Block Producer.

Telos nodes, running `nodeos` generally runs in one of two modes:
1. Producing nodes
2. Non-producing nodes

Prducing nodes are configured for block production. They connect to the Telos perr-to-peer network and activly produce new blocks. Producing nodes produce blocks if they are an assigned producers as part of the active schedule.

Non-producing nodes connect also to the Telos peer-to-peer network, but they do not actively produce blocks. Non-producing nodes are useful to act a proxy nodes, relaying API calls, validating transactions, and broadcasting information to other nodes.

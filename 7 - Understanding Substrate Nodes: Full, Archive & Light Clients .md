**Understanding Substrate Nodes: Full, Archive & Light Clients #7 | Polkadot: Substrate & Rust**

📺 [Watch the full video](https://youtu.be/1r4HpVsXe7U)

# [00:00](https://youtu.be/1r4HpVsXe7U?t=0)  Understanding Substrate Node Types and Runtime
## Overview of Substrate Node Types
- [00:00](https://youtu.be/1r4HpVsXe7U?t=0)  The chapter introduces three types of substrate nodes: full nodes, archive nodes, and light client nodes.
- [00:36](https://youtu.be/1r4HpVsXe7U?t=36)  Full nodes are essential for blockchain operations, storing data, validating transactions, and authoring blocks. They typically retain only the most recent 256 blocks to manage disk space.
- [00:58](https://youtu.be/1r4HpVsXe7U?t=58)  Archive nodes store all historical blocks with complete state information, useful for applications needing access to past data like block explorers and wallets.
- [01:18](https://youtu.be/1r4HpVsXe7U?t=78)  Light client nodes connect to the network with minimal hardware requirements and can be integrated into various applications such as web apps or IoT devices.
## Understanding Runtime in Substrate
- [01:41](https://youtu.be/1r4HpVsXe7U?t=101)  The runtime is a critical component that contains business logic for executing transactions and managing state changes on the blockchain.
- [02:02](https://youtu.be/1r4HpVsXe7U?t=122)  Two main components of runtime are frame pallets (modularized entities for development) and custom pallets (allowing developers to define specific behaviors).
- [02:25](https://youtu.be/1r4HpVsXe7U?t=145)  Frame provides numerous pre-built modules for functionalities like staking and governance; developers can also create custom pallets tailored to their needs.
## Transaction Types in Substrate
- [02:46](https://youtu.be/1r4HpVsXe7U?t=166)  Transactions are mechanisms for changing state within a block. There are three transaction types: signed, unsigned, and inherent transactions.
- [03:08](https://youtu.be/1r4HpVsXe7U?t=188)  Signed transactions require an account's signature using its private key; they incur transaction fees based on runtime logic.
- [03:31](https://youtu.be/1r4HpVsXe7U?t=211)  Unsigned transactions do not need signatures but require custom validation, consuming more resources than signed ones.
- [03:53](https://youtu.be/1r4HpVsXe7U?t=233)  Inherent transactions allow block authoring nodes to add information directly without being communicated or stored elsewhere.
## Consensus Mechanisms in Blockchain
- [04:14](https://youtu.be/1r4HpVsXe7U?t=254)  Before reaching consensus, certain nodes must produce new blocks; this process is known as block authoring.
- [04:35](https://youtu.be/1r4HpVsXe7U?t=275)  Block finalization ensures only one canonical chain exists despite potential forks when two blocks reference the same parent block.
## Finality Mechanisms Explained
- [04:57](https://youtu.be/1r4HpVsXe7U?t=297)  Fork choice rules determine which chain should be extended; examples include the longest chain rule used in protocols like GRANDPA.
- [05:19](https://youtu.be/1r4HpVsXe7U?t=319)  Probabilistic finality occurs through block authoring where chances of reverting a transaction decrease as more blocks build upon it.
- [05:41](https://youtu.be/1r4HpVsXe7U?t=341)  For deterministic finality, additional mechanisms can be implemented where authority members vote on block validity once a threshold is reached.
# [06:03](https://youtu.be/1r4HpVsXe7U?t=363)  Understanding Substrate's Consensus Mechanisms
## Overview of Block Finalization and Consensus
- [06:03](https://youtu.be/1r4HpVsXe7U?t=363)  Two-thirds of blocks that have been finalized cannot be reverted without external coordination, such as a hard fork. This highlights the importance of consensus in blockchain technology.
- [06:03](https://youtu.be/1r4HpVsXe7U?t=363)  A significant advantage of Substrate is the ability to set your own consensus mechanism for your chain. By default, Substrate chains utilize Aura for block authoring and Grandpa for block finalization.
## Details on Aura and Babe
- [06:26](https://youtu.be/1r4HpVsXe7U?t=386)  Aura stands for Authority-based Round Robin scheduling, providing a slot-based block authoring mechanism where a set of authorities take turns creating blocks.
- [06:26](https://youtu.be/1r4HpVsXe7U?t=386)  Babe (Blind Assignment of Blockchain Extension) is another slot-based block authoring mechanism used primarily in proof-of-stake blockchains, relying on a known set of validators.
## Comparison with Proof of Work
- [06:49](https://youtu.be/1r4HpVsXe7U?t=409)  Unlike slot-based mechanisms, Proof of Work does not require a known authority set; anyone can produce a block at any time by solving computationally challenging problems.
## Role of Grandpa in Block Finalization
- [06:49](https://youtu.be/1r4HpVsXe7U?t=409)  Grandpa provides block finalization with a known weighted authority set similar to Babe but does not author blocks; it listens to gossip about the state of the blockchain.

---

**How to Simulate a Substrate Node Network Locally #11 | Polkadot: Substrate & Rust**


# Summary: Simulating a Multi-Node Network in Substrate

This tutorial demonstrates how to launch two independent blockchain nodes (Alice and Bob) on a local system to simulate a decentralized network where nodes discover and sync with each other.

### 1. Introduction to Network Decentralization

* **[[00:01](http://www.youtube.com/watch?v=krmVQRxrY9k&t=1)]**: Concept of nodes in a blockchain. Each node holds a full copy of the ledger, and increasing the number of nodes enhances the network's decentralization.
* **[[00:26](http://www.youtube.com/watch?v=krmVQRxrY9k&t=26)]**: Goal of the video: showing how multiple nodes stay in sync and reach consensus on a local machine.

### 2. Setting Up the First Node (Alice)

* **[[00:44](http://www.youtube.com/watch?v=krmVQRxrY9k&t=44)]**: Cleaning the database for the first node using the `purge-chain` command for the **Alice** account to ensure a fresh start.
* **[[01:03](http://www.youtube.com/watch?v=krmVQRxrY9k&t=63)]**: Launching Alice's node. The command specifies the node key, the telemetry URL, and the ports used for communication.

### 3. Setting Up the Second Node (Bob)

* **[[01:35](http://www.youtube.com/watch?v=krmVQRxrY9k&t=95)]**: Navigating to the same project folder in a second terminal to start another instance.
* **[[01:52](http://www.youtube.com/watch?v=krmVQRxrY9k&t=112)]**: Purging the chain database for the **Bob** account.
* **[[02:03](http://www.youtube.com/watch?v=krmVQRxrY9k&t=123)]**: Launching Bob's node using the `--bootnodes` flag. This flag points to Alice's network address, allowing the two nodes to find each other.

### 4. Verification of Discovery and Sync

* **[[02:18](http://www.youtube.com/watch?v=krmVQRxrY9k&t=138)]**: Identifying the **"Discovered"** message in the logs, which confirms the nodes have successfully found each other.
* **[[02:28](http://www.youtube.com/watch?v=krmVQRxrY9k&t=148)]**: Checking the peer count. The logs show **"1 peer"**, indicating a successful connection between the two local nodes.
* **[[02:44](http://www.youtube.com/watch?v=krmVQRxrY9k&t=164)]**: Observating the **"Imported"** block messages. This proves the nodes are in sync, sharing the same blocks and following the consensus mechanism.

### 5. Conclusion & Next Steps

* **[[03:02](http://www.youtube.com/watch?v=krmVQRxrY9k&t=182)]**: Scaling the simulation. Although done on one computer, this exact process applies to a global network of thousands of nodes.
* **[[03:36](http://www.youtube.com/watch?v=krmVQRxrY9k&t=216)]**: Limitations of the current setup. This was a permissionless network. The speaker introduces the next topic: securing the network using dedicated keys and a keystore.


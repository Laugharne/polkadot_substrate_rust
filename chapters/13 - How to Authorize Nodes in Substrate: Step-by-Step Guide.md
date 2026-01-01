**How to Authorize Nodes in Substrate: Step-by-Step Guide #13 | Polkadot: Substrate & Rust**


# Summary: Node Authorization in Substrate Networks

This tutorial covers the technical steps required to implement the `node-authorization` pallet, allowing for a restricted network where only specific identities can participate and connect as sub-nodes.

### 1. Project Configuration & Dependencies

* **[[01:21](http://www.youtube.com/watch?v=A6SUPZx921c&t=81)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D81s)**: Adding the `palette-node-authorization` dependency to the `runtime/Cargo.toml` file. It's crucial to ensure the Polkadot branch matches other dependencies to avoid build errors.
* **[[03:06](http://www.youtube.com/watch?v=A6SUPZx921c&t=186)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D186s)**: Updating `runtime/src/lib.rs` to include administrative rules and setting parameter types like `MaxWellKnownNodes` and `MaxPeerIdLength`.
* **[[05:14](http://www.youtube.com/watch?v=A6SUPZx921c&t=314)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D314s)**: Integrating the pallet into the `construct_runtime!` macro so the blockchain recognizes the new authorization logic.

### 2. Updating Chain Specification

* **[[06:47](http://www.youtube.com/watch?v=A6SUPZx921c&t=407)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D407s)**: Modifying `node/src/chain_spec.rs` to include the `NodeAuthorizationConfig`. This hardcodes the initial set of authorized nodes (Alice and Bob) into the Genesis state.
* **[[08:05](http://www.youtube.com/watch?v=A6SUPZx921c&t=485)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D485s)**: Compiling the project using `cargo build --release` to apply all runtime changes.

### 3. Simulating the Network Nodes

* **[[09:03](http://www.youtube.com/watch?v=A6SUPZx921c&t=543)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D543s)**: Starting the first two nodes (**Alice** and **Bob**). Since they are pre-authorized, they discover each other and begin syncing immediately.
* **[[11:03](http://www.youtube.com/watch?v=A6SUPZx921c&t=663)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D663s)**: Starting a third node (**Charlie**). Initially, Charlie has **0 peers** because he hasn't been authorized via the runtime yet.

### 4. Authorization via Polkadot.js Portal

* **[[11:42](http://www.youtube.com/watch?v=A6SUPZx921c&t=702)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D702s)**: Connecting to the local node using the Polkadot.js Apps explorer.
* **[[12:13](http://www.youtube.com/watch?v=A6SUPZx921c&t=733)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D733s)**: Using the **Sudo** module to call `add_well_known_node`. By providing Charlie’s Peer ID, the network is updated in real-time to allow him to join.
* **[[13:49](http://www.youtube.com/watch?v=A6SUPZx921c&t=829)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D829s)**: Verifying the transaction in the Explorer; Charlie now successfully connects to Alice and Bob.

### 5. Managing Sub-nodes (Dave)

* **[[14:20](http://www.youtube.com/watch?v=A6SUPZx921c&t=860)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D860s)**: Adding a fourth node (**Dave**) as a "sub-node" of Charlie. This demonstrates a hierarchical permission system.
* **[[16:12](http://www.youtube.com/watch?v=A6SUPZx921c&t=972)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D972s)**: Claiming the node identifier for Dave and authorizing the specific connection between Charlie and Dave through the front-end extrinsics.

### 6. Conclusion

* **[[18:41](http://www.youtube.com/watch?v=A6SUPZx921c&t=1121)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DA6SUPZx921c%26t%3D1121s)**: Final overview of the architecture: a network with Alice, Bob, and Charlie as main nodes, and Dave as an authorized sub-node, all managed via a decentralized governance (Sudo) interface.




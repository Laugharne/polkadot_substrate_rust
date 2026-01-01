**Substrate Nodes: Setting Up a Secure Private Network #12 | Polkadot: Substrate & Rust**


# Detailed Summary: Substrate Permissioned Network Setup

This video explains how to configure a **private and secure blockchain** where only authorized validators can participate.

### 1. Introduction & Network Security

* **[00:00:01](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DL36x28vGM8Y%26t%3D1s)**: Concept of a "Permissioned Network". Unlike open networks, this setup requires nodes to have specific keys stored in their local keystore to be recognized by peers.
* **[00:01:04](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DL36x28vGM8Y%26t%3D64s)**: Setup demonstration using two different Linux users to simulate two independent physical machines.

### 2. Key Generation (Aura & Grandpa)

* **[00:01:54](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DL36x28vGM8Y%26t%3D114s)**: Introduction to the two essential key types:
* **Aura (sr25519)**: Responsible for block production slot allocation.
* **Grandpa (ed25519)**: Responsible for block finality (consensus).


* **[00:03:00](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DL36x28vGM8Y%26t%3D180s)**: Generating the secret phrases (mnemonic) and public keys for both "Node 1" and "Node 2".

### 3. Custom Chain Specification (Chain Spec)

* **[00:06:37](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DL36x28vGM8Y%26t%3D397s)**: Exporting the default chain spec to a JSON file to customize the network identity.
* **[00:07:12](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DL36x28vGM8Y%26t%3D432s)**: Editing the `customSpec.json`:
* Changing the network name.
* Manually inserting the generated Aura and Grandpa public keys into the "Genesis State".


* **[00:08:13](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DL36x28vGM8Y%26t%3D493s)**: Generating the **Raw Chain Spec**, which is the finalized version used by the nodes to launch.

### 4. Keystore Management

* **[00:10:20](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DL36x28vGM8Y%26t%3D620s)**: Clearing previous blockchain data (`purge-chain`) to prevent state mismatch.
* **[00:11:03](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DL36x28vGM8Y%26t%3D663s)**: Inserting the keys into each node's local keystore using the `key insert` command. This links the software's ability to sign blocks with the authorized identities defined in the Chain Spec.

### 5. Network Launch & Validation

* **[00:15:53](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DL36x28vGM8Y%26t%3D953s)**: Starting the first node. It stays "Idle" because it requires a peer to reach consensus.
* **[00:16:53](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DL36x28vGM8Y%26t%3D1013s)**: Starting the second node using the first node's P2P address as a `bootnode`.
* **[00:17:28](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DL36x28vGM8Y%26t%3D1048s)**: Final validation: The logs show "Discovered" and "Imported", proving that the two authorized nodes are successfully communicating and building the chain.


**Forkless Runtime Upgrades with Substrate: A Step-by-Step Guide**


# Summary: Forkless Runtime Upgrades in Substrate

This tutorial explains one of the most powerful features of Substrate: the ability to upgrade a blockchain's logic (runtime) while the network is still running, without requiring a hard fork.

### 1. Introduction to Forkless Upgrades

* **[[00:01](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=1)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D1s)**: Introduction to the concept. Substrate allows for real-time upgrades to the runtime code while the node is active.
* **[[01:41](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=101)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D101s)**: Connecting to the **Polkadot.js Explorer**. The speaker points out that the current version is `node-template/100`. The goal is to update this to version `101`.

### 2. Modifying the Runtime Code

* **[[02:46](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=166)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D166s)**: Adding the `pallet-utility` dependency to the `runtime/Cargo.toml` file.
* **[[04:25](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=265)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D265s)**: Updating `runtime/src/lib.rs` to implement the utility pallet and configuring the runtime to use it.
* **[[05:42](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=342)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D342s)**: **Crucial Step**: Changing the `spec_version` from `100` to `101`. This version increment tells the network that a new logic version is available.

### 3. Compiling the New Runtime

* **[[06:14](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=374)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D374s)**: Building the project with `cargo build --release`.
* **[[07:30](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=450)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D450s)**: Locating the generated WebAssembly (Wasm) file. The specific file needed is `target/release/wbuild/node-template-runtime/node_template_runtime.compact.compressed.wasm`.

### 4. Executing the Upgrade via UI

* **[[08:45](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=525)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D525s)**: Navigating to the **Extrinsics** tab in Polkadot.js.
* **[[09:02](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=542)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D542s)**: Using the **Sudo** module to call `system.setCode`. This function allows the administrator to upload the new Wasm binary directly to the chain.
* **[[09:42](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=582)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D582s)**: Submitting and signing the transaction to push the new code to the running blockchain.

### 5. Verification & Results

* **[[10:12](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=612)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D612s)**: Checking the **Events** tab to confirm the success of the Sudo transaction.
* **[[10:31](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=631)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D631s)**: Final confirmation: The Explorer now displays version `101`, and the blocks continue to produce without any network interruption.

### 6. Conclusion

* **[[11:11](http://www.youtube.com/watch?v=k9TgTuRRTZ0&t=671)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3Dk9TgTuRRTZ0%26t%3D671s)**: Comparison with other blockchains (like Ethereum) where major upgrades often require complex "merges" or forks. Substrate eliminates this pain by allowing "on-the-fly" upgrades.


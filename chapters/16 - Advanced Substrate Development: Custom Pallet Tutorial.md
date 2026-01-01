**Advanced Substrate Development: Custom Pallet Tutorial #16 | Polkadot: Substrate & Rust**


# Summary: Building a Custom Frame Pallet in Substrate

This tutorial guides you through the process of creating and integrating a **custom Frame pallet** into a Substrate node. This allows developers to customize the blockchain's behavior beyond the default modules.

### 1. Preparing the Development Environment

* **[[00:24](http://www.youtube.com/watch?v=88AaOP769Ek&t=24)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3D88AaOP769Ek%26t%3D24s)**: Navigating to the `pallets/template` folder and cleaning up the project. The speaker instructs to delete `benchmarking.rs`, `mock.rs`, and `tests.rs`, leaving only `lib.rs`.
* **[[01:02](http://www.youtube.com/watch?v=88AaOP769Ek&t=62)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3D88AaOP769Ek%26t%3D62s)**: Clearing the content of `lib.rs` to start from scratch.
* **[[01:13](http://www.youtube.com/watch?v=88AaOP769Ek&t=73)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3D88AaOP769Ek%26t%3D73s)**: Adding the necessary macro for building both the **Rust native binary** (standard) and **WebAssembly** (no-standard).

### 2. Implementing the Pallet Skeleton

* **[[01:33](http://www.youtube.com/watch?v=88AaOP769Ek&t=93)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3D88AaOP769Ek%26t%3D93s)**: Introducing the five core components of a Substrate pallet:
1. **Config**: Defines the pallet's dependencies on the runtime.
2. **Events**: For reporting changes to the outside world.
3. **Errors**: For handling invalid transactions.
4. **Storage**: For persisting data on the blockchain.
5. **Extrinsics (Callable Functions)**: Logic that users can execute.


* **[[02:26](http://www.youtube.com/watch?v=88AaOP769Ek&t=146)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3D88AaOP769Ek%26t%3D146s)**: Step-by-step implementation of each part, including creating events like `ClaimCreated` and `ClaimRevoked`.

### 3. Critical Fix & Compilation

* **[[03:18](http://www.youtube.com/watch?v=88AaOP769Ek&t=198)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3D88AaOP769Ek%26t%3D198s)**: **Crucial Tip**: Commenting out line 273 in the `lib.rs` file (related to weights) to avoid compilation errors that aren't documented elsewhere.
* **[[04:35](http://www.youtube.com/watch?v=88AaOP769Ek&t=275)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3D88AaOP769Ek%26t%3D275s)**: Running `cargo check` and `cargo build --release`. The speaker notes that minor warnings are acceptable as long as the build finishes successfully.

### 4. Testing with Polkadot.js UI

* **[[05:01](http://www.youtube.com/watch?v=88AaOP769Ek&t=301)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3D88AaOP769Ek%26t%3D301s)**: Starting the node in development mode (`--dev`) and ensuring it produces blocks.
* **[[05:41](http://www.youtube.com/watch?v=88AaOP769Ek&t=341)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3D88AaOP769Ek%26t%3D341s)**: Accessing the **Extrinsics** tab in Polkadot.js. The user selects the `templateModule` and calls the `createClaim` function with a file hash.
* **[[06:16](http://www.youtube.com/watch?v=88AaOP769Ek&t=376)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3D88AaOP769Ek%26t%3D376s)**: Confirming the transaction success via the green tick notification.

### 5. Verifying Data on the Chain

* **[[06:34](http://www.youtube.com/watch?v=88AaOP769Ek&t=394)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3D88AaOP769Ek%26t%3D394s)**: Reading the blockchain state. By querying the `templateModule.claims`, the user can verify that the claim (owner address and block number) has been correctly stored.

### 6. Conclusion

* **[[07:15](http://www.youtube.com/watch?v=88AaOP769Ek&t=435)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3D88AaOP769Ek%26t%3D435s)**: Final thoughts on the flexibility of Substrate and a teaser for the next chapter on **Smart Contracts**.


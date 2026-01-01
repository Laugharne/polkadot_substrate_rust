**Create Blockchain Apps with Substrate Smart Contracts #17 | Polkadot: Substrate & Rust**


# Summary: Developing Smart Contracts on Substrate

This tutorial covers the complete lifecycle of a smart contract on Substrate: from setting up the development environment to creating, building, deploying, and interacting with a contract.

### 1. Environment Setup & Tooling

* **[[00:48](http://www.youtube.com/watch?v=nLrlOBcTqEw&t=48)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DnLrlOBcTqEw%26t%3D48s)**: Installation of essential tools:
* **Rustup**: The Rust toolchain installer.
* **Cargo Contract CLI**: A specialized tool for managing Substrate smart contracts.


* **[[02:01](http://www.youtube.com/watch?v=nLrlOBcTqEw&t=121)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DnLrlOBcTqEw%26t%3D121s)**: Installation of the **Substrate Contracts Node**, a specialized node equipped with the `pallet-contracts` module necessary for running Wasm smart contracts.

### 2. Creating & Testing a Contract Project

* **[[03:32](http://www.youtube.com/watch?v=nLrlOBcTqEw&t=212)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DnLrlOBcTqEw%26t%3D212s)**: Creating a new project using the **Flipper** template. This basic contract allows for flipping a boolean value (true/false) and retrieving the current state.
* **[[04:30](http://www.youtube.com/watch?v=nLrlOBcTqEw&t=270)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DnLrlOBcTqEw%26t%3D270s)**: Running unit tests with `cargo test` to ensure the logic is correct before deployment.
* **[[04:49](http://www.youtube.com/watch?v=nLrlOBcTqEw&t=289)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DnLrlOBcTqEw%26t%3D289s)**: Building the contract to generate the `.contract` artifact (the Wasm binary and metadata needed for deployment).

### 3. Running the Local Node

* **[[05:09](http://www.youtube.com/watch?v=nLrlOBcTqEw&t=309)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DnLrlOBcTqEw%26t%3D309s)**: Launching the `substrate-contracts-node`. This local blockchain acts as the environment where the smart contract will live and execute.

### 4. Deployment (Instantiation)

* **[[05:37](http://www.youtube.com/watch?v=nLrlOBcTqEw&t=337)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DnLrlOBcTqEw%26t%3D337s)**: Instantiating the smart contract on the running node. The speaker explains the command-line process and how to retrieve the unique **contract address** generated upon success.

### 5. Interacting with the Smart Contract

* **[[06:32](http://www.youtube.com/watch?v=nLrlOBcTqEw&t=392)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DnLrlOBcTqEw%26t%3D392s)**: Calling the **Get** function to read the current state of the Flipper contract.
* **[[08:00](http://www.youtube.com/watch?v=nLrlOBcTqEw&t=480)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DnLrlOBcTqEw%26t%3D480s)**: Executing the **Flip** function, which modifies the state on the blockchain. The speaker demonstrates how to troubleshoot environment variable issues by using the direct contract address.

### 6. Conclusion

* **[[08:54](http://www.youtube.com/watch?v=nLrlOBcTqEw&t=534)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DnLrlOBcTqEw%26t%3D534s)**: Recap of the fundamental stages (Build, Deploy, Interact) which apply to any smart contract project on Substrate, regardless of its complexity.


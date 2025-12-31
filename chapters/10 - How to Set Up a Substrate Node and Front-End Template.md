**How to Set Up a Substrate Node and Front-End Template #10 | Polkadot: Substrate & Rust**

📺 [Watch the full video](https://youtu.be/lRNsMsWyDNs)

- [08:25](https://youtu.be/lRNsMsWyDNs?t=505)  The platform allows for interaction with a local blockchain node, providing a powerful feature set for developers and users alike.
# [00:00](https://youtu.be/lRNsMsWyDNs?t=0)  Starting a Substrate Node on Your Local Machine
## Overview of the Process
- [00:00](https://youtu.be/lRNsMsWyDNs?t=0)  The tutorial begins with the installation of Rust and outlines the steps to start a substrate node on a local machine, including compiling and running both backend and frontend templates.
- [00:36](https://youtu.be/lRNsMsWyDNs?t=36)  Users are instructed to clone the substrate node template from GitHub, navigate into the directory, and prepare for compilation.
## Compiling the Node Template
- [00:58](https://youtu.be/lRNsMsWyDNs?t=58)  After switching to a new branch named with the current date, users run `cargo build --release` to compile the cloned node template.
- [01:34](https://youtu.be/lRNsMsWyDNs?t=94)  An error related to version 32 is mentioned as common; it can be resolved by following specific instructions that may not be clear in documentation.
## Resolving Compilation Errors
- [01:55](https://youtu.be/lRNsMsWyDNs?t=115)  The speaker emphasizes that many users encounter this error but provides reassurance that solutions exist within community forums like Stack Overflow.
- [02:17](https://youtu.be/lRNsMsWyDNs?t=137)  To resolve errors, users should execute `rustup target add <target>` as indicated in error messages. This step is crucial for successful compilation.
## Starting the Local Node
- [02:40](https://youtu.be/lRNsMsWyDNs?t=160)  Once compiled successfully, users can start their local node. Observing logs indicating block formation confirms that everything is functioning correctly.
- [03:26](https://youtu.be/lRNsMsWyDNs?t=206)  The next step involves setting up a frontend template after ensuring that the backend (node) is operational.
# [03:50](https://youtu.be/lRNsMsWyDNs?t=230)  Setting Up Frontend Template
## Prerequisites for Frontend Setup
- [03:50](https://youtu.be/lRNsMsWyDNs?t=230)  Before cloning the frontend template, users must have Node.js and Yarn installed. Familiarity with JavaScript frameworks like React.js is beneficial.
- [01:02:19](https://youtu.be/lRNsMsWyDNs?t=3739)  The speaker shares their current versions of Node (16.14) and Yarn , noting compatibility issues with different versions.
## Cloning and Installing Frontend Template
- [04:45](https://youtu.be/lRNsMsWyDNs?t=285)  Users are guided to clone the substrate frontend template repository and navigate into its directory before running `yarn install` to set up dependencies.
## Running Frontend Application
- [05:22](https://youtu.be/lRNsMsWyDNs?t=322)  After installation, starting the application using `yarn start` launches it in a browser at localhost:8000, displaying user balances and transaction options.
# [06:21](https://youtu.be/lRNsMsWyDNs?t=381)  Interacting with Blockchain through Frontend
## User Interface Features
- [06:21](https://youtu.be/lRNsMsWyDNs?t=381)  The frontend displays user information such as balances for various accounts (e.g., Alice), allowing interaction through fund transfers.
## Executing Transactions
- [06:43](https://youtu.be/lRNsMsWyDNs?t=403)  Users can initiate transactions by selecting recipient addresses (like Charlie or Dave), specifying amounts while adhering to minimum transfer requirements.
# [07:42](https://youtu.be/lRNsMsWyDNs?t=462)  Transaction Verification and Blockchain Interaction
## Understanding Transaction Confirmation
- [07:42](https://youtu.be/lRNsMsWyDNs?t=462)  The transaction directed to Dave is confirmed, and users can verify this through their terminal, indicating that the process is functioning correctly.
- [08:03](https://youtu.be/lRNsMsWyDNs?t=483)  Users are encouraged to take note of various data points available in the UI, including the address of the substrate node and current block information.
- [08:25](https://youtu.be/lRNsMsWyDNs?t=505)  The interface provides access to balances across different wallets within the blockchain, showcasing a comprehensive view of user assets.
## Features of Substrate Node
- [08:25](https://youtu.be/lRNsMsWyDNs?t=505)  Users have the capability to transfer funds between different addresses directly from their browser, enhancing accessibility and usability.
- [08:25](https://youtu.be/lRNsMsWyDNs?t=505)  The platform allows for interaction with a local blockchain node, providing a powerful feature set for developers and users alike.

---


**From State Transitions to XCM: Inside Substrate #8 | Polkadot: Substrate & Rust**

📺 [Watch the full video](https://youtu.be/AUW88S-amvQ)

# [00:00](https://youtu.be/AUW88S-amvQ?t=0)  Understanding State Transitions and Storage in Substrate
## Overview of Transactions and Storage
- [00:00](https://youtu.be/AUW88S-amvQ?t=0)  The chapter builds on previous knowledge about transactions and consensus mechanisms in Substrate, focusing on state transitions, storage concepts, accounts, addresses, keys, off-chain operations, and cross-consensus communication.
## Key Value Databases in Substrate
- [00:22](https://youtu.be/AUW88S-amvQ?t=22)  Substrate utilizes RocksDB as its persistent key-value store for fast storage environments; it also supports an experimental Parity DB.
- [00:43](https://youtu.be/AUW88S-amvQ?t=43)  The key-value storage allows for easy abstraction of storage structures. A modified Merkle trie structure is used to efficiently manage historical block states.
## Trie Abstraction
- [01:05](https://youtu.be/AUW88S-amvQ?t=65)  Tries enable efficient data sharing and verification between blockchain nodes by comparing trie roots; different data results in different roots.
## Querying Storage
- [01:27](https://youtu.be/AUW88S-amvQ?t=87)  Blockchains built with Substrate expose a remote procedure call (RPC) server for querying runtime storage using associated keys.
# [01:48](https://youtu.be/AUW88S-amvQ?t=108)  Accounts, Addresses, and Keys Explained
## Account Representation
- [01:48](https://youtu.be/AUW88S-amvQ?t=108)  An account represents an identity capable of making transactions or holding funds; it can represent individuals or organizations.
## Key Pair Structure
- [02:11](https://youtu.be/AUW88S-amvQ?t=131)  Each account has a public/private key pair; the private key generates a mnemonic seed phrase crucial for account recovery if lost.
## Runtime Account Definition
- [02:56](https://youtu.be/AUW88S-amvQ?t=176)  In a Frame-built runtime, accounts are defined as a storage map with a 32-byte address identifier containing transaction history and balance information.
# [03:18](https://youtu.be/AUW88S-amvQ?t=198)  Specialized Accounts in Substrate
## Types of Specialized Accounts
- [03:18](https://youtu.be/AUW88S-amvQ?t=198)  Different chains can implement specialized accounts with unique rules through pre-built palettes like staking or custom pallets.
### Multi-signature Accounts
- [03:41](https://youtu.be/AUW88S-amvQ?t=221)  Multi-signature accounts require approval from multiple holders to execute transactions.
### Proxy Accounts
- [04:03](https://youtu.be/AUW88S-amvQ?t=243)  Proxy accounts allow primary owners to designate others to act on their behalf while adding security layers by isolating funds.
# [04:25](https://youtu.be/AUW88S-amvQ?t=265)  Off-chain Operations in Substrate
## Off-chain Workers
- [04:25](https://youtu.be/AUW88S-amvQ?t=265)  Off-chain workers handle tasks that exceed maximum block execution time, such as web requests or random number generation.
### Off-chain Storage
- [04:46](https://youtu.be/AUW88S-amvQ?t=286)  Off-chain storage is local to substrate nodes accessible by both off-chain workers and on-chain logic but has limited read access for on-chain state due to cost considerations.
### Optional Services
- [05:08](https://youtu.be/AUW88S-amvQ?t=308)  The optional service allows the runtime to write directly to off-chain storage independently from off-chain workers.
# [05:30](https://youtu.be/AUW88S-amvQ?t=330)  Understanding XCM Message Protocols
## Overview of XCM and Its Purpose
- [05:30](https://youtu.be/AUW88S-amvQ?t=330)  The XCM (Cross-Consensus Messaging) format provides temporary storage for on-chain logic, complementing the on-chain state. It facilitates communication across different consensus systems using a generalized set of instructions for transactions.
## Key Concepts in XCM
- [05:52](https://youtu.be/AUW88S-amvQ?t=352)  Each message in the XCM format consists of a set of instructions requested by a sender, which can be accepted or rejected by the recipient. This section will cover four main concepts: types of messages, available protocols, properties of messages, and their dependence on location and assets.
## Communication Channels in the Portal Ecosystem
- [06:15](https://youtu.be/AUW88S-amvQ?t=375)  There are three primary communication channels within the portal ecosystem:
- **Upward Message Passing**: Allows parachains to send messages to their relay chain.
- **Downward Message Passing**: Enables relay chains to communicate with parachains.
- **Consensus Message Passing**: Facilitates message exchange between connected parachains.
## Properties of XCM Messages
- [06:38](https://youtu.be/AUW88S-amvQ?t=398)  Four important properties characterize messages using the XCM format:
- **Asynchronous**: Messages do not require immediate responses.
- **Absolute Asymmetric**: Different roles exist for senders and recipients.
- **Agnostic**: The system does not depend on specific technologies or platforms.
## Location Identification in XCM
- [07:00](https://youtu.be/AUW88S-amvQ?t=420)  The XCM must express locations unambiguously for various activities such as:
- Executing instructions,
- Withdrawing assets,
- Receiving accounts.
Assets may be located within a relay chain, parachain, foreign chain, specific account, smart contract, or individual palette. Most blockchains rely on digital assets to provide economic incentives crucial for network security.

---

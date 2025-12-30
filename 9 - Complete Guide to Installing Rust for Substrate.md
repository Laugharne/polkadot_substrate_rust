**Complete Guide to Installing Rust for Substrate #9 | Polkadot: Substrate & Rust**

📺 [Watch the full video](https://youtu.be/OkSVYpODIwQ)

# [00:00](https://youtu.be/OkSVYpODIwQ?t=0)  Installing Rust for Substrate Development
## Prerequisites for Working with Substrate
- [00:00](https://youtu.be/OkSVYpODIwQ?t=0)  Before starting with Substrate, it is essential to have Rust installed on your system as Substrate is built using Rust.
- [00:22](https://youtu.be/OkSVYpODIwQ?t=22)  Installation steps vary slightly between operating systems: Linux and Windows share similar commands due to the recommendation of using WSL (Windows Subsystem for Linux), while Mac has its own set of instructions.
## Installation Steps Overview
- [00:53](https://youtu.be/OkSVYpODIwQ?t=53)  The first step involves ensuring that the "build-essential" package is available. If not already installed, it can be easily added through a command mentioned in the course document.
- [01:16](https://youtu.be/OkSVYpODIwQ?t=76)  Additional packages may need installation or upgrading; if errors occur during this process, running `apt-get update` can resolve them.
## Installing Rust
- [01:59](https://youtu.be/OkSVYpODIwQ?t=119)  To install Rust, a specific command is provided which installs the default version. After installation, users are prompted to either restart their shell or run a command to recognize Rust in the current terminal session.
- [02:23](https://youtu.be/OkSVYpODIwQ?t=143)  Verifying the installation can be done by checking the version of rustc (Rust compiler); version 1.69.0 should appear as expected.
## Managing Rust Versions and Packages
- [02:58](https://youtu.be/OkSVYpODIwQ?t=178)  Alongside rustc, `rustup` serves as a package manager for managing different versions of Rust. Users are advised to run `rustup update` after installation.
- [03:35](https://youtu.be/OkSVYpODIwQ?t=215)  It’s crucial to execute certain commands post-installation; failure to do so may lead to errors when trying to run Substrate nodes, specifically regarding missing components like "wasm32".

---

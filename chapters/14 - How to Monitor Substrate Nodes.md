**How to Monitor Substrate Nodes: A Complete Guide #14 | Polkadot: Substrate & Rust**


# Summary: Monitoring Substrate Nodes with Prometheus and Grafana

This tutorial explains how to set up a complete monitoring stack for a Substrate blockchain node. It uses **Prometheus** to collect metrics and **Grafana** to visualize them, ensuring the health and performance of the node can be tracked in real-time.

### 1. Introduction to Monitoring Tools

* **[[00:01](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=1)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D1s)**: Overview of the architecture: **Prometheus** gathers health logs and metrics from the Substrate node, while **Grafana** provides a visual dashboard for that data.
* **[[00:56](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=56)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D56s)**: Demonstrating how to check the raw metrics produced by a Substrate node using a `curl` command on the local port `9615`.

### 2. Installation Strategies (OS Specifics)

* **[[01:40](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=100)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D100s)**: Discussion on installation for different operating systems. For Mac, **Homebrew** is recommended. For Windows, using **WSL (Ubuntu)** is highly advised to match Linux server environments.
* **[[03:00](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=180)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D180s)**: Warning against using **Docker** for this specific setup if you are inexperienced, as configuring communication between separate containers for Substrate, Prometheus, and Grafana can be complex.

### 3. Setting Up Prometheus

* **[[04:38](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=278)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D278s)**: Step-by-step installation guide for Ubuntu/WSL, including creating a dedicated Prometheus user and setting up the necessary directory structures.
* **[[07:44](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=464)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D464s)**: **Crucial Configuration**: Editing the `prometheus.yml` file. A new job named `substrate_node` must be added to the `scrape_configs` section, pointing to `localhost:9615`.
* **[[10:34](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=634)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D634s)**: Launching the Prometheus server and verifying it is "Ready to receive requests" at `localhost:9090`.

### 4. Installing and Starting Grafana

* **[[12:16](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=736)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D736s)**: Installation via the official Grafana repository using `apt-get`.
* **[[13:30](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=810)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D810s)**: Handling Service Management in WSL. Since WSL often lacks `systemctl`, the speaker demonstrates using `sudo service grafana-server start` instead.
* **[[15:10](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=910)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D910s)**: Accessing the Grafana UI at `localhost:3000` (Default login: `admin/admin`).

### 5. Connecting Data Sources

* **[[15:40](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=940)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D940s)**: In the Grafana dashboard, adding **Prometheus** as a data source and linking it to the Prometheus server URL (`http://localhost:9090`).
* **[[16:06](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=966)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D966s)**: Running a "Save & Test" to confirm that Grafana can successfully pull data from the metrics collector.

### 6. Final Conclusion

* **[[16:48](http://www.youtube.com/watch?v=Fpl_1ekfow0&t=1008)](https://www.google.com/search?q=https://www.youtube.com/watch%3Fv%3DFpl_1ekfow0%26t%3D1008s)**: Recap of the full pipeline: Substrate Node (Metrics) → Prometheus (Collector) → Grafana (Visualizer). The setup is now ready for professional-grade blockchain monitoring.


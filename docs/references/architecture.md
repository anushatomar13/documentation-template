# Architecture

Caliper is made up of several key components that work together to benchmark different blockchain systems:

1. **Benchmark Engine**
This is the core part of Caliper. It acts as the conductor, coordinating all the other components and managing the execution of benchmark tests.

2. **Blockchain Adapters**
These are like connectors or bridges that allow Caliper to communicate and interact with different blockchain platforms like Hyperledger Fabric or Ethereum. Each blockchain system has its own adapter that translates commands between Caliper and that blockchain.

3. **Resource Monitors (Optional)**
These optional components collect data about the system resources (CPU, memory, network, etc.) being used during the benchmark tests. This provides insights into how resource-intensive the blockchain system is.

4. **Performance Analyzers**
These components take all the data collected during the benchmark tests (transactions, resource usage, etc.) and process it to generate easy-to-understand performance reports.

The way it works is:
1) The Benchmark Engine takes the test configuration from the user.
2) It uses the appropriate Blockchain Adapter to deploy and run transactions on the target blockchain system.
3) If enabled, the Resource Monitors collect system resource data during the tests.
4) The Performance Analyzers crunch all the collected data and metrics.
5) Finally, the Benchmark Engine gets the processed results and performance reports.

This modular architecture with separate, interchangeable components makes Caliper flexible and extensible. New blockchain adapters or custom resource monitors can be added easily without modifying the core engine.

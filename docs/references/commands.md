# Commands

Hyperledger Caliper provides several commands to manage and run benchmarks. Here are the main commands and their purposes:

1. **`npm run caliper launch`**
   This is the primary command to execute benchmark tests. It requires additional arguments to specify the test configuration:
   
   ```
   npm run caliper launch -- <options>
   ```
   
   The commonly used options are:
   - `manager=<module>`: The type of test manager to use (e.g., `manager=test-manager`).
   - `blockchain=<type>`: The type of blockchain system to test (e.g., `blockchain=fabric`).
   - `benchmark=<path>`: The path to the benchmark configuration file (e.g., `benchmark=benchmarks/samples/fabric/marbles.yaml`).
   - `caliperId=<id>`: A unique identifier for the benchmark run.

2. **`npm run caliper server`**
   This command starts the Caliper web server, which provides a user interface to monitor active and completed benchmark runs.
   
   ```
   npm run caliper server
   ```
   
   By default, the server runs on `http://localhost:8090`.

3. **`npm run caliper bind`**
   This command binds a running Caliper instance to the web server, allowing the instance to be monitored and controlled via the web interface.
   
   ```
   npm run caliper bind --caliper-bind-server <server>:<port>
   ```

4. **`npm run caliper unbind`**
   This command unbinds a Caliper instance from the web server.
   
   ```
   npm run caliper unbind --caliper-bind-server <server>:<port>
   ```

5. **`npm run caliper list`**
   This command lists the available benchmark configurations.
   
   ```
   npm run caliper list --caliper-benchconfig=<path>
   ```
   
   The `--caliper-benchconfig` option specifies the directory containing the benchmark configuration files.

6. **`npm run caliper publish`**
   This command publishes benchmark results to a remote service (e.g., a database or file server).
   
   ```
   npm run caliper publish --caliper-publish-uri=<uri>
   ```
   
   The `--caliper-publish-uri` option specifies the URI of the remote service.


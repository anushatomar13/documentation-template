# Operator's Guide


## Hyperledger Caliper Operator's Guide

This guide provides instructions for operators to deploy, configure, and manage Hyperledger Caliper in their environment.

### Prerequisites

- Node.js (v8.X or higher) and npm installed
- One or more blockchain systems to benchmark (e.g., Hyperledger Fabric, Ethereum)
- Familiarity with the blockchain system(s) you want to test

### Deployment

1. Clone the Caliper repository:

```bash
git clone https://github.com/anushatomar13/documentation-template
```

2. Install Caliper dependencies: 

```bash
cd caliper
npm install
```

### Configuration

Caliper requires configuration files for the blockchain system(s) and test case(s). Sample configurations are provided.

1. Copy the sample configuration to a new directory:

```bash
mkdir my-tests
cp -r caliper/benchmarks/* my-tests/
```

2. Modify the configuration files in `my-tests/` to match your blockchain network setup and test requirements.

### Running Tests

To execute a test, use the `caliper launch` command:

```bash
npm run caliper launch -- manager=test-manager benchmark=my-tests/my-test.yaml
```

This will run the test defined in `my-test.yaml` using the test manager.

### Monitoring

Caliper provides a web UI to monitor active and completed test runs:

```bash
npm run caliper server
```

Then access the UI at `http://localhost:8090`

### Reports

After a test run, Caliper generates a report with performance metrics in `caliper/report`. Open the HTML report to analyze the results.

### Documenting Tests

Document your test configurations using comments in the YAML files. This helps with tracking and understanding test parameters.

### Advanced Configuration

Refer to the documentation for advanced configuration options, such as:

- Adding blockchain system adapters
- Extending resource monitoring
- Customizing performance analysis

### Logging

Caliper uses `winston` for logging. Configure `caliper-log-level` and `caliper-log-file` in your test YAML files.

### Automation

Integrate Caliper into your CI/CD pipeline by invoking `npm run caliper launch` with appropriate test configurations.

### Upgrading

When upgrading Caliper, review the release notes for any changes that may impact your tests or configurations.


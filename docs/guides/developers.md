# Developer's Guide

## Hyperledger Caliper Developer's Guide

This guide will help you understand the architecture and codebase of Hyperledger Caliper and provide instructions for contributing to the project.

### Architecture Overview

Caliper is designed with a modular architecture that separates the core benchmark logic from the blockchain-specific implementations. The main components are:

1. **Benchmark Engine**: The core component that orchestrates the execution of benchmark tests.
2. **Blockchain Adapters**: Implementations that integrate Caliper with specific blockchain systems (e.g., Fabric, Ethereum).
3. **Resource Monitors**: Modules that monitor system resources (e.g., CPU, memory) during benchmark runs.
4. **Performance Analyzers**: Components that process the collected data and generate performance reports.

### Codebase Structure

The Caliper codebase is organized as follows:

```
caliper/
├── benchmark/         # Default benchmark test cases
├── docs/              # Documentation
├── node_modules/      # Node.js dependencies
├── src/               # Source code
│   ├── contract/      # Smart contract files
│   ├── fabric/        # Fabric adapter implementation
│   ├── ethereum/      # Ethereum adapter implementation
│   ├── comm/          # Communication modules
│   ├── monitor/       # Resource monitor implementations
│   ├── report/        # Report generation modules
│   └── utils/         # Utility functions
├── test/              # Unit tests
├── caliper.js         # Caliper executable
├── package.json       # Node.js package file
└── ...
```

### Contributing

To contribute to Caliper, follow these steps:

1. Fork the Caliper repository on GitHub.
2. Clone your fork locally:

```bash
git clone https://github.com/anushatomar13/documentation-template
```

3. Create a new branch for your changes:

```bash
git checkout -b my-feature-branch
```

4. Make your changes and commit them with clear commit messages.
5. Push your changes to your fork:

```bash
git push origin my-feature-branch
```

6. Open a pull request against the main Caliper repository.

### Development Workflow

1. Install dependencies:

```bash
npm install
```

2. Run unit tests:

```bash
npm test
```

3. Start the development server for live reloading:

```bash
npm run caliper server
```

4. In another terminal, run benchmark tests:

```bash
npm run caliper launch -- <test_options>
```

### Documentation

The documentation is written in Markdown and built using MkDocs. To preview the docs locally:

```bash
mkdocs serve
```

Then, open `http://localhost:8000` in your web browser.

To build the documentation for publishing:

```bash
mkdocs build
```

The built documentation will be in the `site/` directory.


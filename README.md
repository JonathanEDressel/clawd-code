# Claw-Code Rewrite
Better Harness Tools, not merely an archive.

This repository provides a clean-room implementation and enhancement of the Claw Code harness. Following the exposure of the original source, this project was developed to provide a faster, memory-safe, and legally distinct version of the architecture for the developer community.

## Project Overview

Claw-Code is a high-performance harness designed to wire tools, orchestrate agent tasks, and manage complex runtime contexts. We are currently maintaining two primary implementations:

**Rust Port (`/rust`):** A systems-level implementation focusing on speed, memory safety, and providing a definitive harness runtime.

**Python Workspace (`/src`):** A clean-room rewrite that captures architectural patterns without proprietary code, ideal for rapid prototyping and parity auditing.

## Key Features

- **API Client:** Provider abstraction with OAuth and streaming support.
- **MCP Orchestration:** Seamless session state and tool manifest management.
- **Interactive CLI:** A robust REPL with markdown rendering and project bootstrap flows.
- **Plugin System:** A flexible hook pipeline for custom extensions.

> **Note:** This repository is a backup/mirror. For the actively maintained and updated version, visit [https://github.com/instructkr/claw-code](https://github.com/instructkr/claw-code).

## Support the Research

If these harness tools are helping you build better agent workflows, consider supporting the continued research and engineering. Your contributions help maintain the infrastructure and fuel further development passes.

### Crypto Donations

- **BTC:** [32BJw5mpyQ6fuLeiR5yrAAR2H8gerB9GAD]
- **ETH / ERC-20:** [0xc0066CCD708376cF3fA34CF5a3a8eB88AF58c97A]
- **SOL:** [7vfBGpjZTEZEsKNi1ZdYYBPGq1uFzWvLuV6xRP13tSo9]
- **XRP / Tag:** [rLHzPsX6oXkzU2qL12kHCH8G8cnZv1rBJh (Tag: 204756592)]

## Quickstart

### Python Workspace

Render the current porting summary and inspect the manifest:

```bash
python3 -m src.main summary
python3 -m src.main manifest
```

### Rust Implementation

For the high-performance build:

```bash
cd rust
cargo build --release
```

## Disclaimer

This repository does not claim ownership of the original Claw Code source material.

This repository is not affiliated with, endorsed by, or maintained by the original authors.

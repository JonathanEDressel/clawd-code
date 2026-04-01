# Claw-Code Rewrite
Better Harness Tools, not merely an archive.

## Table of Contents

- [Background: The Claude Code Exposure](#background-the-claude-code-exposure)
  - [Why Repositories Keep Getting Taken Down](#why-repositories-keep-getting-taken-down)
  - [Why This Repository Exists and Should Stay Available](#why-this-repository-exists-and-should-stay-available)
  - [What This Repository Is Not](#what-this-repository-is-not)
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Support the Research](#support-the-research)
- [Quickstart](#quickstart)
  - [Python Workspace](#python-workspace)
  - [Rust Implementation](#rust-implementation)
- [Disclaimer](#disclaimer)

---

This repository provides a clean-room implementation and enhancement of the Claw Code harness. Following the exposure of the original source, this project was developed to provide a faster, memory-safe, and legally distinct version of the architecture for the developer community.

---

## Background: The Claude Code Exposure

In early 2026, the internal source code for **Claude Code** — Anthropic's proprietary AI-assisted coding agent — was inadvertently exposed and circulated publicly. Claude Code had been in closed beta and select internal deployment as Anthropic's answer to AI-native development environments: a fully integrated agent harness capable of running tools, managing multi-step tasks, orchestrating sub-agents, maintaining session context, tracking costs, and interfacing with language models across multiple providers.

The leaked codebase revealed a sophisticated, production-grade system built on years of internal research. It included:

- A **multi-layer agent runtime** capable of spawning, supervising, and communicating between concurrent sub-agents
- A **tool dispatch and registration system** with dynamic plugin loading and permission gating
- A **session and transcript store** with structured history, cost attribution, and resumable context windows
- An **MCP (Model Context Protocol) client** for standardized tool-calling across providers
- A **bootstrap and project onboarding flow** that could clone settings, infer project structure, and pre-populate context
- A complete **CLI REPL** with rich rendering, keybinding support, and interactive dialogs
- A **remote runtime bridge** for dispatching tasks to isolated compute environments
- Extensive **parity auditing infrastructure** to track what had and hadn't been ported or validated

The exposure was not a simple config leak or credential dump. It was a full architectural disclosure — enough to understand exactly how Anthropic had structured an agentic coding system at production scale. Within days of circulation, forks, mirrors, and derivative repositories began disappearing from public hosting platforms as takedown pressure mounted.

### Why Repositories Keep Getting Taken Down

As with many leaks involving commercially sensitive IP, the response from platform hosts has been aggressive and coordinated. GitHub, GitLab, and several self-hosted forge instances have received DMCA-adjacent takedown requests citing proprietary source disclosure. Many mirrors and forks — even those containing only architectural notes or clean-room rewrites — have been removed without individual review, caught in broad sweeps targeting anything bearing identifiable naming conventions or structural fingerprints from the original.

This creates a chilling effect: researchers, developers, and engineers who want to study, extend, or simply understand how production-grade agent runtimes are architected are left without persistent access to the material. Legitimate uses — academic study, clean-room re-implementation, parity benchmarking, security auditing, and independent verification of the architecture's claims — are collateral damage in a takedown regime that treats visibility itself as the threat.

### Why This Repository Exists and Should Stay Available

This repository is **not a verbatim copy** of the leaked material. It is a clean-room re-implementation, a port, and an architectural study. The goal is to preserve the *ideas*, not the proprietary text — the same way textbooks describe algorithms without reproducing commercial implementations of them.

There are several concrete reasons this kind of work must remain accessible:

1. **Transparency and accountability.** When a company deploys an AI coding agent at scale, the architectural choices it makes have real consequences for users — around privacy, data retention, tool permissions, model routing, and cost. Public study of how these systems are built is how the community develops informed critique, not just credulous adoption.

2. **Educational value.** The Claude Code architecture represents one of the most complete public glimpses into how a production multi-agent system is actually structured — not in a research paper, but in deployed, tested code. This is precisely the kind of material that helps engineers level up from toy implementations to systems that work under real conditions.

3. **Re-implementation is not reproduction.** Clean-room rewrites have a long and legally recognized history in software. The Rust port in `/rust` and the Python workspace in `/src` were built by reading the architecture and re-expressing it, not copying it. The interfaces, patterns, and design decisions are studied here — not the literal source.

4. **Preservation against revisionism.** Once access to this material is erased, the narrative around it becomes easier to control. Keeping a study-grade mirror available means the existence and nature of the software remains part of the historical and technical record.

5. **Community continuity.** There are developers who had already begun building tools, workflows, and integrations on top of the architecture revealed in this leak before takedowns began. Those workflows deserve a stable reference point to continue development against.

### What This Repository Is Not

This repository is not a vehicle for any malicious use, unauthorized access to Anthropic systems, model piracy, or credential theft. We do not distribute API keys, model weights, proprietary datasets, or internal credentials. Nothing here enables circumventing Anthropic's access controls or abusing their services.

If you are here because you want to cause harm to Anthropic or its users, you are in the wrong place.

---

## Project Overview

Claw-Code is a high-performance harness designed to wire tools, orchestrate agent tasks, and manage complex runtime contexts. We are currently maintaining two primary implementations:

**Rust Port (`/rust`):** A systems-level implementation focusing on speed, memory safety, and providing a definitive harness runtime.

**Python Workspace (`/src`):** A clean-room rewrite that captures architectural patterns without proprietary code, ideal for rapid prototyping and parity auditing.

## Key Features

- **API Client:** Provider abstraction with OAuth and streaming support.
- **MCP Orchestration:** Seamless session state and tool manifest management.
- **Interactive CLI:** A robust REPL with markdown rendering and project bootstrap flows.
- **Plugin System:** A flexible hook pipeline for custom extensions.

## Support the Research

If these harness tools are helping you build better agent workflows, consider supporting the continued research and engineering. Your contributions help maintain the infrastructure and fuel further development passes.

### Crypto Donations

- **BTC:** 32BJw5mpyQ6fuLeiR5yrAAR2H8gerB9GAD
- **ETH / ERC-20:** 0xc0066CCD708376cF3fA34CF5a3a8eB88AF58c97A
- **SOL:** 7vfBGpjZTEZEsKNi1ZdYYBPGq1uFzWvLuV6xRP13tSo9
- **XRP / Tag:** rLHzPsX6oXkzU2qL12kHCH8G8cnZv1rBJh (Tag: 204756592)

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

> **Note:** This repository is a backup/mirror. For the actively maintained and updated version, visit [https://github.com/instructkr/claw-code](https://github.com/instructkr/claw-code).

---

If this repository has been useful to you — for research, learning, or building — consider giving it a **star**. It helps keep the mirror visible and signals to others that the work here is worth preserving.

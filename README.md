<div align="center">

<!-- Animated Typing Banner -->
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=2E9EF7&center=true&vCenter=true&multiline=true&repeat=true&width=600&height=100&lines=GraphQL+Development+Assistant;7+Agents+%7C+7+Skills+%7C+4+Commands;Production-Grade+Claude+Code+Plugin" alt="GraphQL Development Assistant" />

<br/>

<!-- Badge Row 1: Status Badges -->
[![Version](https://img.shields.io/badge/Version-2.0.0-blue?style=for-the-badge)](https://github.com/pluginagentmarketplace/custom-plugin-graphql/releases)
[![License](https://img.shields.io/badge/License-Custom-yellow?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production-brightgreen?style=for-the-badge)](#)
[![SASMP](https://img.shields.io/badge/SASMP-v1.3.0-blueviolet?style=for-the-badge)](#)

<!-- Badge Row 2: Content Badges -->
[![Agents](https://img.shields.io/badge/Agents-7-orange?style=flat-square&logo=robot)](#-agents)
[![Skills](https://img.shields.io/badge/Skills-7-purple?style=flat-square&logo=lightning)](#-skills)
[![Commands](https://img.shields.io/badge/Commands-4-green?style=flat-square&logo=terminal)](#-commands)

<br/>

<!-- Quick CTA Row -->
[**Install Now**](#-quick-start) | [**Explore Agents**](#-agents) | [**View Skills**](#-skills) | [**Star this repo**](https://github.com/pluginagentmarketplace/custom-plugin-graphql)

---

### What is this?

> **GraphQL Development Assistant** is a production-grade Claude Code plugin with **7 specialized agents** and **7 skills** for building GraphQL APIs - from fundamentals to production deployment.

</div>

---

## Table of Contents

<details>
<summary>Click to expand</summary>

- [Quick Start](#-quick-start)
- [Features](#-features)
- [Agents](#-agents)
- [Skills](#-skills)
- [Commands](#-commands)
- [Architecture](#-architecture)
- [Documentation](#-documentation)
- [Contributing](#-contributing)
- [License](#-license)

</details>

---

## Quick Start

### Prerequisites

- Claude Code CLI v2.0.27+
- Active Claude subscription

### Installation (Choose One)

<details open>
<summary><strong>Option 1: From Marketplace (Recommended)</strong></summary>

```bash
# Step 1: Add the plugin
/plugin marketplace add pluginagentmarketplace/custom-plugin-graphql

# Step 2: Restart Claude Code
# Close and reopen your terminal/IDE
```

</details>

<details>
<summary><strong>Option 2: Local Installation</strong></summary>

```bash
# Clone the repository
git clone https://github.com/pluginagentmarketplace/custom-plugin-graphql.git
cd custom-plugin-graphql

# Load locally
/plugin load .

# Restart Claude Code
```

</details>

### Verify Installation

After restart, you should see 7 GraphQL agents available.

---

## Features

| Feature | Description |
|---------|-------------|
| **7 Specialized Agents** | GraphQL Fundamentals, Schema Design, Resolvers, Apollo Server, Apollo Client, Security, Codegen |
| **7 Production Skills** | Complete code examples, patterns, and troubleshooting guides |
| **4 Interactive Commands** | Learn, Assess, Browse Agents, View Roadmaps |
| **SASMP v1.3.0** | Full protocol compliance with agent-skill bonding |
| **Production Patterns** | DataLoader, Federation, graphql-shield, TypeScript codegen |

---

## Agents

### 7 Specialized GraphQL Agents

| # | Agent | Purpose | Expertise |
|---|-------|---------|-----------|
| 1 | **01-graphql-fundamentals** | Core GraphQL educator | Types, queries, mutations, subscriptions, fragments |
| 2 | **02-graphql-schema** | Schema design architect | Naming conventions, pagination, error handling, interfaces |
| 3 | **03-graphql-resolvers** | Performance specialist | DataLoader, N+1 prevention, batching, context design |
| 4 | **04-graphql-apollo-server** | Server configuration expert | Apollo Server v4, plugins, federation, caching |
| 5 | **05-graphql-apollo-client** | React integration expert | Hooks, cache management, optimistic UI, subscriptions |
| 6 | **06-graphql-security** | Security architect | JWT auth, graphql-shield, rate limiting, validation |
| 7 | **07-graphql-codegen** | TypeScript code generation | Types, React hooks, configuration, fragments |

### Invoke Agents

```
Task(subagent_type="graphql:01-graphql-fundamentals")
Task(subagent_type="graphql:02-graphql-schema")
Task(subagent_type="graphql:03-graphql-resolvers")
Task(subagent_type="graphql:04-graphql-apollo-server")
Task(subagent_type="graphql:05-graphql-apollo-client")
Task(subagent_type="graphql:06-graphql-security")
Task(subagent_type="graphql:07-graphql-codegen")
```

---

## Skills

### 7 Production-Grade Skills

| Skill | Description | Complexity | Invoke |
|-------|-------------|------------|--------|
| **graphql-fundamentals** | Types, queries, mutations, subscriptions | Beginner | `Skill("graphql-fundamentals")` |
| **graphql-schema-design** | Naming, pagination, error patterns | Intermediate | `Skill("graphql-schema-design")` |
| **graphql-resolvers** | DataLoader, batching, N+1 prevention | Intermediate | `Skill("graphql-resolvers")` |
| **graphql-apollo-server** | Server v4, plugins, federation | Advanced | `Skill("graphql-apollo-server")` |
| **graphql-apollo-client** | React hooks, cache, optimistic UI | Intermediate | `Skill("graphql-apollo-client")` |
| **graphql-security** | Auth, rate limiting, validation | Advanced | `Skill("graphql-security")` |
| **graphql-codegen** | TypeScript types, React hooks | Intermediate | `Skill("graphql-codegen")` |

### Skill Features

Each skill includes:
- Quick reference tables
- Production code examples
- Troubleshooting guides
- Debug checklists
- Related skills and agents

---

## Commands

| Command | Description | Usage |
|---------|-------------|-------|
| `/learn` | Interactive GraphQL learning path | `/learn [topic]` |
| `/assess` | Knowledge assessment & skill gap analysis | `/assess [topic]` |
| `/browse-agent` | Explore 7 specialized GraphQL agents | `/browse-agent [name]` |
| `/roadmap` | Complete GraphQL learning roadmaps | `/roadmap [path]` |

### Example Usage

```bash
# Start learning GraphQL
/learn fundamentals

# Assess your knowledge
/assess

# Browse available agents
/browse-agent

# View full-stack roadmap
/roadmap full-stack
```

---

## Architecture

### Agent-Skill Bonding

```
Agent                         Skill (PRIMARY_BOND)
──────────────────────────────────────────────────
01-graphql-fundamentals  ←→  graphql-fundamentals
02-graphql-schema        ←→  graphql-schema-design
03-graphql-resolvers     ←→  graphql-resolvers
04-graphql-apollo-server ←→  graphql-apollo-server
05-graphql-apollo-client ←→  graphql-apollo-client
06-graphql-security      ←→  graphql-security
07-graphql-codegen       ←→  graphql-codegen
```

### Learning Path Dependencies

```
fundamentals (no prerequisites)
     ↓
schema-design (requires: fundamentals)
     ↓
resolvers (requires: fundamentals, schema)
     ↓
  ┌──┴──┐
  ↓     ↓
server  client (requires: fundamentals)
  │       │
  ↓       ↓
security codegen
```

---

## Project Structure

<details>
<summary>Click to expand</summary>

```
custom-plugin-graphql/
├── .claude-plugin/
│   ├── plugin.json          # Plugin manifest
│   └── marketplace.json     # Marketplace metadata
├── agents/                   # 7 specialized agents
│   ├── 01-graphql-fundamentals.md
│   ├── 02-graphql-schema.md
│   ├── 03-graphql-resolvers.md
│   ├── 04-graphql-apollo-server.md
│   ├── 05-graphql-apollo-client.md
│   ├── 06-graphql-security.md
│   └── 07-graphql-codegen.md
├── skills/                   # 7 production skills
│   ├── graphql-fundamentals/SKILL.md
│   ├── graphql-schema-design/SKILL.md
│   ├── graphql-resolvers/SKILL.md
│   ├── graphql-apollo-server/SKILL.md
│   ├── graphql-apollo-client/SKILL.md
│   ├── graphql-security/SKILL.md
│   └── graphql-codegen/SKILL.md
├── commands/                 # 4 interactive commands
│   ├── learn.md
│   ├── assess.md
│   ├── browse-agent.md
│   └── roadmap.md
├── hooks/
│   └── hooks.json
├── README.md
├── CHANGELOG.md
└── LICENSE
```

</details>

---

## Documentation

| Document | Description |
|----------|-------------|
| [CHANGELOG.md](CHANGELOG.md) | Version history |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to contribute |
| [LICENSE](LICENSE) | License information |

---

## Metadata

| Field | Value |
|-------|-------|
| **Version** | 2.0.0 |
| **Last Updated** | 2025-12-30 |
| **Status** | Production Ready |
| **SASMP** | v1.3.0 |
| **Agents** | 7 |
| **Skills** | 7 |
| **Commands** | 4 |

---

## Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md).

1. Fork the repository
2. Create your feature branch
3. Follow SASMP v1.3.0 for new agents/skills
4. Submit a pull request

---

## Security

> **Important:** This repository contains third-party code and dependencies.
>
> - Always review code before using in production
> - Check dependencies for known vulnerabilities
> - Follow security best practices
> - Report security issues privately via [Issues](../../issues)

---

## License

Copyright 2025 **Dr. Umit Kacar** & **Muhsin Elcicek**

Custom License - See [LICENSE](LICENSE) for details.

---

## Contributors

<table>
<tr>
<td align="center">
<strong>Dr. Umit Kacar</strong><br/>
Senior AI Researcher & Engineer
</td>
<td align="center">
<strong>Muhsin Elcicek</strong><br/>
Senior Software Architect
</td>
</tr>
</table>

---

<div align="center">

**Made with care for the Claude Code Community**

[![GitHub](https://img.shields.io/badge/GitHub-pluginagentmarketplace-black?style=for-the-badge&logo=github)](https://github.com/pluginagentmarketplace)

</div>

<div align="center">

<!-- Animated Typing Banner -->
<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=28&duration=3000&pause=1000&color=2E9EF7&center=true&vCenter=true&multiline=true&repeat=true&width=600&height=100&lines=Prompt+Engineering+Assistant;7+Agents+%7C+7+Skills;Claude+Code+Plugin" alt="Prompt Engineering Assistant" />

<br/>

<!-- Badge Row 1: Status Badges -->
[![Version](https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge)](https://github.com/pluginagentmarketplace/custom-plugin-prompt-engineering/releases)
[![License](https://img.shields.io/badge/License-Custom-yellow?style=for-the-badge)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Production-brightgreen?style=for-the-badge)](#)
[![SASMP](https://img.shields.io/badge/SASMP-v1.3.0-blueviolet?style=for-the-badge)](#)

<!-- Badge Row 2: Content Badges -->
[![Agents](https://img.shields.io/badge/Agents-7-orange?style=flat-square&logo=robot)](#-agents)
[![Skills](https://img.shields.io/badge/Skills-7-purple?style=flat-square&logo=lightning)](#-skills)
[![Commands](https://img.shields.io/badge/Commands-1-green?style=flat-square&logo=terminal)](#-commands)

<br/>

<!-- Quick CTA Row -->
[📦 **Install Now**](#-quick-start) · [🤖 **Explore Agents**](#-agents) · [📖 **Documentation**](#-documentation) · [⭐ **Star this repo**](https://github.com/pluginagentmarketplace/custom-plugin-prompt-engineering)

---

### What is this?

> **Prompt Engineering Assistant** is a Claude Code plugin with **7 agents** and **7 skills** for prompt engineering development.

</div>

---

## 📑 Table of Contents

<details>
<summary>Click to expand</summary>

- [Quick Start](#-quick-start)
- [Features](#-features)
- [Agents](#-agents)
- [Skills](#-skills)
- [Commands](#-commands)
- [Documentation](#-documentation)
- [Contributing](#-contributing)
- [License](#-license)

</details>

---

## 🚀 Quick Start

### Prerequisites

- Claude Code CLI v2.0.27+
- Active Claude subscription

### Installation (Choose One)

<details open>
<summary><strong>Option 1: From Marketplace (Recommended)</strong></summary>

```bash
# Step 1️⃣ Add the marketplace
/plugin add marketplace pluginagentmarketplace/custom-plugin-prompt-engineering

# Step 2️⃣ Install the plugin
/plugin install prompt-engineering-assistant@pluginagentmarketplace-prompt-engineering

# Step 3️⃣ Restart Claude Code
# Close and reopen your terminal/IDE
```

</details>

<details>
<summary><strong>Option 2: Local Installation</strong></summary>

```bash
# Clone the repository
git clone https://github.com/pluginagentmarketplace/custom-plugin-prompt-engineering.git
cd custom-plugin-prompt-engineering

# Load locally
/plugin load .

# Restart Claude Code
```

</details>

### ✅ Verify Installation

After restart, you should see these agents:

```
prompt-engineering-assistant:07-advanced-techniques-agent
prompt-engineering-assistant:01-prompt-fundamentals-agent
prompt-engineering-assistant:03-chain-of-thought-agent
prompt-engineering-assistant:05-prompt-optimization-agent
prompt-engineering-assistant:06-evaluation-testing-agent
... and 2 more
```

---

## ✨ Features

| Feature | Description |
|---------|-------------|
| 🤖 **7 Agents** | Specialized AI agents for prompt engineering tasks |
| 🛠️ **7 Skills** | Reusable capabilities with Golden Format |
| ⌨️ **1 Commands** | Quick slash commands |
| 🔄 **SASMP v1.3.0** | Full protocol compliance |

---

## 🤖 Agents

### 7 Specialized Agents

| # | Agent | Purpose |
|---|-------|---------|
| 1 | **07-advanced-techniques-agent** | Advanced prompting specialist - Implements meta-prompting, s |
| 2 | **01-prompt-fundamentals-agent** | Prompt engineering fundamentals specialist - Teaches core co |
| 3 | **03-chain-of-thought-agent** | Chain-of-thought reasoning specialist - Implements step-by-s |
| 4 | **05-prompt-optimization-agent** | Prompt optimization specialist - Refines prompts for token e |
| 5 | **06-evaluation-testing-agent** | Prompt evaluation specialist - Tests prompt robustness, meas |
| 6 | **04-react-pattern-agent** | ReAct pattern specialist - Implements Reasoning+Acting patte |
| 7 | **02-few-shot-specialist-agent** | Few-shot prompting expert - Designs effective example-based  |

---

## 🛠️ Skills

### Available Skills

| Skill | Description | Invoke |
|-------|-------------|--------|
| `prompt-design` | Core prompt design patterns and templates for effective LLM  | `Skill("prompt-engineering-assistant:prompt-design")` |
| `prompt-evaluation` | Prompt testing, metrics, and A/B testing frameworks | `Skill("prompt-engineering-assistant:prompt-evaluation")` |
| `chain-of-thought` | Step-by-step reasoning patterns for complex problem solving | `Skill("prompt-engineering-assistant:chain-of-thought")` |
| `structured-output` | JSON, XML, and structured data generation patterns | `Skill("prompt-engineering-assistant:structured-output")` |
| `prompt-templates` | Reusable prompt templates for common tasks and optimization  | `Skill("prompt-engineering-assistant:prompt-templates")` |
| `react-pattern` | Reasoning and Acting patterns for agentic LLM workflows | `Skill("prompt-engineering-assistant:react-pattern")` |
| `few-shot-prompting` | Example-based prompting techniques for in-context learning | `Skill("prompt-engineering-assistant:few-shot-prompting")` |

---

## ⌨️ Commands

| Command | Description |
|---------|-------------|
| `/prompt-review` | Review and improve a prompt for better LLM performance |

---

## 📚 Documentation

| Document | Description |
|----------|-------------|
| [CHANGELOG.md](CHANGELOG.md) | Version history |
| [CONTRIBUTING.md](CONTRIBUTING.md) | How to contribute |
| [LICENSE](LICENSE) | License information |

---

## 📁 Project Structure

<details>
<summary>Click to expand</summary>

```
custom-plugin-prompt-engineering/
├── 📁 .claude-plugin/
│   ├── plugin.json
│   └── marketplace.json
├── 📁 agents/              # 7 agents
├── 📁 skills/              # 7 skills (Golden Format)
├── 📁 commands/            # 1 commands
├── 📁 hooks/
├── 📄 README.md
├── 📄 CHANGELOG.md
└── 📄 LICENSE
```

</details>

---

## 📅 Metadata

| Field | Value |
|-------|-------|
| **Version** | 1.0.0 |
| **Last Updated** | 2025-12-29 |
| **Status** | Production Ready |
| **SASMP** | v1.3.0 |
| **Agents** | 7 |
| **Skills** | 7 |
| **Commands** | 1 |

---

## 🤝 Contributing

Contributions are welcome! Please read our [Contributing Guide](CONTRIBUTING.md).

1. Fork the repository
2. Create your feature branch
3. Follow the Golden Format for new skills
4. Submit a pull request

---

## ⚠️ Security

> **Important:** This repository contains third-party code and dependencies.
>
> - ✅ Always review code before using in production
> - ✅ Check dependencies for known vulnerabilities
> - ✅ Follow security best practices
> - ✅ Report security issues privately via [Issues](../../issues)

---

## 📝 License

Copyright © 2025 **Dr. Umit Kacar** & **Muhsin Elcicek**

Custom License - See [LICENSE](LICENSE) for details.

---

## 👥 Contributors

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

**Made with ❤️ for the Claude Code Community**

[![GitHub](https://img.shields.io/badge/GitHub-pluginagentmarketplace-black?style=for-the-badge&logo=github)](https://github.com/pluginagentmarketplace)

</div>

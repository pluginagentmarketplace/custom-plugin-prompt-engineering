---
name: prompt-templates
description: Reusable prompt templates for common tasks and optimization patterns
sasmp_version: "1.3.0"
bonded_agent: prompt-optimization-agent
bond_type: PRIMARY_BOND
---

# Prompt Templates Skill

**Bonded to:** `prompt-optimization-agent`

---

## Quick Start

```bash
Skill("custom-plugin-prompt-engineering:prompt-templates")
```

---

## Available Templates

1. Code Review Template
2. Documentation Generator
3. Bug Analysis Template
4. API Design Template
5. Test Case Generator

---

## Usage

Templates use `{variable}` placeholders for customization.

```
You are a {role} expert.
Analyze the following {input_type}:
{content}

Provide {output_format}.
```

---

## References

See `assets/` for template files.

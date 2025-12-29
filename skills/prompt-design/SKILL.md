---
name: prompt-design
description: Core prompt design patterns and templates for effective LLM communication
sasmp_version: "1.3.0"
bonded_agent: prompt-fundamentals-agent
bond_type: PRIMARY_BOND
---

# Prompt Design Skill

**Bonded to:** `prompt-fundamentals-agent`

---

## Quick Start

```bash
Skill("custom-plugin-prompt-engineering:prompt-design")
```

---

## Instructions

1. Define the task objective clearly
2. Specify the role/persona for the LLM
3. Provide necessary context
4. Set output format requirements
5. Add constraints and guardrails

---

## Core Patterns

### ROLE-CONTEXT-TASK-FORMAT

```
You are a [ROLE] with expertise in [DOMAIN].

Context: [RELEVANT BACKGROUND]

Task: [SPECIFIC REQUEST]

Format: [OUTPUT STRUCTURE]
```

### INSTRUCTION-INPUT-OUTPUT

```
Instruction: [WHAT TO DO]
Input: [DATA TO PROCESS]
Output: [EXPECTED RESULT FORMAT]
```

---

## Examples

### Code Review Prompt

```
You are a senior software engineer reviewing code.

Review the following code for:
- Security vulnerabilities
- Performance issues
- Best practice violations

Provide feedback in this format:
- Issue: [description]
- Severity: [high/medium/low]
- Fix: [recommendation]
```

---

## References

See `references/` for detailed methodology guides.

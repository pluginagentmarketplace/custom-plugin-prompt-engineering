---
name: chain-of-thought
description: Step-by-step reasoning patterns for complex problem solving
sasmp_version: "1.3.0"
bonded_agent: chain-of-thought-agent
bond_type: PRIMARY_BOND
---

# Chain-of-Thought Skill

**Bonded to:** `chain-of-thought-agent`

---

## Quick Start

```bash
Skill("custom-plugin-prompt-engineering:chain-of-thought")
```

---

## Instructions

1. Add "Let's think step by step" trigger
2. Break problem into logical steps
3. Show intermediate reasoning
4. Verify each step before proceeding
5. Summarize final answer

---

## Patterns

### Basic CoT

```
Q: [Complex question]
A: Let's think step by step.
   Step 1: [First reasoning step]
   Step 2: [Second reasoning step]
   Step 3: [Third reasoning step]
   Therefore, the answer is: [Final answer]
```

### Self-Consistency CoT

Generate multiple reasoning paths and select the most consistent answer.

---

## References

See `references/` for advanced CoT techniques.

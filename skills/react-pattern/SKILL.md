---
name: react-pattern
description: Reasoning and Acting patterns for agentic LLM workflows
sasmp_version: "1.3.0"
bonded_agent: react-pattern-agent
bond_type: PRIMARY_BOND
---

# ReAct Pattern Skill

**Bonded to:** `react-pattern-agent`

---

## Quick Start

```bash
Skill("custom-plugin-prompt-engineering:react-pattern")
```

---

## Instructions

1. Define available tools/actions
2. Structure Thought-Action-Observation loop
3. Implement reasoning before action
4. Process observations and iterate
5. Know when to stop

---

## Pattern

```
Thought: I need to [reasoning about what to do]
Action: [tool_name](parameters)
Observation: [result from action]

Thought: Based on this, I should [next reasoning]
Action: [next_action]
Observation: [result]

Thought: I now have enough information
Final Answer: [conclusion]
```

---

## References

See `references/` for tool integration guides.

---
name: structured-output
description: JSON, XML, and structured data generation patterns
sasmp_version: "1.3.0"
bonded_agent: advanced-techniques-agent
bond_type: PRIMARY_BOND
---

# Structured Output Skill

**Bonded to:** `advanced-techniques-agent`

---

## Quick Start

```bash
Skill("custom-plugin-prompt-engineering:structured-output")
```

---

## Patterns

### JSON Output

```
Respond in valid JSON format:
{
  "field1": "value",
  "field2": ["item1", "item2"],
  "field3": {
    "nested": "value"
  }
}
```

### Schema-Constrained

```
Output must match this schema:
{
  "type": "object",
  "properties": {
    "name": {"type": "string"},
    "score": {"type": "number", "minimum": 0, "maximum": 100}
  },
  "required": ["name", "score"]
}
```

---

## References

See `assets/` for schema templates.

---
name: few-shot-prompting
description: Example-based prompting techniques for in-context learning
sasmp_version: "1.3.0"
bonded_agent: few-shot-specialist-agent
bond_type: PRIMARY_BOND
---

# Few-Shot Prompting Skill

**Bonded to:** `few-shot-specialist-agent`

---

## Quick Start

```bash
Skill("custom-plugin-prompt-engineering:few-shot-prompting")
```

---

## Instructions

1. Select diverse, representative examples
2. Format examples consistently
3. Order examples strategically
4. Balance example count (3-5 typically optimal)
5. Include edge cases when relevant

---

## Patterns

### Standard Few-Shot

```
Example 1:
Input: [input1]
Output: [output1]

Example 2:
Input: [input2]
Output: [output2]

Now process:
Input: [new_input]
Output:
```

### Labeled Few-Shot

```
Classify the sentiment:

Text: "I love this product!" -> Positive
Text: "Terrible experience" -> Negative
Text: "It's okay, nothing special" -> Neutral

Text: "[new_text]" ->
```

---

## References

See `references/` for example selection strategies.

---
name: prompt-evaluation
description: Prompt testing, metrics, and A/B testing frameworks
sasmp_version: "1.3.0"
bonded_agent: evaluation-testing-agent
bond_type: PRIMARY_BOND
---

# Prompt Evaluation Skill

**Bonded to:** `evaluation-testing-agent`

---

## Quick Start

```bash
Skill("custom-plugin-prompt-engineering:prompt-evaluation")
```

---

## Metrics

1. **Accuracy** - Correct outputs / Total outputs
2. **Consistency** - Same input produces same output
3. **Robustness** - Handles edge cases gracefully
4. **Efficiency** - Token usage vs quality tradeoff

---

## Test Framework

```python
test_cases = [
    {"input": "...", "expected": "...", "category": "basic"},
    {"input": "...", "expected": "...", "category": "edge"},
]

def evaluate_prompt(prompt, test_cases):
    results = []
    for test in test_cases:
        output = run_prompt(prompt, test["input"])
        results.append(compare(output, test["expected"]))
    return calculate_metrics(results)
```

---

## References

See `scripts/` for evaluation scripts.

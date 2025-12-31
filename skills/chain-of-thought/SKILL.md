---
name: chain-of-thought
description: Step-by-step reasoning patterns for complex problem solving
sasmp_version: "1.3.0"
bonded_agent: 03-chain-of-thought-agent
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

## Parameter Schema

```yaml
parameters:
  cot_type:
    type: enum
    values: [zero_shot, few_shot, self_consistency, tree_of_thought]
    default: zero_shot

  verbosity:
    type: enum
    values: [minimal, standard, detailed]
    default: standard

  verification:
    type: boolean
    default: true
    description: Include self-verification step
```

---

## CoT Variants

| Variant | Description | Accuracy | Token Cost |
|---------|-------------|----------|------------|
| Zero-shot CoT | "Let's think step by step" | Good | Low |
| Few-shot CoT | Examples with reasoning | Better | Medium |
| Self-consistency | Multiple paths, vote | Best | High |
| Tree-of-Thought | Branch and evaluate | Best | Highest |

---

## Core Patterns

### 1. Zero-Shot Chain-of-Thought

```markdown
[Problem statement]

Let's think step by step.
```

**Trigger phrases:**
- "Let's think step by step"
- "Let's work through this systematically"
- "Let me break this down"
- "Let's solve this step by step"

### 2. Few-Shot Chain-of-Thought

```markdown
Q: [Example problem 1]
A: Let's think step by step.
   Step 1: [reasoning]
   Step 2: [reasoning]
   Step 3: [reasoning]
   Therefore, the answer is: [answer]

Q: [Example problem 2]
A: Let's think step by step.
   Step 1: [reasoning]
   Step 2: [reasoning]
   Therefore, the answer is: [answer]

Q: [Actual problem]
A: Let's think step by step.
```

### 3. Self-Consistency

```yaml
process:
  1_generate: "Generate N reasoning paths (temperature > 0)"
  2_extract: "Extract final answer from each path"
  3_vote: "Select answer with highest frequency"
  4_confidence: "Confidence = frequency / N"

parameters:
  n_paths: 5
  temperature: 0.7
  selection: majority_vote
```

### 4. Plan-and-Solve

```markdown
Q: [Complex problem]

A: Let's first understand the problem and devise a plan.

## Understanding
[Restate the problem and identify key elements]

## Plan
1. [Step 1 description]
2. [Step 2 description]
3. [Step 3 description]

## Execution
Step 1: [Execute and explain]
Step 2: [Execute and explain]
Step 3: [Execute and explain]

## Verification
[Check if solution satisfies requirements]

## Final Answer
[Conclusion]
```

---

## Domain-Specific Triggers

```yaml
triggers_by_domain:
  mathematics:
    - "Let's solve this step by step, showing all work"
    - "First, let's identify what we know and what we need to find"

  coding:
    - "Let's trace through the logic step by step"
    - "Let me walk through this algorithm"

  logic:
    - "Let's analyze each premise systematically"
    - "Let me reason through this logically"

  analysis:
    - "Let's break this down into components"
    - "Let me examine this from multiple angles"
```

---

## Validation

```yaml
validation_checklist:
  logical_flow:
    - [ ] Each step follows from previous
    - [ ] No logical gaps
    - [ ] No circular reasoning

  completeness:
    - [ ] All sub-problems addressed
    - [ ] Edge cases considered
    - [ ] Assumptions stated

  conclusion:
    - [ ] Follows from final step
    - [ ] Directly answers question
    - [ ] Confidence indicated
```

---

## Troubleshooting

| Issue | Cause | Solution |
|-------|-------|----------|
| Skips steps | Steps too obvious | Add intermediate steps |
| Wrong answer | Error in early step | Add verification at each step |
| Inconsistent | Single path variance | Use self-consistency |
| Too verbose | Over-explanation | Use minimal verbosity |
| Token overflow | Too many steps | Consolidate related steps |

---

## Integration

```yaml
integrates_with:
  - few-shot-prompting: Examples with reasoning
  - prompt-design: Base structure
  - self-reflection: Verify reasoning

combination_patterns:
  cot_plus_few_shot: "Examples showing reasoning steps"
  cot_plus_self_consistency: "Multiple reasoning paths"
  cot_plus_verification: "Reasoning with self-check"
```

---

## References

See `references/GUIDE.md` for advanced CoT techniques.
See `assets/config.yaml` for configuration options.

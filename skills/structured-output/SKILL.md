---
name: structured-output
description: JSON, XML, and structured data generation patterns
sasmp_version: "1.3.0"
bonded_agent: 07-advanced-techniques-agent
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

## Parameter Schema

```yaml
parameters:
  output_format:
    type: enum
    values: [json, yaml, xml, csv, markdown_table]
    default: json

  schema_validation:
    type: boolean
    default: true

  strict_mode:
    type: boolean
    default: false
    description: "Fail on any schema violation"
```

---

## Output Formats

### JSON Output

```markdown
Respond with valid JSON only. No additional text before or after.

Schema:
{
  "field1": "string value",
  "field2": 123,
  "field3": ["array", "items"],
  "field4": {
    "nested": "object"
  }
}
```

### YAML Output

```markdown
Respond with valid YAML only.

field1: string value
field2: 123
field3:
  - array
  - items
field4:
  nested: object
```

### XML Output

```markdown
Respond with valid XML only.

<root>
  <field1>string value</field1>
  <field2>123</field2>
  <field3>
    <item>array</item>
    <item>items</item>
  </field3>
</root>
```

---

## Schema Enforcement Patterns

### JSON Schema

```markdown
Output must strictly match this JSON Schema:

{
  "$schema": "http://json-schema.org/draft-07/schema#",
  "type": "object",
  "properties": {
    "name": {
      "type": "string",
      "minLength": 1,
      "maxLength": 100
    },
    "score": {
      "type": "number",
      "minimum": 0,
      "maximum": 100
    },
    "tags": {
      "type": "array",
      "items": {"type": "string"},
      "maxItems": 5
    }
  },
  "required": ["name", "score"],
  "additionalProperties": false
}
```

### TypeScript-Style Schema

```markdown
Output must match this TypeScript interface:

interface Response {
  name: string;           // Required, non-empty
  score: number;          // 0-100
  tags?: string[];        // Optional, max 5 items
  metadata?: {
    created: string;      // ISO date format
    version: number;
  };
}
```

### Pydantic-Style Schema

```markdown
Output must match this Pydantic model:

class Response(BaseModel):
    name: str = Field(..., min_length=1, max_length=100)
    score: float = Field(..., ge=0, le=100)
    tags: Optional[List[str]] = Field(default=None, max_items=5)
```

---

## Prompting Techniques

### 1. Schema-First Prompting

```markdown
## Output Schema
[Define exact schema]

## Task
[What to do]

## Input
[Data to process]

Remember: Output ONLY valid [format] matching the schema above.
```

### 2. Example-Guided Output

```markdown
## Task
Extract entities from text.

## Example
Input: "Apple CEO Tim Cook announced iPhone 15"
Output: {
  "entities": [
    {"name": "Apple", "type": "ORG"},
    {"name": "Tim Cook", "type": "PERSON"},
    {"name": "iPhone 15", "type": "PRODUCT"}
  ]
}

## Your Turn
Input: "[actual_text]"
Output:
```

### 3. Constrained Generation

```markdown
Generate output following these STRICT rules:
1. Valid JSON only
2. No markdown code blocks
3. No explanatory text
4. Exactly these fields: [field_list]
5. All strings in quotes
6. No trailing commas
```

---

## Validation Strategies

```yaml
validation_layers:
  syntax:
    - JSON/YAML/XML parse check
    - Well-formed structure
    - Proper encoding

  schema:
    - Required fields present
    - Types match
    - Constraints satisfied

  semantic:
    - Values make sense
    - References are valid
    - Business rules met

recovery:
  on_parse_error: "Request regeneration with error details"
  on_schema_error: "Identify specific violations, request fix"
  on_semantic_error: "Flag for review"
```

---

## Common Patterns

### Entity Extraction

```json
{
  "entities": [
    {"text": "extracted text", "type": "ENTITY_TYPE", "confidence": 0.95}
  ]
}
```

### Classification Result

```json
{
  "label": "category_name",
  "confidence": 0.87,
  "alternatives": [
    {"label": "other_category", "confidence": 0.10}
  ]
}
```

### Analysis Report

```json
{
  "summary": "Brief summary",
  "findings": [
    {"id": 1, "description": "Finding", "severity": "high"}
  ],
  "recommendations": ["Action 1", "Action 2"],
  "metadata": {"analyzed_at": "2025-01-01T00:00:00Z"}
}
```

---

## Troubleshooting

| Issue | Cause | Solution |
|-------|-------|----------|
| Invalid JSON | Missing quotes/commas | Add syntax examples |
| Extra text | Not enforced | Add "JSON only" constraint |
| Missing fields | Schema not clear | Use required field markers |
| Wrong types | Type confusion | Add type examples |
| Nested issues | Complex structure | Flatten or simplify schema |

---

## Integration

```yaml
integrates_with:
  - prompt-design: Structure prompt for output
  - prompt-evaluation: Validate output quality
  - react-pattern: Tool return formats

parsing_libraries:
  python: json, pydantic, jsonschema
  javascript: ajv, zod
  go: encoding/json, gojsonschema
```

---

## References

See `references/GUIDE.md` for advanced schema patterns.
See `assets/config.yaml` for configuration options.

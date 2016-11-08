---
title: Spacing
toc: false
---

Spacing check on if, for, while, switch, try statements and around operators.

### Configuration

```json
{
    "type": "Spacing",
    "props": {
        "severity": "INFO",
        "spaceIfCondition": "should",
        "spaceForLoop": "should",
        "spaceWhileLoop": "should",
        "spaceSwitchCase": "should",
        "spaceCatch": "should",
        "spaceAroundBinop": true,
        "noSpaceAroundUnop": true,
        "ignoreRangeOperator": true
    }
}
```

Valid values for `spaceIfCondition`, `spaceForLoop`, `spaceWhileLoop`, `spaceSwitchCase` and `spaceCatch` are:

- `should` - space should be there between statement and condition
- `shouldNot` - space should not be there between statement and condition
- `any` - ignores the space check

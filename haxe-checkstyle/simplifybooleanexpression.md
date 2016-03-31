---
title: Simplify Boolean Expression
toc: false
---

Checks for over-complicated boolean expressions. Finds code like `if (b == true), b || true, !false`, etc.

### Configuration

```json
{
    "type": "SimplifyBooleanExpression",
    "props": {
        "severity": "ERROR"
    }
}
```
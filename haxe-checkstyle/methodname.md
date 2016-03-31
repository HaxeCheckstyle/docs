---
title: Method Name
toc: false
---

Checks that method names conform to a format specified by the `format` property.

### Configuration

```json
{
    "type": "MethodName",
    "props": {
        "severity": "ERROR",
        "format": "^[a-z][a-zA-Z0-9]*$",
        "tokens": [
        "PUBLIC",
        "PRIVATE",
        "STATIC",
        "NOTSTATIC",
        "INLINE",
        "NOTINLINE"
        ]
    }
}
```

You can define different rules for different type of methods using the `tokens` property.

The above regex allows `camelCase` names.
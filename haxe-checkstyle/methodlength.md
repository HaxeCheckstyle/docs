---
title: Method Length
toc: false
---

Checks for long methods. If a method becomes very long it is hard to understand.
Therefore long methods should usually be refactored into several individual methods that focus on a specific task.

### Configuration

```json
{
    "type": "MethodLength",
    "props": {
        "severity": "ERROR",
        "max": 50,
        "ignoreEmptyLines": true
    }
}
```

### Options

**`ignoreEmptyLines`** - ignores or includes empty lines when counting method length (available since 2.6.0)

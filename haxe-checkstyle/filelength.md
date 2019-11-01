---
title: File Length
toc: false
---

Checks for long source files. If a source file becomes very long it is hard to understand.
Therefore long classes should usually be refactored into several individual classes that focus on a specific task.

### Configuration

```json
{
    "type": "FileLength",
    "props": {
        "severity": "WARNING",
        "max": 1000,
        "ignoreEmptyLines": true
    }
}
```

### Options

**`ignoreEmptyLines`** - ignores or includes empty lines when counting total file length (available since 2.6.0)

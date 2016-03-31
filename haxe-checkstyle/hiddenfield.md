---
title: Hidden Field
toc: false
---

Checks that a local variable or a parameter does not shadow a field that is defined in the same class.

### Configuration

```json
{
    "type": "HiddenField",
    "props": {
    "ignoreSetter": true,
    "ignoreFormat": "^(main|run)$",
    "ignoreConstructorParameter": true,
    "severity": "ERROR"
    }
}
```
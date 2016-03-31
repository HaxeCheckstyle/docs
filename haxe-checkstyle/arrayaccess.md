---
title: Array Access
toc: false
---

Checks for spaces before array access or inside array elements. Finds code like `a [0], a[ 0]`, etc.

### Configuration

```json
{
    "type": "ArrayAccess",
    "props": {
        "spaceBefore": false,
        "spaceInside": false,
        "severity": "INFO"
    }
}
```
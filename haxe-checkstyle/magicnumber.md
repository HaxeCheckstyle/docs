---
title: Magic Number
keywords: magic, number
toc: false
---

Checks that there are no magic numbers. By default, -1, 0, 1, and 2 are not considered to be magic numbers.

### Configuration

```json
{
    "type": "MagicNumber",
    "props": {
        "ignoreNumbers": [-1, 0, 1, 2],
        "severity": "INFO"
    }
}
```
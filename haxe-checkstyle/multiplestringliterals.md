---
title: Multiple String Literals
toc: false
---

Checks for multiple occurrences of the same string literal within a single file.
Code duplication makes maintenance more difficult, so it's better to replace the multiple occurrences with a constant.

### Configuration

```json
{
    "type": "MultipleStringLiterals",
    "props": {
        "minLength": 2,
        "ignore": "^\\s+$",
        "allowDuplicates": 2,
        "severity": "WARNING"
    }
}
```
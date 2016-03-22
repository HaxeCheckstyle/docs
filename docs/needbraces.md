---
title: Need Braces
keywords: needbraces
toc: false
---

Checks for braces on function, if, for and while statements. It has an option to allow single line statements without braces using property `allowSingleLineStatement` like `if (b) return 10;`.

### Configuration

```json
{
    "type": "NeedBraces",
    "props": {
        "allowSingleLineStatement": true,
        "tokens": [
            "FOR",
            "IF",
            "ELSE_IF",
            "WHILE",
            "DO_WHILE"
        ],
        "severity": "INFO"
    }
}
```
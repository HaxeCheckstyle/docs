---
title: String Literal
keywords: literal, string
toc: false
---

Checks for single or double quote string literals.

### Configuration

```json
{
    "type": "StringLiteral",
    "props": {
        "policy": "doubleAndInterpolation",
        "allowException": true,
        "severity": "INFO"
    }
}
```

Available policy values are:

| Policy                   | Description                                                  |
| ------------------------ | ------------------------------------------------------------ |
| `onlySingle`             | enforce single quotes                                        |
| `onlyDouble`             | enforce double quotes, no interpolation allowed              |
| `doubleAndInterpolation` | enforce double quotes, allow single quotes for interpolation |

`allowException` allows using single quotes in `onlyDouble` and `doubleAndInterpolation` mode, when string contains a double quote character. Or double quotes in `onlySingle`mode when string contains a single quote character, reducing the need to escape quotation marks.
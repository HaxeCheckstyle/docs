---
title: Separator Whitespace
keywords: whitespace, separator
toc: false
---

Checks that whitespace is present or absent around a separators.

### Configuration

```json
{
    "type": "SeparatorWhitespace",
    "props": {
        "severity": "WARNING",
        "dotPolicy": "around",
        "commaPolicy": "none",
        "semicolonPolicy": "none"
    }
}
```

| Policy                 | Operators
| ---------------------- | ------------- |
| `dotPolicy`            | `.`           |
| `commaPolicy`          | `,`           |
| `semicolonPolicy`      | `;`           |

<br>

Available policy values are:

| Option     | Description |
| --------- | ----------- |
| `around`  | enforce whitespace before and after operator |
| `before`  | enforce whitespace before and no whitespace after operator |
| `after`   | enforce no whitespace before and whitespace after operator |
| `none`    | enforce no whitespace before and after operator |
| `ignore`  | skip checks |


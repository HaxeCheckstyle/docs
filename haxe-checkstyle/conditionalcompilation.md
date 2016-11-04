---
title: Conditional Compilation
toc: false
---

Checks placement and indentation of conditional compilation flags.

### Configuration

```json
{
    "type": "ConditionalCompilation",
    "props": {
        "policy": "aligned",
        "allowSingleline": true,
        "severity": "INFO"
    }
}
```

| Policy        | Description                                                                      |
| ------------- | -------------------------------------------------------------------------------- |
| `aligned`     | Indentation of #if, #else, #elseif and #end match surrounding code               |
| `startOfLine` | #if, #else, #elseif and #end must start at beginning of line                     |

Both `aligned` and `startOfLine` will produce a message if conditional compilation flags are not on a separate line. All #else, #elseif and #end flags must have the same indentation as their corresponding #if.
`allowSingleline` allows or prevents using single line conditional compilation flags.
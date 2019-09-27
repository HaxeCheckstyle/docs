---
title: Avoid Inline Conditionals
toc: false
---

Detects use of ternary operator. Useful for developers who find ternary operators hard to read and want forbid them.

### Configuration

```json
{
    "type": "AvoidInlineConditionals",
    "props": {
        "severity": "ERROR"
    }
}
```

### Invalid
```
var keycode = (event.keyCode != null) ? event.keyCode : event.which;
```
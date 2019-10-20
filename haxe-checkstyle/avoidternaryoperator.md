---
title: Avoid Ternary Operator
toc: false
---

Detects ternary operators. Useful for developers who find ternary operators hard to read and want forbid them.
AvoidTernaryOperator was renamed from AvoidInlineConditionals in 2.6.0.

### Configuration

```json
{
    "type": "AvoidTernaryOperator",
    "props": {
        "severity": "ERROR"
    }
}
```

### Invalid

```java
var keycode = (event.keyCode != null) ? event.keyCode : event.which;
```

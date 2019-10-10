---
title: Block Breaking Conditional
toc: false
---

Detects block breaking conditionals. Useful for developers who find want to avoid conditionals to cross block boundaries. (available since 2.5.0)

### Configuration

```json
{
    "type": "BlockBreakingConditional",
    "props": {
        "severity": "INFO"
    }
}
```

### Invalid

```java
#if js
    if (true) {
#end
        trace(data);
#if js
    }
#end
```

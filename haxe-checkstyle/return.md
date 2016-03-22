---
title: Return
keywords: return
toc: false
---

Warns if Void is used for return or if return type is not specified when returning.

### Configuration

```json
{
    "type": "Return",
    "props": {
        "severity": "INFO",
        "allowEmptyReturn": true
    }
}
```

It has an option to allow empty returns which are mostly used to exit functions.

```java
function test(val:Int) {
    if (val == -1) return;
}
```
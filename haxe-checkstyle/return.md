---
title: Return
toc: false
---

Warns if Void is used for return or if return type is not specified when returning.

### Configuration

```json
{
    "type": "Return",
    "props": {
        "severity": "INFO",
        "allowEmptyReturn": true,
        "enforceReturnType": false
    }
}
```

It has an option to allow empty returns which are mostly used to exit functions.

`enforceReturnType` makes sure every function has a return type specification.

```java
function test(val:Int) {
    if (val == -1) return;
}
```
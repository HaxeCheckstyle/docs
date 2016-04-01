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

### Options

- `allowEmptyReturn` - Allows empty return which are mostly used to exit functions.

```java
function test(val:Int) {
    if (val == -1) return;
}
```

- `enforceReturnType` - Makes sure every function has a return type specification.

```java
function test(val:Int):Void {
    if (val == -1) {
        
    }
}
```

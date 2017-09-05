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
        "enforceReturnType": false,
        "enforceReturnTypeForAnonymous": false
    }
}
```

### Options

**`allowEmptyReturn`** - Allows empty return which is mostly used to exit functions.

```java
function test(val:Int) {
    if (val == -1) return;
}
```

**`enforceReturnType`** - Enforces return type for every function if set to `true`.

```java
function test(val:Int):Void {

}
```

```java
function test(val:Int):Float {
    return val * 0.5;
}
```

**`enforceReturnTypeForAnonymous`** - Enforces return type for anonymous functions if set to `true`.

---
title: Array Literal
keywords: array, literal
toc: false
---

Checks if the array is instantiated using [] which is shorter and cleaner, not with new.

### Configuration

```json
{
    "type": "ArrayLiteral",
    "props": {
        "severity": "ERROR"
    }
}
```
<br>

### Valid

```
var test:Array = [];
```
<br>

### Invalid

```
var test:Array = new Array();
```

`Bad array instantiation, use the array literal notation [] which is shorter and cleaner`
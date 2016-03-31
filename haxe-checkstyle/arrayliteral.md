---
title: Array Literal
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

### Valid

```java
var test:Array = [];
```

### Invalid

```java
var test:Array = new Array();
```

{{site.data.alerts.error}} Bad array instantiation, use the array literal notation [] which is shorter and cleaner {{site.data.alerts.end}}
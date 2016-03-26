---
title: Multiple Variable Declarations
keywords: multiple, variable, declarations
toc: false
---

Checks that each variable declaration is in its own statement and on its own line.

### Configuration

```json
{
    "type": "MultipleVariableDeclarations",
    "props": {
        "severity": "WARNING"
    }
}
```

### Invalid

```java
var d,e,f;

var d; var e;
```

{{site.data.alerts.error}} Each variable declaration must be in its own statement {{site.data.alerts.end}}

{{site.data.alerts.error}} Only one variable definition per line allowed {{site.data.alerts.end}}
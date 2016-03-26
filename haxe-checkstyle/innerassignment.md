---
title: Inner Assignment
keywords: coding, inner assignment
toc: false
---

Checks for assignments in subexpressions, such as in `if ((a=b) > 0) return;`.

### Configuration

```json
{
    "type": "InnerAssignment",
    "props": {
        "severity": "WARNING"
    }
}
```

### Valid

```java
if (a == b) a = c;
while ((a=b) > 0) b=c;
```

### Invalid

```java
if (a = b) a = c;
switch a=b {
    case 0: return true;
    default: return false;
}
```

{{site.data.alerts.error}} Inner assignment detected {{site.data.alerts.end}}
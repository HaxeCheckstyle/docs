---
title: Hexadecimal Literal
toc: false
---

Checks the letter case of hexadecimal literals.

### Configuration

```json
{
    "type": "HexadecimalLiteral",
    "props": {
        "severity": "INFO",
        "option": "upperCase"
    }
}
```

### Valid

```java
var clr = 0xFFFFFF;
```

### Invalid

```java
var clr = 0xffffff;
```

{{site.data.alerts.error}} Bad hexademical literal, use upperCase {{site.data.alerts.end}}
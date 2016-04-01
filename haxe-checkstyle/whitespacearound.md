---
title: Whitespace Around
toc: false
---

Checks for whitespace around a token.

### Configuration

```json
{
    "type": "WhitespaceAround",
    "props": {
        "severity": "WARNING",
        "tokens": [ "=", "+" ]
    }
}
```

### Valid

```java
var test = [];
test2 = 1 + 2;
```

### Invalid

```java
var test =[];
test2 = 1+ 2;
```

{{site.data.alerts.error}} No whitespace around {{site.data.alerts.end}}

{{site.data.alerts.error}} No whitespace around + {{site.data.alerts.end}}

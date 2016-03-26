---
title: Whitespace After
keywords: whitespace, after
toc: false
---

Checks for whitespace after a token.

### Configuration

```json
{
    "type": "WhitespaceAfter",
    "props": {
        "severity": "WARNING",
        "tokens": [ ",", ";" ]
    }
}
```

### Valid

```java
var test = [0, 1, 2,
        3, 5, 6];
```

### Invalid

```java
var test = [0,1,2,3,5,6];test.push(7);
```

{{site.data.alerts.error}} Warning No whitespace after , {{site.data.alerts.end}}

{{site.data.alerts.error}} Warning No whitespace after ; {{site.data.alerts.end}}
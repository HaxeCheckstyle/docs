---
title: EReg Literal
keywords: regex,literal
toc: false
---

Checks for usage of EReg literals (between ~/ and /) instead of new.

### Configuration

```json
{
    "type": "ERegLiteral",
    "props": {
        "severity": "ERROR"
    }
}
```

### Valid

```java
var reg:EReg = ~/test/i;
```

### Invalid

```java
var reg:EReg = new EReg("test", "i");
```

{{site.data.alerts.error}} Bad EReg instantiation, define expression between ~/ and / {{site.data.alerts.end}}
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

```
var reg:EReg = ~/test/i;
```

### Invalid

```
var reg:EReg = new EReg("test", "i");
```

`Bad EReg instantiation, define expression between ~/ and /`
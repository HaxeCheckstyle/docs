---
title: Constant Name
keywords: constant,name
toc: false
---

Checks that the constants (static / static inline with initialisation) conform to a format specified by the `format` property.

The default reg-ex as specified in the configuration below allows all upper case names for static constants.

### Configuration

```json
{
    "type": "ConstantName",
    "props": {
        "severity": "ERROR",
        "format": "^[A-Z][A-Z0-9]*(_[A-Z0-9]+)*$",
        "tokens": [
            "INLINE",
            "NOTINLINE"
        ]
    }
}
```

<br>

### Valid

```
static var COUNT:Int = 1;

static inline var COUNT:Int = 1;
```

### Invalid

```
static inline var Count:Int = 1;
```

`Invalid const signature: Count (name should be ~/^[A-Z][A-Z0-9]*(_[A-Z0-9]+)*$/)`
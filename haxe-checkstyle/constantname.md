---
title: Constant Name
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
            "INLINE"
        ]
    }
}
```

### Available Tokens

- `INLINE`
- `NOTINLINE`

### Valid

```java
static var COUNT:Int = 1;

static inline var COUNT:Int = 1;
```

### Invalid

```java
static inline var Count:Int = 1;
```

{{site.data.alerts.error}} Invalid const signature: Count (name should be ~/^[A-Z][A-Z0-9]*(_[A-Z0-9]+)*$/) {{site.data.alerts.end}}

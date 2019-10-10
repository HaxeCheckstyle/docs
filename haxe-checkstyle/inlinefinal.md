---
title: Inline Final
toc: false
---

Checks for places that use inline var instead of inline final (Haxe 4+, available since 2.5.0).

### Configuration

```json
{
    "type": "InlineFinal",
    "props": {
        "severity": "INFO"
    }
}
```

### Invalid

```java
class Main {
    inline var test:String = "0";
    static inline var test:String = "0";
}
```

### Valid

```java
class Main {
    inline final test:String = "0";
    static inline final test:String = "0";
}
```

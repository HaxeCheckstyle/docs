---
title: Final
toc: false
---

Checks for places that use var instead of final (Haxe 4+, available since 2.6.0, was InlineFinal in 2.5.0).

### Configuration

```json
{
    "type": "Final",
    "props": {
        "severity": "INFO"
    }
}
```

### Compliant

```java
class Main {
    inline final test:String = "0";
    static inline final test:String = "0";
    public static final test:String = "0";
    static var test:String = "0";
}
```

### Non-compliant

```java
class Main {
    inline var test:String = "0";
    static inline var test:String = "0";
    public static var test:String = "0";
}
```


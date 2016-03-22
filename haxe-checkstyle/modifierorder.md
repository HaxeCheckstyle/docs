---
title: Modifier Order
keywords: modifier, order
toc: false
---

Checks that the order of modifiers conforms to the standards.

### Configuration

```json
{
    "type": "ModifierOrder",
    "props": {
        "severity": "WARNING",
        "modifiers": [
            "MACRO",
            "OVERRIDE",
            "PUBLIC_PRIVATE",
            "STATIC",
            "INLINE",
            "DYNAMIC"
        ]
    }
}
```

### Valid

```java
public static inline var COUNT:Int = 1;
```

```java
override public function close() {}
```

### Invalid

```java
inline public static var COUNT:Int = 1;\
```

{{site.data.alerts.error}} Invalid access modifier order: COUNT (modifier: PUBLIC_PRIVATE) {{site.data.alerts.end}}

```java
public override function close() {}
```

{{site.data.alerts.error}} Invalid access modifier order: close (modifier: OVERRIDE) {{site.data.alerts.end}}
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

```
public static inline var COUNT:Int = 1;
```

```
override public function close() {}
```

### Invalid

```
inline public static var COUNT:Int = 1;\
```

`Invalid access modifier order: COUNT (modifier: PUBLIC_PRIVATE)`

```
public override function close() {}
```

`Invalid access modifier order: close (modifier: OVERRIDE)`
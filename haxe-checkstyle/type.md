---
title: Type
toc: false
---

Checks of type is specified or not for member variables.

### Configuration

```json
{
    "type": "Type",
    "props": {
        "severity": "INFO",
        "ignoreEnumAbstractValues": true
    }
}
```

### Options

**`ignoreEnumAbstractValues`** - Ignores variables in `@:enum abstract` / `enum abstract`

```java
@:enum abstract MyEnum(String) {
  var ConstantValue = "ConstantValue";
}
```

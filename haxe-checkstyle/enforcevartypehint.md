---
title: Enforce Var Type Hint
toc: false
---

Checks if all variables have type hint. Looks at all `var` and `final` variables, regardless if they are member or local variables. (available since 2.6.0)

### Configuration

```json
{
   "type": "EnforceVarTypeHint",
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

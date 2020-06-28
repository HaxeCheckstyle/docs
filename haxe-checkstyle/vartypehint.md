---
title: Var Type Hint
toc: false
---

Checks type hints of variables. Looks at all `var` and `final` variables, regardless if they are member or local variables. (available since 2.7.0)

### Configuration

```json
{
   "type": "VarTypeHint",
    "props": {
        "severity": "INFO",
        "ignoreEnumAbstractValues": true,
        "typeHintPolicy": "infer_new_or_const"
    }
}
```

### Options

**`ignoreEnumAbstractValues`** - Ignores variables in `@:enum abstract` / `enum abstract`

| `typeHintPolicy`       |                                                                                       |
| ---------------------- | ------------------------------------------------------------------------------------- |
| `enforce_all`          | var / final require a type hint                                                       |
| `infer_new_or_const`   | var / final require a type hint unless you assign a number, a string or new <Object>  |
| `infer_all`            | var / final only require a type hint if you do not assign anything                    |

---
title: Catch Parameter Name
keywords: naming, catch, parameter, name
toc: false
---

Checks that catch parameter names conform to a format specified by the `format` property.

### Configuration

```json
{
    "type": "CatchParameterName",
    "props": {
        "format": "^(e|t|ex|[a-z][a-z][a-zA-Z]+)$",
        "severity": "ERROR"
    }
}
```

The following `format` regex only allows `e`, `t` or `ex` as catch parameter names.

```
^(e|t|ex)$
```
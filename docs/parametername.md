---
title: Parameter Name
keywords: naming, parameter, name
toc: false
---

Checks that parameter names conform to a format specified by the `format` property.

### Configuration

```json
{
    "type": "ParameterName",
    "props": {
        "severity": "ERROR",
        "format": "^[a-z][a-zA-Z0-9]*$"
    }
}
```

The above regex allows `camelCase` names.
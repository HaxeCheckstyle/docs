---
title: Type Name
toc: false
---

Checks that type names conform to a format specified by the `format` property.

### Configuration

```json
{
    "type": "TypeName",
    "props": {
        "severity": "ERROR",
        "format": "^[A-Z]+[a-zA-Z0-9]*$",
        "tokens": [
            "CLASS",
            "ENUM",
            "TYPEDEF"
        ]
    }
},
{
    "type": "TypeName",
    "props": {
        "severity": "ERROR",
        "format": "^I[A-Z]+[a-zA-Z0-9]*$",
        "tokens": [
            "INTERFACE"
        ]
    }
}
```

The above configuration allows `PascalCase/UpperCamelCase` for `classes`, `enums`, `typedefs` and `PascalCase/UpperCamelCase` starting with `I` for `interfaces`.

### Available Tokens

- `CLASS`
- `INTERFACE`
- `ENUM`
- `ABSTRACT`
- `TYPEDEF`

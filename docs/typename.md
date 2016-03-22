---
title: Type Name
keywords: naming, type, name
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
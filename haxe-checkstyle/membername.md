---
title: Member Name
toc: false
---

Checks that instance variable names conform to a format specified by the `format` property.

### Configuration

```json
{
    "type": "MemberName",
    "props": {
        "severity": "ERROR",
        "format": "^[a-z][a-zA-Z0-9]*$",
        "tokens": [
            "PUBLIC",
            "PRIVATE",
            "TYPEDEF"
        ]
    }
}
```

### Available Tokens

- PUBLIC
- PRIVATE
- ENUM
- CLASS
- ABSTRACT
- TYPEDEF

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
            "CLASS"
        ]
    }
}
```

### Available Tokens

- `ENUM`
- `CLASS`
- `ABSTRACT`
- `TYPEDEF`
- `PUBLIC`
- `PRIVATE`

Note: 
- `PUBLIC` or `PRIVATE` only work on class and abstract types.
- If `tokens` contains neither `CLASS` nor `ABSTRACT`, `PUBLIC` and `PRIVATE` match both types.
- If `tokens` contains either `CLASS` or `ABSTRACT`, `PUBLIC` and `PRIVATE` match only members of that type.
- If `tokens` contains both `CLASS` and `ABSTRACT`, `PUBLIC` and `PRIVATE` match both types.
- If `tokens` contains neither `PUBLIC` nor `PRIVATE`, `CLASS` and `ABSTRACT` match public and private members.
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

Note: `PUBLIC` or `PRIVATE` tokens only work in combination with `CLASS` or `ABSTRACT` and vice versa. You have to specify a `CLASS` or `ABSTRACT` and at least one access modifier to activate a naming check on these types. `ENUM` and `TYPEDEF` don't have that requirement.

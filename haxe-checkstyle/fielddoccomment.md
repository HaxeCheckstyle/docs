---
title: Field Doc Comment
toc: false
---

Checks code documentation on fields

### Configuration

```json
{
  "type": "FieldDocComment"}
  "props": {
    "requireParams": true,
    "fieldType": "BOTH",
    "requireReturn": true,
    "ignoreOverride": true,
    "tokens": [
      "ABSTRACT_DEF",
      "CLASS_DEF",
      "ENUM_DEF",
      "INTERFACE_DEF",
      "TYPEDEF_DEF"
    ],
    "modifier": "PUBLIC",
    "excludeNames": [
      "new",
      "toString"
    ]
  }
}
```

Only checks fields matching types listed in `tokens`:

| Token Name            |                 |
| --------------------- | ----------------|
| `ABSTRACT_DEF`        | abstract types  |
| `CLASS_DEF`           | class types     |
| `ENUM_DEF`            | enum types      |
| `INTERFACE_DEF`       | interface types |
| `TYPEDEF_DEF`         | typdef types    |

Limit types of fields to check with `fieldType`:

| fieldType     |                         |
| --------------| ------------------------|
| `VARS`        | only var fields         |
| `FUNCTIONS`   | only functions          |
| `BOTH`        | both vars and functions |

Limit modifiers of fields to check with `modifier`:

| modifier   |                            |
| -----------| ---------------------------|
| `PUBLIC`   | only public fields         |
| `PRIVATE`  | only private fields        |
| `BOTH`     | public and private fields  |

Use `requireParams` and `requireReturn` to require `@param param1 ` and `@return ` for every param and return values.
`ignoreOverride` ignores functions wqith override.

`excludeNames` lists a all names that should not produce a checkstyle violation. Defaults to `["new", "toString"]`.

---
title: Type Doc Comment
toc: false
---

Checks code documentation on type level

### Configuration

```json
{
  "type": "TypeDocComment",
  "props": {
    "tokens": [
      "ABSTRACT_DEF",
      "CLASS_DEF",
      "ENUM_DEF",
      "INTERFACE_DEF",
      "TYPEDEF_DEF"
    ]
  }
}
```

Every type from `tokens` must have a documenting comment on type definition level.

| Token Name            | Description     |
| --------------------- | ----------------|
| `ABSTRACT_DEF`        | abstract types  |
| `CLASS_DEF`           | class types     |
| `ENUM_DEF`            | enum types      |
| `INTERFACE_DEF`       | interface types |
| `TYPEDEF_DEF`         | typdef types    |

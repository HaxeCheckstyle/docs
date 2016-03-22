---
title: Empty Block
keywords: emptyblock
toc: false
---

Checks for empty blocks. The policy to verify is specified using the property `option`.

### Configuration

```json
{
    "type": "EmptyBlock",
    "props": {
        "tokens": [
            "CLASS_DEF",
            "ENUM_DEF",
            "ABSTRACT_DEF",
            "TYPEDEF_DEF",
            "INTERFACE_DEF",
            "OBJECT_DECL",
            "FUNCTION",
            "FOR",
            "IF",
            "WHILE",
            "SWITCH",
            "TRY",
            "CATCH"
        ],
        "option": "empty",
        "severity": "IGNORE"
    }
}
```

| Option    | Description                                                                      |
| --------- | -------------------------------------------------------------------------------- |
| `empty`   | allows empty blocks but enforces `{}` notation                                   |
| `text`    | empty blocks must contain something apart from whitespace (comment or statement) |
| `stmt`    | all blocks must contain at least one statement                                   |
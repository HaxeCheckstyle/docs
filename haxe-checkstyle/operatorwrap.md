---
title: Operator Wrap
toc: false
---

Checks line wrapping with operators.

### Configuration

```json
{
    "type": "OperatorWrap",
    "props": {
        "severity": "INFO",
        "option": "eol",
        "tokens": [
            "=", "+", "-", "*", "/", "%", ">", "<",
            ">=", "<=", "==", "!=", "&", "|", "^",
            "&&", "||", "<<", ">>", ">>>", "+=",
            "-=", "*=", "/=", "%=", "<<=", ">>=",
            ">>>=", "|=", "&=", "^=", "...", "=>",
            "!", "++", "--"
        ]
    }
}
```

Available options are end of line (`eol`) and new line (`nl`)

### Valid

option set to `eol`

```java
var test = test1 +
    test2;
```

option set to `nl`

```java
var test = test1
    + test2;
```
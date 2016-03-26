---
title: Separator Wrap
keywords: whitespace, separator, wrap
toc: false
---

Checks line wrapping with separators.

### Configuration

```json
{
    "type": "SeparatorWrap",
    "props": {
        "severity": "INFO",
        "option": "eol",
        "tokens": [
            ".", ","
        ]
    }
}
```

Available options are end of line (`eol`) and new line (`nl`)

### Valid

option set to `eol`

```
    val = test.
        text();
```

option set to `nl`

```
    val = test
        .text();
```
---
title: Listener Name
toc: false
---

Checks the naming conventions of event listener functions specified using `listeners` property.

Useful if you want to have a different naming convention for listener functions like for example prefixing with `on`.

Note that this check assumes that the second parameter is the listener function which may not be true in all cases.

### Configuration

```json
{
    "type": "ListenerName",
    "props": {
        "severity": "ERROR",
        "format": "^_?on.*",
        "listeners": [
            "addEventListener",
            "addListener",
            "on",
            "once"
        ]
    }
}
```
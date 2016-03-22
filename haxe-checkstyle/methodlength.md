---
title: Method Length
keywords: method, length
toc: false
---

Checks for long methods. If a method becomes very long it is hard to understand. Therefore long methods should usually be refactored into several individual methods that focus on a specific task.


### Configuration

```json
{
    "type": "MethodLength",
    "props": {
        "severity": "ERROR",
        "max": 50
    }
}
```
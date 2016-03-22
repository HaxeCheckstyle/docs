---
title: Method Count
keywords: method, count
toc: false
---

Checks the number of methods declared in each type. This includes the number of each scope (`private` and `public`) as well as an overall total.

### Configuration

```json
{
    "type": "MethodCount",
    "props": {
        "maxPrivate": 100,
		"maxPublic": 100,
		"maxTotal": 100,
        "severity": "ERROR"
    }
}
```
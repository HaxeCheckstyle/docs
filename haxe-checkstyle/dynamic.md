---
title: Dynamic
keywords: dynamic
toc: false
---

Checks for use of Dynamic type anywhere in the code.

### Configuration

```json
{
    "type": "Dynamic",
    "props": {
        "severity": "INFO"
    }
}
```

The following is a sample `Dynamic` usage.

```
var count:Dynamic;

function calc(val1:Dynamic, val2:Dynamic):Dynamic {
	count = 25;
	return count;
}
```

`Dynamic type used: count`


`Dynamic type used: val1`


`Dynamic type used: val2`


`Dynamic type used: calc`

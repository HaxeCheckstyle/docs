---
title: Return Count
keywords: return, count
toc: false
---

Restricts the number of return statements in methods (2 by default). Ignores methods that matches `ignoreFormat` regex property.

### Configuration

```json
{
	"type": "ReturnCount",
	"props": {
        "ignoreFormat": "^$",
		"max": 2,
		"severity": "WARNING"
	}
}
```
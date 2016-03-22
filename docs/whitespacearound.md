---
title: Whitespace Around
keywords: whitespace, around
toc: false
---

Checks for whitespace around a token.

### Configuration

```json
{
	"type": "WhitespaceAround",
	"props": {
		"severity": "WARNING",
		"tokens": [ "=", "+" ]
	}
}
```

### Valid

```
	var test = [];
	test2 = 1 + 2;
```

### Invalid

```
	var test =[];
	test2 = 1+ 2;
```

`Warning No whitespace around`


`Warning No whitespace around +`
---
title: Whitespace After
keywords: whitespace, after
toc: false
---

Checks for whitespace after a token.

### Configuration

```json
{
	"type": "WhitespaceAfter",
	"props": {
		"severity": "WARNING",
		"tokens": [ ",", ";" ]
	}
}
```

### Valid

```
	var test = [0, 1, 2,
		3, 5, 6];
```

### Invalid

```
	var test = [0,1,2,3,5,6];test.push(7);
```

`Warning No whitespace after ,`


`Warning No whitespace after ;`
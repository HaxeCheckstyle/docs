---
title: Operator Wrap
keywords: whitespace, operator, wrap
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

```
var test = test1 +
	test2;
```

option set to `nl`

```
var test = test1
	+ test2;
```
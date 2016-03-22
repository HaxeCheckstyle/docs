---
title: Multiple Variable Declarations
keywords: multiple, variable, declarations
toc: false
---

Checks that each variable declaration is in its own statement and on its own line.

### Configuration

```json
{
	"type": "MultipleVariableDeclarations",
	"props": {
		"severity": "WARNING"
	}
}
```

### Invalid

```
var d,e,f;

var d; var e;
```

`Each variable declaration must be in its own statement`

`Only one variable definition per line allowed`
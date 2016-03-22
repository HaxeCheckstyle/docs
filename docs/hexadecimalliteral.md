---
title: Hexadecimal Literal
keywords: hexadecimal,literal
toc: false
---

Checks the letter case of hexadecimal literals.

### Configuration

```json
{
	"type": "HexadecimalLiteral",
	"props": {
		"severity": "INFO",
		"option": "upperCase"
	}
}
```

### Valid

```haxe
var clr = 0xFFFFFF;
```

### Invalid

```haxe
var clr = 0xffffff;
```

`Bad hexademical literal, use upperCase`
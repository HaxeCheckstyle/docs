---
title: Operator Whitespace
keywords: whitespace, operator
toc: false
---

Checks that whitespace is present or absent around a operators.

### Configuration

```json
{
	"type": "OperatorWhitespace",
	"props": {
		"severity": "WARNING",
		"assignOpPolicy": "around",      // =, +=, -=, *=, /=, <<=, >>=, >>>=, &=, |=, ^=
		"unaryOpPolicy": "none",         // ++, --, !
		"arithmeticOpPolicy": "around",  // +, -, *, /, %
		"compareOpPolicy": "around",     // ==, !=, <, <=, >, >=
		"bitwiseOpPolicy": "around",     // ~, &, |, ^, <<, >>, >>>
		"boolOpPolicy": "around",        // &&, ||
		"intervalOpPolicy": "none"       // ...
	}
}
```

Available policy values are:

| Option     | Description |
| --------- | ----------- |
| `around`  | enforce whitespace before and after operator |
| `before`  | enforce whitespace before and no whitespace after operator |
| `after`   | enforce no whitespace before and whitespace after operator |
| `none`    | enforce no whitespace before and after operator |
| `ignore`  | skip checks |

<br>

For unary operators only whitespace between operator and operand is checked, available policy values are:

| Option     | Description |
| --------- | ----------- |
| `inner`   | enforce whitespace between unary operator and operand |
| `none`    | enforce no whitespace between unary operator and operand |
| `ignore`  | skip checks |
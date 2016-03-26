---
title: Right Curly
keywords: rightcurly
toc: false
---

Checks for placement of right curly braces.

### Configuration

```json
{
	"type": "RightCurly",
	"props": {
		"severity": "WARNING",
		"option": "aloneorsingle",
		"tokens": [
			"CLASS_DEF",
			"ENUM_DEF",
			"ABSTRACT_DEF",
			"TYPEDEF_DEF",
			"INTERFACE_DEF",
			"OBJECT_DECL",
			"FUNCTION",
			"FOR",
			"IF",
			"WHILE",
			"SWITCH",
			"TRY",
			"CATCH",
			"REIFICATION",
			"ARRAY_COMPREHENSION"
		]
	}
}
```

| Option   | Description |
| ---------------- | ------------|
| `alone`          | alone on a new line |
| `same`           | right curly must be alone on a new line, except for `} else` and `} catch` |
| `aloneorsingle`  | right curly can occur on same line as left curly or must be alone on a new line |

| Token Name            | Description          | Example                                 |
| --------------------- | -------------------- | --------------------------------------- |
| `CLASS_DEF`           | class definition     | class Test {}                           |
| `ENUM_DEF`            | enum definition      | enum Test {}                            |
| `ABSTRACT_DEF`        | abstract definition  | abstract Test {}                        |
| `TYPEDEF_DEF`         | typdef definition    | typedef Test = {}                       |
| `INTERFACE_DEF`       | interface definition | interface Test {}                       |
| `OBJECT_DECL`         | object declaration   | { x: 0, y: 0, z: 0}                     |
| `FUNCTION`            | function body        | function test () {}                     |
| `FOR`                 | for body             | for (i in 0..10) {}                     |
| `IF`                  | if / else body       | if (test) {} else {}                    |
| `WHILE`               | while body           | while (test) {}                         |
| `SWITCH`              | switch / case body   | switch (test) { case: {} default: {} }  |
| `TRY`                 | try body             | try {}                                  |
| `CATCH`               | catch body           | catch (e:Dynamic) {}                    |
| `REIFICATION`         | macro reification    | $i{}                                    |
| `ARRAY_COMPREHENSION` | array comprehension  | [for (i in 0...10) {i * 2}]             |
---
title: Unused Import
keywords: import
toc: false
---

Checks for unused or duplicate imports.

### Configuration

```json
{
	"type": "UnusedImports",
	"props": {
		"severity": "WARNING",
		"ignoreModules": [
			"haxe.macro.Type"
		],
		"moduleTypeMap": {
			"haxe.macro.Expr": [
				"ExprDef",
				"ComplexType"
			]
		}
	}
}
```

**Limitation:** Unused import check has no information about imported modules and the types contained within, other than the name used in import specification.

**Note:** UnusedImport skips all files named `import.hx`.

<br>

### Valid

```haxe
package com.project;

import haxe.macro.Expr;
import com.test.Type;
import com.project.sub.Type2;

class Main extends Type {
	var type:Type2;
	var exprDef:ExprDef;
}
```

### Invalid

```haxe
package com.project;

import com.test.Type;
import com.project.sub.Type2;
import com.project.sub.Type2;
import com.project.SomeType;

import String;

class Main extends Type2 implements SomeType {
}
```

`Unused import com.test.Type detected`


`Duplicate import com.project.sub.Type2 detected`


`Unneccessary toplevel import String detected`


`Detected import com.project.SomeType from same package com.project`
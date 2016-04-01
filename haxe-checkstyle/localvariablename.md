---
title: Local Variable Name
toc: false
---

Checks that the local variable names conform to a format specified by the `format` property.

{{site.data.alerts.info}} Local variables are the ones that are visible/accessible only within the block of code in which it appears. {{site.data.alerts.end}}

### Configuration

```json
{
    "type": "LocalVariableName",
    "props": {
        "severity": "ERROR",
        "format": "^[a-z][a-zA-Z0-9]*$"
    }
}
```

The above regex allows `camelCase` names.

### Invalid

```java
class Test {
	public function test() {
		var Count:Int = 1;
	}
}
```

{{site.data.alerts.error}} Invalid local var signature: "Count" (name should be "~/$^[a-z][a-zA-Z0-9]*$/") {{site.data.alerts.end}}

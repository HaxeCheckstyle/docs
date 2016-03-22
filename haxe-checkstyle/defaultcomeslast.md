---
title: Default Comes Last
keywords: switch, default
toc: false
---

Check that the `default` is after all the cases in a `switch` statement. Haxe allows `default` anywhere within the `switch` statement. But it is more readable if it comes after the last `case`.

### Configuration

```json
{
	"type": "DefaultComesLast",
	"props": {
		"severity": "WARNING"
	}
}
```

### Valid

```java
switch(a) {
	case 1:
    case 4:
    default: trace("test");
}
```

### Invalid

```java
switch(a) {
	case 1:
	default: trace("test");
    case 4:
}
```

{{site.data.alerts.error}} Default should be last label in the switch {{site.data.alerts.end}}
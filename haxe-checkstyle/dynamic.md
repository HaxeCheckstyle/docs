---
title: Dynamic
keywords: dynamic
toc: false
---

Checks for use of Dynamic type anywhere in the code.

### Configuration

```json
{
    "type": "Dynamic",
    "props": {
        "severity": "INFO"
    }
}
```

The following is a sample `Dynamic` usage.

```java
var count:Dynamic;

function calc(val1:Dynamic, val2:Dynamic):Dynamic {
    count = 25;
    return count;
}
```

{{site.data.alerts.error}} Dynamic type used: count {{site.data.alerts.end}}

{{site.data.alerts.error}} Dynamic type used: val1 {{site.data.alerts.end}}

{{site.data.alerts.error}} Dynamic type used: val2 {{site.data.alerts.end}}

{{site.data.alerts.error}} Dynamic type used: calc {{site.data.alerts.end}}
---
title: Interface
toc: false
---

Checks and enforces interface style. Either to allow properties and methods or just methods. Has an option to `allowMarkerInterfaces`.

### Configuration

```json
{
    "type": "Interface",
    "props": {
        "allowProperties": false,
        "allowMarkerInterfaces": true,
        "severity": "INFO"
    }
}
```

### Valid

```java
interface IComponentController {
    function init():Void;
}
```

### Invalid (When allowProperties is set to false)

```java
interface IComponentController {
	var a:Int = 1;
    function init():Void;
}
```

{{site.data.alerts.error}} Properties are not allowed in interfaces {{site.data.alerts.end}}

### Invalid (When allowMarkerInterfaces is set to false)

```java
interface IComponentController {}
```

{{site.data.alerts.error}} Marker interfaces are not allowed {{site.data.alerts.end}}

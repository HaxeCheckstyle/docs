---
title: Anonymous
keywords: anonymous
toc: false
---

Check to find any anonymous type structures used.

### Configuration

```json
{
    "type": "Anonymous",
    "props": {
        "severity": "ERROR"
    }
}
```

### Valid

```java
var data:Data;
```


```java
typedef Data = {
    var name:String;
    var value:Int;
}
```

### Invalid

```java
var data:{name:String, value:Int};
```

{{site.data.alerts.error}} Anonymous structure found, it is advised to use a typedef instead "data" {{site.data.alerts.end}}
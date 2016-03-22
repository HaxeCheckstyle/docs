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

<br>

### Valid

```
var data:Data;
```


```
typedef Data = {
    var name:String;
    var value:Int;
}
```

<br>

### Invalid

```
var data:{name:String, value:Int};
```

`Anonymous structure found, it is advised to use a typedef instead "data"`
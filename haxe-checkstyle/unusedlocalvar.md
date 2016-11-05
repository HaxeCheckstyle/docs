---
title: Unused Local Var
toc: false
---

Checks for unused local variables.

### Configuration

```json
{
    "type": "UnusedLocalVar"
}
```

### No violation

```java
class Main {
    function test() {
        var a;
        var b;
        var c;
        var d;

        a++;
        call(b);
        call(function() {
            c++;
        });
        trace ('$d');
    }
}
```

### Violations

```java
class Main {
    function test() {
        var name;
    }
    function test2() {
        call(function() {
            var name;
        });
    }
}
```

{{site.data.alerts.error}} Unused local variable name {{site.data.alerts.end}}
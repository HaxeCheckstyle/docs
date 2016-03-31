---
title: Unnecessary Constructor
toc: false
---

Checks for unnecessary constructor in classes that contain only static methods or fields.

{{site.data.alerts.info}} Instantiating static classes does not make sense.
So this check helps to find unnecessary constructors in static/utility classes. {{site.data.alerts.end}}

### Configuration

```json
{
    "type": "UnnecessaryConstructor",
    "props": {
        "severity": "ERROR"
    }
}
```
---
title: Interface
keywords: interface
toc: false
---

Checks for unnecessary constructor in classes that contain only static methods or fields.

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
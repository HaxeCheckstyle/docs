---
title: Redundant Access Meta
toc: false
---

Checks for redundant `@:access` metadata (available since 2.4.2)

### Configuration

```json
{
    "type": "RedundantAccessMeta",
    "props": {
        "prohibitMeta": false,
        "severity": "INFO"
    }
}
```

`prohibitMeta` set to `true` generates a checkstyle message for every use of `@:access`. When set to `false` it will compare field level to type level `@:access` metas.

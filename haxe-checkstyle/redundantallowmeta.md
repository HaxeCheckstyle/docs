---
title: Redundant Allow Meta
toc: false
---

Checks for redundant `@:allow` metadata (available since 2.4.2)

### Configuration

```json
{
    "type": "RedundantAllowMeta",
    "props": {
        "prohibitMeta": false,
        "severity": "INFO"
    }
}
```

`prohibitMeta` set to `true` generates a checkstyle message for every use of `@:allow`. When set to `false` it will look for `@:allow` on public fields and compare field level to type level `@:allow` metas.

---
title: Spacing
toc: false
---

Spacing check on if, for, while, switch, try statements and around operators.

### Configuration

```json
{
    "type": "Spacing",
    "props": {
        "severity": "INFO",
        "spaceIfCondition": "should",
        "spaceForLoop": "should",
        "spaceWhileLoop": "should",
        "spaceSwitchCase": "should",
        "spaceCatch": "should",
        "spaceAroundBinop": true,
        "noSpaceAroundUnop": true,
        "ignoreRangeOperator": true
    }
}
```

Valid values for `spaceIfCondition`, `spaceForLoop`, `spaceWhileLoop`, `spaceSwitchCase` and `spaceCatch` are:

- `should` - space should be there between statement and condition
- `shouldNot` - space should not be there between statement and condition
- `any` - ignores the space check

### Invalid

`spaceIfCondition` set to `should`

```java
if(true) {}
```

{{site.data.alerts.error}} No space between "if" and "(" {{site.data.alerts.end}}


`noSpaceAroundUnop` set to `true`

```java
var a = a ++;
```

{{site.data.alerts.error}} Space around "++" {{site.data.alerts.end}}

---
title: Variable Initialisation
toc: false
---

Checks for instance variables that are initialised at class level.

### Configuration

```json
{
    "type": "VariableInitialisation",
    "props": {
        "severity": "ERROR",
        "allowFinal": false
    }
}
```

### Options

**`allowFinal`** - when allowFinal is true then VariableInitialisation won't complain about initialisation at class level for final fields (available since 2.6.1)
---
title: Nested Control Flow
toc: false
---

Checks for maximium nesting depth of control flow expressions (`if`, `for`, `while`, `do/while`, `switch` and `try`). (available since 2.6.0)

### Configuration

```json
{
    "type": "NestedControlFlow",
    "props": {
        "severity": "INFO",
        "max": 3
    }
}
```

### Options

**`max`** - maximum number of nested control flow expressions before a warning is raised

### Compliant

```java
while (true) {                               // level 1
  for (outerParam in params)  {              // level 2
    for (innerParam in params) {             // level 3 = compliant, not exceeding limit of 3
    }
  }
}
```

### Noncompliant

```java
while (true) {                               // level 1
  for (outerParam in params) {               // level 2
    for (innerParam in params) {             // level 3
      if (innerParam == null) {              // level 4 = exceeding `max` value of 3
      }
    }
  }
}
```

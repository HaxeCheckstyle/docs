---
title: Simplify Boolean Return
toc: false
---

Checks for over-complicated boolean return statements.

### Configuration

```json
{
    "type": "SimplifyBooleanReturn",
    "props": {
        "severity": "ERROR"
    }
}
```

For example the following code

```java
if (isValid()) {
    return false;
}
else {
    return true;
}
```
        
could be written as

```java
return !isValid();
```
        
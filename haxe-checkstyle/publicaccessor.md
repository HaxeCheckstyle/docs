---
title: Public Accessor
toc: false
---

Checks for public accessors.

### Configuration

```json
{
    "type": "PublicAccessor",
    "props": {
        "severity": "INFO"
    }
}
```

### Invalid

```java
class Main {
    public function get_test() {}
}
```

### Valid

```java
class Main {
    function get_test() {}
    private function get_test() {}
}
```

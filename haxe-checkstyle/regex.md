---
title: RegEx Reference
toc: false
---

### `camelCase`

```
^[a-z][a-zA-Z0-9]*$
```

### `PascalCase` or `UpperCamelCase`

```
^[A-Z]+[a-zA-Z0-9]*$
```

### `PascalCase` or `UpperCamelCase` starting with letter `I`

```
^I[A-Z]+[a-zA-Z0-9]*$
```

### `UpperCase` separated by `_`

```
^[A-Z][A-Z0-9]*(_[A-Z0-9]+)*$
```
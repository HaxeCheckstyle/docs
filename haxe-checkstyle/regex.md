---
title: RegEx Reference
toc: false
---

The following are the recommended links to create and test and regular expressions:

- [regexr.com](http://regexr.com/)
- [regex101.com](https://regex101.com/)

## Samples

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
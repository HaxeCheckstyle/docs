---
title: RegEx Reference
keywords: regex
toc: false
---

The following are the recommended links to create and test and regular expressions:

- [regexr.com](http://regexr.com/)
- [regex101.com](https://regex101.com/)

### Samples

| Expression                      | Description                                               |
| ------------------------------- | --------------------------------------------------------- |
| `^I[A-Z]+[a-zA-Z0-9]*$`         | `PascalCase` or `UpperCamelCase` starting with letter `I` |
| `^[A-Z]+[a-zA-Z0-9]*$`          | `PascalCase` or `UpperCamelCase`                          |
| `^[a-z][a-zA-Z0-9]*$`           | `camelCase`                                               |
| `^[A-Z][A-Z0-9]*(_[A-Z0-9]+)*$` | `UpperCase` separated by `_`                              |
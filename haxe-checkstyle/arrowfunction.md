---
title: Arrow Function
toc: false
---

Checks for use of curlies, nested (non-arrow) functions or returns in arrow functions. (available since 2.6.0)

### Configuration

```json
{
    "type": "ArrowFunction",
    "props": {
        "severity": "INFO",
        "allowCurlyBody": false,
        "allowFunction": false,
        "allowReturn": false,
        "allowSingleArgParens": false
    }
}
```

**`allowCurlyBody`** - allow using curly block as arrow function body (`{...}`)

**`allowFunction`** - allow using `function` inside arrow function bodies

**`allowReturn`** - allow using `return` inside arrow function bodies

**`allowSingleArgParens`** - allow using parenthesis around single argument arrow function (`(arg) -> arg * 2`)

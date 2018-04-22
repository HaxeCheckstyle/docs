---
title: Indentation
toc: false
---

Checks correct indentation.

Indentation increases everytime a block opens, affecting the line after left curly (`{`). 
It also increases after `if`, `else`, `for`, (inside) `do-while`, `while`, `case` and `default`. 
Square brackets (`[`) also increase indentation unless directly followed by left curly (`[{`).
Multiline strings may break indentation and there is handling for line-wrapped indentation.

Available since 2.2.1

### Configuration

```json
{
    "type": "Indentation",
    "props": {
        "severity": "INFO",
        "character": "tab",
        "ignoreConditionals": false,
        "ignoreComments": true,
        "wrapPolicy", "larger"
    }
}
```

`character` can either be `tab` or a number of spaces e.g. `  ` or `    `, etc.
Setting `ignoreConditionals` to `true` allows lines starting with `#if/#else/#elseif/#end` to break indentation. Setting it to `false` means conditionals must have correct indentation.
Setting `ignoreComments` to `true` ignores lines starting with a comment, if you want your comments to use correct indentation then set `ignoreComments` to `false`.

| `wrapPolicy` |                                                                               |
| ------------ | ----------------------------------------------------------------------------- |
| `none`       | wrapped statements must have the same indentation as parent                   |
| `exact`      | wrapped statemenmts must have a +1 indentation in relation to parent          |
| `larger`     | wrapped statements must have a +1 or larger indentation in relation to parent |

{{site.data.alerts.error}} Indentation mismatch: expected: 2, actual: 3 {{site.data.alerts.end}}


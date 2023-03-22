---
title: Indentation
toc: false
---

Checks correct indentation. (available since 2.2.1)

Indentation increases everytime a block opens, affecting the line after left curly (`{`). 
It also increases after `if`, `else`, `for`, (inside) `do-while`, `while`, `case` and `default`. 
Square brackets (`[`) also increase indentation unless directly followed by left curly (`[{`).
Multiline strings may break indentation and there is handling for line-wrapped indentation.


### Configuration

```json
{
    "type": "Indentation",
    "props": {
        "severity": "INFO",
        "character": "tab",
        "ignoreConditionals": false,
        "ignoreComments": true,
        "conditionalPolicy": "aligned",
        "wrapPolicy": "larger"
    }
}
```

`character` can either be `tab` or a number of spaces e.g. "  ", etc.
Setting `ignoreConditionals` to `true` allows lines starting with `#if/#else/#elseif/#end/#error` to break indentation. Setting it to `false` means conditionals must have correct indentation.
Setting `ignoreComments` to `true` ignores lines starting with a comment, if you want your comments to use correct indentation then set `ignoreComments` to `false`.

| conditionalPolicy   | (available since 2.3.0)                                                                               |
| ------------------- | ----------------------------------------------------------------------------------------------------- |
| `ignore`            | ignores conditioonals, same as `ignoreConditionals`                                                   |
| `fixed_zero`        | contitionals have to start at the beginning of a line, only where conditional is the first statement  |
| `aligned`           | contitionals share indentation of surrounding code                                                    |
| `aligned_increase`  | like `aligned` but increases indentation of enclosed code                                             |

| wrapPolicy   |                                                                               |
| ------------ | ----------------------------------------------------------------------------- |
| `none`       | wrapped statements must have the same indentation as parent                   |
| `exact`      | wrapped statemenmts must have a +1 indentation in relation to parent          |
| `larger`     | wrapped statements must have a +1 or larger indentation in relation to parent |

{{site.data.alerts.error}} Indentation mismatch: expected: "\t"[1], actual: no indentation {{site.data.alerts.end}}


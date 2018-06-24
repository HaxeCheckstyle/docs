---
title: Doc Comment Style
toc: false
---

Checks code documentation style (/**…**/ vs /*…*/)

### Configuration

```json
{
  "type": "DocCommentStyle",
  "props": {
    "lineStyle": "none",
    "startStyle": "twostars"
  }
}
```

`startStyle` defines how many stars should occur at the start and end of documenting comment. `onestar` equals `/* … */`, `twostars` stands for `/** … **/`
Start and end must be symmetric.
`lineStyle` defines how many stars should occur at the start of every line (apart from start and end lines).

| style          |                                                    |
| -------------- | -------------------------------------------------- |
| `ignore`       | ignores number of stars                            |
| `none`         | no (additional) stars                              |
| `onestar`      | exactly one star allowed                           |
| `twostars`     | exactly two stars allowed                          |

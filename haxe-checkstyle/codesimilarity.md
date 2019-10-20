---
title: Code Similarity
toc: false
---

Checks for identical or similar code. Currently looks for similar or identical functions, `if`, `for`, `switch`, `while`, `do/while`, `try` and block expressions. (available since 2.6.0)

### Configuration

```json
{
   "type": "CodeSimilarity",
    "props": {
        "severity": "INFO",
        "severityIdentical": "WARNING",
        "thresholdIdentical": 8,
        "thresholdSimilar": 12
    }
}
```

### Options

**`severityIdentical`** - Severity level for identical code blocks

**`thresholdIdentical`** - number of lines where identical code is tolerated

**`thresholdSimilar`** - number of lines where similar code is tolerated

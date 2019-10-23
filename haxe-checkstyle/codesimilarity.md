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

**`severityIdentical`** - Severity level for identical code blocks (`severity` is used for reporting similar code blocks)

**`thresholdIdentical`** - number of lines where identical code is tolerated

**`thresholdSimilar`** - number of lines where similar code is tolerated

### Similar and identical code

`CodeSimilarity` determines similar and identical code parts by generating and comparing hashes for each eligible code section.

Code is considered identical if names, keywords, operations, values and overall structure are identical in two or more places.

Code is considered similar if keywords and overall structure are identical, names and values may vary, and operators need to fall into identical categories. 

If e.g. code A has `+` , code B has `-` and code C has `&&` then A and B show up as similar, C will not. For operator categories see [Haxe manual](https://haxe.org/manual/expression-operators-binops.html).

Comments and whitespace have no influence to detecting similar or identical code fragments.

`CodeSimilarity` will only look at `function`, `if`, `for`, `switch`, `while`, `do/while`, `try` and `{` as starting points for similar or identical code.
Current version of check will not look at individiual lines outside or surrounding keywords / tokens of that list. So there might be code fragments that `CodeSimilarity` will not mark as similar or identical, even though they might preceed or follow a section of code that was found to be similar.

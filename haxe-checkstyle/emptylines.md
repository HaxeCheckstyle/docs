---
title: Empty Lines
keywords: lines
toc: false
---

Checks for consecutive empty lines (default is 1). Also have options to check empty line separators after package, single-line and multi-line comments and class/interface/abstract declarations.

### Configuration

```json
{
    "type": "EmptyLines",
    "props": {
    	"requireEmptyLineAfterInterface": true,
    	"requireEmptyLineAfterAbstract": true,
    	"allowEmptyLineAfterSingleLineComment": true,
    	"requireEmptyLineAfterClass": true,
    	"allowEmptyLineAfterMultiLineComment": true,
    	"max": 1,
    	"severity": "INFO"
    }
}
```
---
title: Cyclomatic Complexity
keywords: metrics,cyclomatic,complexity
toc: false
---

Checks the complexity of methods using McCabe simplified [cyclomatic complexity](https://en.wikipedia.org/wiki/Cyclomatic_complexity) check. Complexity levels can be customised using `thresholds` property.

### Configuration

```json
{
    "type": "CyclomaticComplexity",
    "props": {
        "thresholds": [
            {
                "severity": "INFO",
                "complexity": 6
            },
            {
                "severity": "WARNING",
                "complexity": 11
            },
            {
                "severity": "ERROR",
                "complexity": 21
            }
        ]
    }
}
```

In general, for function level complexity:

|  Score | Complexity        |
| --------- | ---------------- |
| `< 10`   | Easy to maintain  |
| `11 - 20`    | Harder to maintain |
| `> 20`    | Candidates for re-factoring/redesign  |


The following function has a complexity score of **`8`**.

```java
public function test() {
	var a = 1;
	if (a == 1) {
		for (i in 0 ... 10) {
			for (j in 0 ... 100) {
				if (i == 5) {
					if (j == 50) {
						trace(j);
					}
				}
			}
		}
	}

	switch (a) {
		case 1:
			trace(1);
		case 2:
			trace(2);
		default:
			trace("default");
	}
}
```

{{site.data.alerts.error}} Function "test" is too complex (score: 8) {{site.data.alerts.end}}
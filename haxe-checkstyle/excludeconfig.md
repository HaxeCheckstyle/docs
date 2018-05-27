---
title: Excluding code from checkstyle
toc: false
---

### Suppressing and excluding files and parts of file

Sometimes checkstyle complains about things, that you can't or won't fix. With excludes and suppression you can then tell checkstyle to ignore those parts of your code.
Checkstyle supports inline suppresstion through a `@SuppressWarnings` meta annotation above the offending part. It also supports exclusions though your checkstyle configuration file or a dedicated checkstyle exclude file. 

#### Exclude packages/classes with a configuration file

You can define excludes either inside your `checkstyle.json` configuration file, or you can put them into a separate `checkstyle-exclude.json` file (use `-c`and `-e` command line options to change default filenames). 
Checkstyle will skip files that match an entry under the `"all"` key. The Dynamic check will not run on any file matching an entry in the `"Dynamic"` section.

New since checkstyle 2.4.0: each entry can have an additional range specification. 
| Valid ranges are:                     |
| ------------------------------------- |
| `:<lineNumber>`                       |
| `:<lineNumberStart>-<lineNumberEnd>`  |
| `:<identifier>`                       |
Where `lineNumber`, `lineNumberStart` and `lineNumberEnd` must be positive integers, should specify valid line numbers of affected files. Linenumbers start at 1.
`identifier` can be any identifier name inside your code (excluding Haxe keywords).
If you use a range specification for an entry under the `"all"` key, then checkstyle processes files matching that entry but the specifiedd range will be excluded from every check (as long as the check supports exclusion/suppression).

```json
{
    "version": 1,
    "path": "RELATIVE_TO_SOURCE",
    "all": [
      "checkstyle/checks/Checks"
    ],
    "Dynamic": [
        "checkstyle/Main",
        "checkstyle/Checker:105"
        "checkstyle/Checker:25-37"
        "checkstyle/Checker:createContext"
    ],
    "MultipleStringLiterals": [
        "checks",
        "token"
    ],
    "NestedForDepth": [
        "TestMain"
    ],
    "MemberName": [
        "checkstyle/Main"
    ]
}
```

The path option needs to be specified in order to use file paths. Exclude paths may be relative to the source (RELATIVE_TO_SOURCE) or project path (RELATIVE_TO_PROJECT). If no path option is given, the default is to see the excludes as regular expressions e.g. Test$ will match anything ending in Test.  

{{site.data.alerts.tip}} Exclude can either reside in rules JSON file or in a separate JSON file. If separate JSON file is used, it has to be passed using -e option.{{site.data.alerts.end}}

### Suppress warnings with inline annotations

An alternative way to exclude classes/methods using meta data.

`SuppressWarnings` is an useful feature when you want to omit a class/function/line from a specific check.

For example, if you have a class which has `Dynamic` usage and you want to omit that class from `Dynamic` check you can use `@SuppressWarnings` as show below.

```java
@SuppressWarnings("checkstyle:Dynamic")
```

You can also omit multiple checks.

```java
@SuppressWarnings(["checkstyle:Dynamic", "checkstyle:LineLength"])
```

{{site.data.alerts.important}} @SuppressWarnings may not work on all checks. {{site.data.alerts.end}}
---
title: Setup
tags: [setup, installation, configuration]
type: intro
toc: false
---

### Installation

```
haxelib install checkstyle
```

### Options

To see all the options available run the following command.

```
haxelib run checkstyle
```

```
[-s | --source] <path>    : Set source folder to process (multiple allowed)
[-c | --config] <path>    : Set config file (default: checkstyle.json)
[-e | --exclude] <path>   : Set exclude config file (default: checkstyle-exclude.json)
[-r | --reporter] <name>  : Set reporter (xml, json or text, default: text)
[-p | --path] <path>      : Set reporter output path
[-x | --xslt] <style>     : Set reporter style (XSLT)
[-progress]               : Show percentage progress
[-exitcode]               : Return number of failed checks in exitcode
[--list-checks]           : List all available checks and exit
[--list-reporters]        : List all available reporters and exit
[--default-config] <path> : Generate a default config and exit
[-nostyle]                : To omit styling in output summary
[-report]                 : Show report [DEPRECATED]
[-showMissingChecks]      : Show checks missing from active config
```

### Rules

The default configuration can be found [here](https://github.com/HaxeCheckstyle/haxe-checkstyle/blob/dev/resources/default-config.json).

It's recommended to define your own set of rules based on the needs of your project.

The library will automatically look for `checkstyle.json` at root level where all the rules and excludes can be defined.

The default severity for all checks can be defined using `defaultSeverity` property and can be overridden for each check as shown below.

The following is a sample `checkstyle.json` with 2 rules.

```json
{
    "defaultSeverity": "INFO",
    "checks": [
        {
            "type": "EmptyLines",
            "props": {
                "maxConsecutiveEmptyLines": 1
            }
        },
        {
            "type": "FileLength",
            "props": {
                "severity": "WARNING",
                "max": 2000
            }
        }
    ]
}
```

### Running Checkstyle

```
haxelib run checkstyle -s src
```

Multiple source folders can be defined as shown below:

```
haxelib run checkstyle -s src -s samples
```

### Exclude Packages/Classes

Classes/Packages can be excluded as shown below for each check:

```json
"exclude": {
    "all": [],
     "Dynamic": [
         "checkstyle.Main",
         "checkstyle.Checker"
     ],
     "MultipleStringLiterals": [
         "checks",
         "token"
     ],
     "NestedForDepth": [
         "TestMain"
     ],
     "MemberName": [
         "checkstyle.Main"
     ]
 }
```

{{site.data.alerts.note}} Exclude paths should be relative to the source paths specified. {{site.data.alerts.end}}

{{site.data.alerts.tip}} Exclude can either reside in rules JSON file or in a separate JSON file. If separate JSON file is used, it has to be passed using -e option.{{site.data.alerts.end}}

### Suppress Warnings

An alternative way to exclude classes/methods using meta data.

`SuppressWarnings` is an useful feature when you want to omit a class/function/line from a specific check.

For example, if you have a class which has `Dynamic` usage and you want to omit that class from `Dynamic` check you can use `@SuppressWarnings` as show below.

```java
@SuppressWarnings("checkstyle:Dynamic")
```

You can also omit multiple checks.

```java
@SuppressWarnings("checkstyle:Dynamic", "checkstyle:LineLength")
```

{{site.data.alerts.note}} Note that @SuppressWarnings may not work on all checks. {{site.data.alerts.end}}
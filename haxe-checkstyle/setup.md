---
title: Setup
toc: false
---

### Installation

```bash
haxelib install checkstyle
```

### Options

To see all the options available run the following command.

```bash
haxelib run checkstyle
```

```bash
Haxe Checkstyle v2.5.0
[-s | --source] <path>    : Set source path to process (multiple allowed)
[-c | --config] <path>    : Set config file (default: checkstyle.json)
[-e | --exclude] <path>   : Set exclude file (default: checkstyle-exclude.json)
[-r | --reporter] <name>  : Set reporter (xml, json or text, default: text)
[-p | --path] <path>      : Set reporter output path
[-x | --xslt] <style>     : Set reporter style (XSLT)
[--checkerthreads] <num>  : Sets the number of checker threads
[--default-config] <path> : Generate a default config and exit
[--detect] <path>         : Try to detect your coding style (experimental)
[--exitcode]              : Return number of failed checks in exitcode
[--list-checks]           : List all available checks and exit
[--list-reporters]        : List all available reporters and exit
[--nostyle]               : Omit styling in output summary
[--nothreads]             : Do not use checker threads
[--progress]              : Show percentage progress
[--show-missing-checks]   : Show checks missing from active config
[--show-parser-errors]    : Adds error messages for files that checkstyle fails to parse
```

### Rules

The default configuration can be found [here](https://github.com/HaxeCheckstyle/haxe-checkstyle/blob/dev/resources/default-config.json).

It's recommended to define your own set of rules based on the needs of your project.

The library will automatically look for `checkstyle.json` at root level where all the rules and excludes can be defined.

The default severity for all checks can be defined using `defaultSeverity` property and can be overridden for each check as shown below.

You can inherit a checkstyle configuration by using `extendsConfigPath` to point to a parent checkstyle json file. (available since 2.3.0)

The following is a sample `checkstyle.json` with 2 rules.

```json
{
    "defaultSeverity": "INFO",
    "extendsConfigPath": "parentCheckstyle.json",
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

### Automatically detect your coding style (available since 2.3.0)

Checkstyle can try to detect your coding style if you run it with `-detect <path>` (Warning: will overwrite `<path>`).
e.g.:

```bash
haxelib run checkstyle -s src --detect myCheckstyle.json
```

see [Automatic detection of coding style](autodetect.html)

### Running Checkstyle

```bash
haxelib run checkstyle -s src
```

Multiple source folders can be defined as shown below:

```bash
haxelib run checkstyle -s src -s samples
```

### Exclude Packages/Classes/Code fragments

see [Excluding code from checkstyle](excludeconfig.html)

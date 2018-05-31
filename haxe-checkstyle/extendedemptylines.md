---
title: Extended Empty Lines
toc: false
---

Checks for consecutive empty lines. (available since 2.4.0)

### Configuration

```json
{
    "type": "EmptyLines",
    "props": {
        "defaultPolicy": "none",
        "ignore": [],
        "none": [
          "beginClass",
          "betweenImports"
        ],
        "exact": [
          "afterPackage",
          "afterImports"
        ],
        "upto": [],
        "atleast": [],
        "max": 1,
        "skipSingleLineTypes": true,
        "severity": "INFO"
    }
}
```

`max` defines the number of empty lines for `exact`, `upto` and `atleast` policies.
To ignore single line typ definitions set `skipSingleLineTypes` to `true`.
`defaultPolicy` defines the policy to use for all places that are not listed in `ignore`, `none`, `exact`, `upto` and `atleast` arrays.

| defaultPolicy  |                                                    |
| -------------- | -------------------------------------------------- |
| `ignore`       | ignores all entries                                |
| `none`         | no empty line allowed                              |
| `exact`        | exactly `max` empty line(s) required               |
| `upto`         | up to `max` empty line(s) allowed (0 - `max`)      |
| `atleast`      | at least `max` empty lines required                |

`ignore`, `none`, `exact`, `upto` and `atleast` arrays must contain places from the following table:

| places                       |                                                            |
| ---------------------------- | ---------------------------------------------------------- |
| `beforePackage`              | before package                                             |
| `afterPackage`               | after package                                              |
| `betweenImports`             | between imports/usings                                     |
| `beforeUsing`                | before using block                                         |
| `afterImports`               | after all imports/usings                                   |
| `anywhereInFile`             | anywhere in file                                           |
| `betweenTypes`               | betgween two types                                         |
| `beforeFileEnd`              | before EOF                                                 |
| `inFunction`                 | anywhere inside function body                              |
| `afterLeftCurly`             | after left curly                                           |
| `beforeRightCurly`           | before right curly                                         |
| `typeDefinition`             | between type and left curly                                |
| `beginClass`                 | after class left curly                                     |
| `endClass`                   | before class right curly                                   |
| `afterClassStaticVars`       | after static class var block                               |
| `afterClassVars`             | after class var block                                      |
| `betweenClassStaticVars`     | between static class vars                                  |
| `betweenClassVars`           | between class vars                                         |
| `betweenClassMethods`        | between class methods                                      |
| `beginAbstract`              | after abstract left curly                                  |
| `endAbstract`                | before abstract right curly                                |
| `afterAbstractVars`          | after abstract var block                                   |
| `betweenAbstractVars`        | between abstract vars                                      |
| `betweenAbstractMethods`     | between abstract methods                                   |
| `beginInterface`             | after interface left curly                                 |
| `endInterface`               | before interface right curly                               |
| `betweenInterfaceFields`     | between interface fields                                   |
| `beginEnum`                  | after enum left curly                                      |
| `endEnum`                    | before enum right curly                                    |
| `betweenEnumFields`          | between enum fields                                        |
| `beginTypedef`               | after typedef left curly                                   |
| `endTypedef`                 | before typedef right curly                                 |
| `betweenTypedefFields`       | between typedef fields                                     |
| `afterSingleLineComment`     | after single line comment                                  |
| `afterMultiLineComment`      | after multi line comment                                   |

---
title: Extended Empty Lines
toc: false
---

Checks for consecutive empty lines. (available since 2.4.0)

### Configuration

```json
{
    "type": "ExtendedEmptyLines",
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
| `afterAbstractVars`          | after abstract var block                                   |
| `afterClassStaticVars`       | after static class var block                               |
| `afterClassVars`             | after class var block                                      |
| `afterImports`               | after all imports/usings                                   |
| `afterLeftCurly`             | after left curly                                           |
| `afterMultiLineComment`      | after multi line comment                                   |
| `afterPackage`               | after package                                              |
| `afterSingleLineComment`     | after single line comment                                  |
| `anywhereInFile`             | anywhere in file                                           |
| `beforePackage`              | before package                                             |
| `beforeRightCurly`           | before right curly                                         |
| `beforeUsing`                | before using block                                         |
| `beginAbstract`              | after abstract left curly                                  |
| `beginClass`                 | after class left curly                                     |
| `beginEnum`                  | after enum left curly                                      |
| `beforeFileEnd`              | before EOF                                                 |
| `beginInterface`             | after interface left curly                                 |
| `beginTypedef`               | after typedef left curly                                   |
| `betweenAbstractMethods`     | between abstract methods                                   |
| `betweenAbstractVars`        | between abstract vars                                      |
| `betweenClassMethods`        | between class methods                                      |
| `betweenClassStaticVars`     | between static class vars                                  |
| `betweenClassVars`           | between class vars                                         |
| `betweenEnumFields`          | between enum fields                                        |
| `betweenImports`             | between imports/usings                                     |
| `betweenInterfaceFields`     | between interface fields                                   |
| `betweenTypedefFields`       | between typedef fields                                     |
| `betweenTypes`               | betgween two types                                         |
| `endClass`                   | before class right curly                                   |
| `endAbstract`                | before abstract right curly                                |
| `endInterface`               | before interface right curly                               |
| `endEnum`                    | before enum right curly                                    |
| `endTypedef`                 | before typedef right curly                                 |
| `inFunction`                 | anywhere inside function body                              |
| `typeDefinition`             | between type and left curly                                |

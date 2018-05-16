---
title: Automatic detection of coding style
toc: false
---

### Automatically detect your coding style (available since 2.3.0)

Checkstyle can try to detect your coding style if you run it with `-detect <path>` (Warning: will overwrite `<path>`).
e.g.:
```
haxelib run checkstyle -s src -detect myCheckstyle.json
```

Auto detection is meant as a starting point, helping you to set up a basic configuration, that you can then modify to make it work with your coding style.

It works by running these checks with different configuration options on your source folder and selecting options with the least amount of checkstyle violations.
For each check and each single property value detection will stop going through your files as soon as it finds a difference in checkstyle violations. 

Since each check runs multiple times and many checks need to look at more than one file, it may take some time to complete a detection run (especially when running though neko). So using a small set of source files produces quicker results, but they might not contain all relevant cases, so you can end up with a less perfect configuration. Though, using your full source code is not a real guarantee for a flawless detection. 
Most likely you will have to adjust configuration settings and you might need to disable checks that don't apply to you. Some checks like e.g. TODOComment, Dyanmic, TrailingWhitespace or Trace have no real options, so checkstyle's auto detection includes them regardless of whether they apply to you or nor (because the only real option is to not use them).


| Checks supported by automatic detection:               |
| ------------------------------------------------------ |
| [Anonymous](anonymous.html)                            |
| [ArrayAccess](arrayaccess.html)                        |
| [AvoidStarImport](avoidstarimport.html)                |
| [ConditionalCompilation](conditionalcompilation.html)  |
| [ConstantName](constantname.html)                      |
| [CyclomaticComplexity](cyclomaticcomplexity.html)      |
| [Dynamic](dynamic.html)                                |
| [EmptyLines](emptylines.html)                          |
| [EmptyPackage](emptypackage.html)                      |
| [FileLength](filelength.html)                          |
| [HiddenField](hiddenfield.html)                        |
| [Indentation](indentation.html)                        |
| [IndentationCharacter](indentationcharacter.html)      |
| [InnerAssignment](innerassignment.html)                |
| [Interface](interface.html)                            |
| [LeftCurly](leftcurly.html)                            |
| [LineLength](linelength.html)                          |
| [MethodCount](methodcount.html)                        |
| [MethodLength](methodlength.html)                      |
| [NestedForDepth](nestedfordepth.html)                  |
| [NestedIfDepth](nestedifdepth.html)                    |
| [NestedTryDepth](nestedtrydepth.html)                  |
| [NullableParameter](nullableparameter.html)            |
| [OperatorWhitespace](operatorwhitespace.html)          |
| [OperatorWrap](operatorwrap.html)                      |
| [ParameterNumber](parameternumber.html)                |
| [RedundantModifier](redundantmodifier.html)            |
| [Return](return.html)                                  |
| [ReturnCount](returncount.html)                        |
| [RightCurly](rightcurly.html)                          |
| [SeparatorWhitespace](separatorwhitespace.html)        |
| [SeparatorWrap](separatorwrap.html)                    |
| [Spacing](spacing.html)                                |
| [StringLiteral](stringliteral.html)                    |
| [TODOComment](todocomment.html)                        |
| [Trace](trace.html)                                    |
| [TrailingWhitespace](trailingwhitespace.html)          |
| [Type](type.html)                                      |
| [UnnecessaryConstructor](unnecessaryconstructor.html)  |
| [UnusedImport](unusedimport.html)                      |
| [UnusedLocalVar](unusedlocalvar.html)                  |

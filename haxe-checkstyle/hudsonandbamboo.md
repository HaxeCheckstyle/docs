---
title: Hudson, Jenkins & Bamboo
toc: false
---

Checkstyle has `xml` report option that can be used to integrate with Hudson, Jenkins and Bamboo.

If you want to style the generated XML you can set XSLT style for the XML generated. See the sample below.

```
haxelib run checkstyle -s src -c config.json -r xml -p report.xml -x report.xsl
```

### Configure Jenkins

You'll need the [Checkstyle Plugin](https://wiki.jenkins.io/display/JENKINS/Checkstyle+Plugin) installed.

Add the Post-build Action: "Publish Checkstyle analysis results" to ingest the generated `xml` report on your Jenkins job.

### Sample Trend Chart

![img](images/hudson.png)

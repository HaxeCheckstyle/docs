---
title: Hudson & Bamboo
keywords: hudson, bamboo, integration
toc: false
---

Checkstyle has `xml` report option that can be used to integrate with Hudson and Bamboo.

If you want to style the generated XML you can set XSLT style for the XML generated. See the sample below.

```java
haxelib run checkstyle -s src -c config.json -p report.xml -x report.xsl
```
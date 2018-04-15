---
title: About
toc: false
homepage: true
---

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](http://opensource.org/licenses/MIT)
[![Release](https://img.shields.io/github/release/HaxeCheckstyle/haxe-checkstyle.svg)](http://lib.haxe.org/p/checkstyle/)
[![Build Status](https://travis-ci.org/HaxeCheckstyle/haxe-checkstyle.svg)](https://travis-ci.org/HaxeCheckstyle/haxe-checkstyle)
[![Codecov](https://img.shields.io/codecov/c/github/HaxeCheckstyle/haxe-checkstyle.svg)](https://codecov.io/github/HaxeCheckstyle/haxe-checkstyle?branch=dev)
[![Code Climate](https://codeclimate.com/github/HaxeCheckstyle/haxe-checkstyle/badges/gpa.svg)](https://codeclimate.com/github/HaxeCheckstyle/haxe-checkstyle)
[![Code Climate Issues](https://img.shields.io/codeclimate/issues/github/HaxeCheckstyle/haxe-checkstyle.svg)](https://codeclimate.com/github/HaxeCheckstyle/haxe-checkstyle/issues)
[![Gitter chat](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/HaxeCheckstyle/haxe-checkstyle)
[![Support Haxe Checkstyle on Patreon](http://www.waudjs.com/images/patreon_btn.png)](https://www.patreon.com/adireddy)

**Haxe Checkstyle** is a static analysis tool to help developers write Haxe code that adheres to a coding standard.

It automates the process of checking Haxe code to spare developers of this boring (but important) task.

Code conventions improve readability, allowing team members to understand each other's code better.

Ideal for any project that wants to enforce coding conventions.

Static analysis is usually performed as part of a code review.

{{site.data.alerts.callout_info}} Static analysis also called "static code analysis" or "white-box testing", is a way of examining the code without executing it. The process provides an understanding of the code structure, and can help to ensure that the code adheres to industry standards. {{site.data.alerts.end}}

{{site.data.alerts.callout_info}} The principal advantage of static analysis is the fact that it can reveal errors that do not manifest themselves until a disaster occurs weeks, months or years after release. Nevertheless, static analysis is only a first step in a comprehensive software quality-control regime. After the static analysis has been done, dynamic analysis is often performed in an effort to uncover subtle defects or vulnerabilities. {{site.data.alerts.end}}

{{site.data.alerts.callout_danger}} Static analysis tool can sometimes warn you about odd fragments. It means that the code can actually be quite correct. It is called false-positive reports. Only the developer can understand if the analyzer points to a real error or it is just a false positive. {{site.data.alerts.end}}

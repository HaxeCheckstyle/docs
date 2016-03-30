---
title: About
tags: [about, checkstyle, static analysis, coding standards]
audience: all
type: intro
toc: false
homepage: true
---

![logo](https://raw.githubusercontent.com/HaxeCheckstyle/haxe-checkstyle/dev/resources/logo.png)

[![License](https://img.shields.io/badge/license-MIT-blue.svg?style=flat)](http://opensource.org/licenses/MIT)
[![Build Status](https://travis-ci.org/HaxeCheckstyle/haxe-checkstyle.svg?branch=master)](https://travis-ci.org/HaxeCheckstyle/haxe-checkstyle)
[![codecov.io](https://codecov.io/github/HaxeCheckstyle/haxe-checkstyle/coverage.svg?branch=dev)](https://codecov.io/github/HaxeCheckstyle/haxe-checkstyle?branch=dev)
[![Code Climate](https://codeclimate.com/github/HaxeCheckstyle/haxe-checkstyle/badges/gpa.svg)](https://codeclimate.com/github/HaxeCheckstyle/haxe-checkstyle)
[![Issue Count](https://codeclimate.com/github/HaxeCheckstyle/haxe-checkstyle/badges/issue_count.svg)](https://codeclimate.com/github/HaxeCheckstyle/haxe-checkstyle)
[![Version](https://img.shields.io/badge/haxelib-v2.1.1-EA8220.svg)](http://lib.haxe.org/p/checkstyle/)
[![Gitter chat](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/HaxeCheckstyle/haxe-checkstyle)

**Haxe Checkstyle** is a static analysis tool to help developers write Haxe code that adheres to a coding standard.

It automates the process of checking Haxe code to spare developers of this boring (but important) task.

Code conventions improve readability, allowing team members to understand each other's code better.

Ideal for any project that wants to enforce coding conventions.

Static analysis is usually performed as part of a code review.

{{site.data.alerts.callout_info}} Static analysis also called "static code analysis" or "white-box testing", is a way of examining the code without executing it. The process provides an understanding of the code structure, and can help to ensure that the code adheres to industry standards. {{site.data.alerts.end}}

{{site.data.alerts.callout_info}} The principal advantage of static analysis is the fact that it can reveal errors that do not manifest themselves until a disaster occurs weeks, months or years after release. Nevertheless, static analysis is only a first step in a comprehensive software quality-control regime. After the static analysis has been done, dynamic analysis is often performed in an effort to uncover subtle defects or vulnerabilities. {{site.data.alerts.end}}

{{site.data.alerts.callout_danger}} Static analysis tool can sometimes warn you about odd fragments. It means that the code can actually be quite correct. It is called false-positive reports. Only the developer can understand if the analyzer points to a real error or it is just a false positive. {{site.data.alerts.end}}

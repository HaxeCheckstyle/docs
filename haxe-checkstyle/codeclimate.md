---
title: Codeclimate
keywords: codeclimate, integration
toc: false
---

### .codeclimate.yml

```yml
engines:
  haxe-checkstyle:
    enabled: true

exclude_paths:
  - resources/**/*

ratings:
  paths:
    - "**.hx"

```
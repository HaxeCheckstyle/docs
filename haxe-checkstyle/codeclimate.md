---
title: Codeclimate
keywords: codeclimate, integration
toc: false
---

### Example .codeclimate.yml

Below is an example `.codeclimate.yml` with `haxe-checkstyle` engine enabled.

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

[Click here](https://docs.codeclimate.com/docs/ratings) to see how ratings work.

### GitHub Integration

- [Pull Request Integration](https://docs.codeclimate.com/docs/github-pull-request-integration)
- [Issues Integration](https://docs.codeclimate.com/docs/github-issues-integration)
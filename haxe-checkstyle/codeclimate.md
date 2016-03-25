---
title: Code Climate
keywords: codeclimate, integration
toc: false
---

Create `.codeclimate.yml` and place it in your root directory.

The engine will automatically pick up `checkstyle.json` configuration if it's available in the root directory.

It's highly recommended to define your own set of rules in the configuration file based on the needs of your project.

### Example .codeclimate.yml

Below is an example `.codeclimate.yml` with `haxe-checkstyle` engine enabled.

```yml
engines:
  haxe-checkstyle:
    enabled: true

exclude_paths:
  - test/**/*

ratings:
  paths:
    - "**.hx"

```

You can add multiple engines in `.codeclimate.yml`. [Click here](https://docs.codeclimate.com/docs/list-of-engines) to see all available engines in Code Climate.

[Click here](https://docs.codeclimate.com/docs/excluding-files-and-folders) for more information on excluding files and folders.

[Click here](https://docs.codeclimate.com/docs/ratings) to see how ratings work.

### GitHub Integration

- [Pull Request Integration](https://docs.codeclimate.com/docs/github-pull-request-integration)
- [Issues Integration](https://docs.codeclimate.com/docs/github-issues-integration)
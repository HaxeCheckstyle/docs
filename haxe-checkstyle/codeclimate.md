---
title: Code Climate
toc: false
---

Haxe Checkstyle is available on the [Code Climate platform](https://docs.codeclimate.com/docs/haxe-checkstyle) (free for open source projects).

It requires a `.codeclimate.yml` file and an optional but recommended `checkstyle.json` file to be added to the root of your repository.

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

You can add multiple [engines](https://docs.codeclimate.com/docs/list-of-engines) in `.codeclimate.yml`.

[Click here](https://docs.codeclimate.com/docs/excluding-files-and-folders) for more information on excluding files and folders.

[Click here](https://docs.codeclimate.com/docs/ratings) to see how ratings work.

### GitHub Integration

Immediate results, right in your pull requests.

![img](https://codeclimate.com/marketing/images/features/pull_requests-67ad7029.png)

More information:

- [Pull Request Integration](https://docs.codeclimate.com/docs/github-pull-request-integration)
- [Issues Integration](https://docs.codeclimate.com/docs/github-issues-integration)

# pre-commit-uv-action

[![Build Status](https://github.com/akx/pre-commit-uv-action/actions/workflows/test.yml/badge.svg)](https://github.com/akx/pre-commit-uv-action/actions/workflows/test.yml)

A GitHub action to run [pre-commit] using [uv] via [setup-uv] and [pre-commit-uv].

## Workflow template

```yaml
name: pre-commit

on:
  pull_request:
  push:
    branches:
      - main

jobs:
  lint:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      - uses: akx/pre-commit-uv-action@v0.1.0
```

[pre-commit]: https://pre-commit.com
[pre-commit-uv]: https://github.com/tox-dev/pre-commit-uv
[uv]: https://github.com/astral-sh/uv
[setup-uv]: https://github.com/astral-sh/setup-uv

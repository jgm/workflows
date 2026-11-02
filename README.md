# Some reusable workflows

## haskell-ci.yml

A generic Haskell CI build on linux (with several ghc versions) and windows.
To use, provide the following in `.github/workflows/ci.yml`:

```yaml
name: CI tests

on:
  push:
    branches: [main]
    tags: ['*']
  pull_request:
  workflow_dispatch:

jobs:
  ci:
    uses: jgm/workflows/.github/workflows/haskell-ci.yml@main
```

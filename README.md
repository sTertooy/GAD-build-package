# gda-build-pkg

This GitHub action builds the GAP package located in the current directory. Based on [gap-actions/build-pkg](https://github.com/gap-actions/build-pkg).


## Usage

This action can be optionally called in the workflow of a GAP package to compile said package.

### Example

```yaml
name: CI

on:
  - push
  - pull_request
  - workflow_dispatch

jobs:
  build:
    name: "Build the GAP package"
    runs-on: ubuntu-latest

    container:
      image: ghcr.io/stertooy/gda-image:master-slim

    steps:
      - uses: actions/checkout@v3
      - uses: stertooy/gda-build-pkg@v1
```

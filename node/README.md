# Github Action Node project

### Example

```
name: Main
on: [push]
jobs:
  build:
    name: Build
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: senolatac/sha-action/node/build@v9
  lint:
    name: Lint
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: senolatac/sha-action/node/lint@v9
```

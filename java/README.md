# Github Action Java project

### Example

```
name: Main
on: [push]
jobs:
  build_test:
    name: Build and Test
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: senolatac/sha-action/java/test@v8
  coverage:
    name: Upload Coverage Report
    needs: build_test
    if: github.ref != 'refs/heads/master'
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - uses: senolatac/sha-action/java/coverage@v8
        with:
          codacy-project-token: ${{ secrets.CODACY_PROJECT_TOKEN }}
```

# Pull request dependency checkout

This action checks if there is a pull request with the same title in the external repository.
Otherwise it checkouts the default branch.

## Usage

```yaml
on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4

      - uses: sreimers/pr-dependency-action@v1
        with:
          name: repo
          repo: https://github.com/external/repo.git
          secret: ${{ secrets.GITHUB_TOKEN }}
```

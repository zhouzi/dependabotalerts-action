# dependabotalerts-action

[![units-test](https://github.com/MTES-MCT/dependabotalerts-action/actions/workflows/test.yml/badge.svg)](https://github.com/MTES-MCT/dependabotalerts-action/actions/workflows/test.yml)

Github action that fetches Github dependabot security alerts and report results as JSON.

## Usage

First, you need to store your repository read-only token in repo secrets as `DEPENDABOTALERTS_TOKEN`.

```yaml
jobs:
  scan:
    runs-on: ubuntu-latest
    steps:
      - uses: "MTES-MCT/dependabotalerts-action@main"
        with:
          token: ${{ secrets.DEPENDABOTALERTS_TOKEN }}
          repositories: '["MTES-MCT/dashlord", "MTES-MCT/dependabotalerts-action"]'
          output: dependabotalerts.json
```

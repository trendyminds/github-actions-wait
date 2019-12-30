# Wait Action

## Required arguments

| Argument  | Description                                                                   |
|-----------|-------------------------------------------------------------------------------|
| `time`    | The duration to wait before moving to the next step. Example: `30s` or `2m`   |

## Usage

```yaml
name: Create Sandbox

on: pull_request

jobs:
  deploy:
    name: Deploy
    runs-on: ubuntu-latest

    steps:
      - name: Checkout code
        uses: actions/checkout@v1

      - name: Sleep for 30 seconds
        uses: trendyminds/github-actions-wait@master
        with:
          time: '30s'
```

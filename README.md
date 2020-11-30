# junit-report-annotations-action
Add check runs to your CI with annotations listing the test failures.

## Setup

```
- uses: turpif/junit-report-annotations-action@0.1.0
  if: always()
  with:
    access-token: ${{ secrets.GITHUB_TOKEN }}
```

## Parameters

| Name | Description | Default value |
| ---: | --- | --- |
| `access-token` | Mandatory Github token | You should set it to `${{ secrets.GITHUB_TOKEN }}` |
| `path` | Glob to JUnit XML files | `**/TEST-*.xml` |
| `numFailures` | Max number of failed tests to include (-1 for no limit) | `-1` (no limit) |
| `name` | Name of the Check in the GitHub Actions UI (if you use several times this action) | `JUnit Report` |

# Demonstration

Actions in this repository demonstrate what this GitHub Action is doing.

A successful run will look like

![Pass](docs/pass.png?raw=true)

A failed run will look like

![Fail](docs/fail.png?raw=true)

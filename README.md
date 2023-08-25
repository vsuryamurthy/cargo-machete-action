# Cargo Machete Action

A github action for cargo machete.

[Cargo machete](https://github.com/bnjbvr/cargo-machete) finds unused dependencies in your rust projects.

## Example usage

The step given by,
```
      - uses: vsuryamurthy/cargo-machete-action@v1
```
can be added to any workflow.

An example workflow is shown below:

```yaml
name: Cargo Machete
on:
  pull_request: { branches: "*" }

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout
        uses: actions/checkout@v3
      - name: Machete
        uses: vsuryamurthy/cargo-machete-action@v1
```

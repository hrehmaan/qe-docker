# Quantum ESPRESSO Docker Environment

This repository provides a Docker environment for building Quantum ESPRESSO from the official QEF GitLab repository.

Source repository: https://gitlab.com/QEF/q-e

## Build locally

```bash
docker build -t test_qef .
```

## Run the container

```bash
docker run -it -v $(pwd):/root/shared --rm -w /root/shared test_qef
```

## Test Quantum ESPRESSO

Inside the container, run:

```bash
which pw.x
pw.x -h
```

## Notes

The image currently builds Quantum ESPRESSO from the `develop` branch.
For better reproducibility, a fixed release tag is recommended for serious use.

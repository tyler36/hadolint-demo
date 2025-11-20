[![Dependabot Updates](https://github.com/tyler36/hadolint-demo/actions/workflows/dependabot/dependabot-updates/badge.svg)](https://github.com/tyler36/hadolint-demo/actions/workflows/dependabot/dependabot-updates)

# Hadolint <!-- omit in toc -->

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
  - [Docker](#docker)
- [Configuration](#configuration)
  - [Ignoring Rules](#ignoring-rules)

## Overview

Hadolint is a smarter Dockerfile linter that helps you build [best practice](https://docs.docker.com/engine/userguide/eng-image/dockerfile_best-practices) Docker images.

[Homepage](https://github.com/hadolint/hadolint)

## Installation

- Install [Hadolint](https://github.com/hadolint/hadolint)

  ```bash
  brew install hadolint
  ```

## Usage

- CLI

```shell
hadolint Dockerfile
```

### Docker

```shell
docker run --rm -i ghcr.io/hadolint/hadolint < Dockerfile
```

## Configuration

List of [rules](https://github.com/hadolint/hadolint/tree/master?tab=readme-ov-file#rules)

### Ignoring Rules

```dockerfile
# hadolint ignore=DL3003,DL3006,SC1035
FROM ubuntu

RUN cd /tmp && echo "foo"
```

# Docker images

[![Scheduled build (Ubuntu)](https://github.com/catthehacker/docker_images/actions/workflows/build-ubuntu.yml/badge.svg?event=schedule)](https://github.com/catthehacker/docker_images/actions/workflows/build-ubuntu.yml)
[![On-demand build (Ubuntu)](https://github.com/catthehacker/docker_images/actions/workflows/build-ubuntu.yml/badge.svg?event=workflow_dispatch)](https://github.com/catthehacker/docker_images/actions/workflows/build-ubuntu.yml)
[![Scheduled build (Alpine)](https://github.com/catthehacker/docker_images/actions/workflows/build-alpine.yml/badge.svg?event=schedule)](https://github.com/catthehacker/docker_images/actions/workflows/build-alpine.yml)
[![On-demand build (Alpine)](https://github.com/catthehacker/docker_images/actions/workflows/build-alpine.yml/badge.svg?event=workflow_dispatch)](https://github.com/catthehacker/docker_images/actions/workflows/build-alpine.yml)
[![Linter](https://github.com/catthehacker/docker_images/actions/workflows/lint.yml/badge.svg)](https://github.com/catthehacker/docker_images/actions/workflows/lint.yml)

## When updates will be applied to images

- A package that will be required for action(s) to work properly might be added/removed/changed
- Any maintenance that will be required due to:
  - Docker Hub
  - Quay
  - GitHub Container Registry
  - GitHub Actions
  - Act
- Performance and/or disk space improvements

## Images available

- [virtual-environments][catthehacker/runner-image] - GitHub Actions runner image containing all possible tools (image is extremely big, 20GB compressed, ~60GB extracted)
  - `catthehacker/ubuntu:full-20.04` - this image is updated manually due to amount of changes in [actions/virtual-environments][actions/virtual-environments]
  - more to come...
- [`/linux/ubuntu/runner/`](./linux/ubuntu/runner/) - `catthehacker/ubuntu:act-*` but with `runner` as user instead of `root`
  - docker.io (DockerHub)
    - `catthehacker/ubuntu:runner-16.04`
    - `catthehacker/ubuntu:runner-18.04`
    - `catthehacker/ubuntu:runner-20.04`
    - `catthehacker/ubuntu:runner-latest`
- [`/linux/ubuntu/act/`](./linux/ubuntu/act/) - image used in [github.com/nektos/act](https://github.com/nektos/act) as medium size image retaining compatibility with most actions while maintaining small size
  - docker.io (DockerHub)
    - `catthehacker/ubuntu:act-16.04`
    - `catthehacker/ubuntu:act-18.04`
    - `catthehacker/ubuntu:act-20.04`
    - `catthehacker/ubuntu:act-latest`
- [`/linux/alpine/act/`](./linux/alpine/act/) - Alpine base image for `act`
  - docker.io (DockerHub)
    - `catthehacker/alpine:act`
    - `catthehacker/alpine:runner`

## Repository contains parts of [`actions/virtual-environments`][actions/virtual-environments] which is licenced under ["MIT License"](https://github.com/actions/virtual-environments/blob/main/LICENSE)

[actions/virtual-environments]: https://github.com/actions/virtual-environments
[catthehacker/runner-image]: https://github.com/catthehacker/virtual-environments

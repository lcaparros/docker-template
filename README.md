# docker-<nameService>
Some amazing Docker images to work with <nameService> Out Of The Box

[![Docker Pulls](https://img.shields.io/docker/pulls/lcaparros/<nameService>.svg?color=4edafc&labelColor=555555&logoColor=ffffff&style=for-the-badge&label=pulls&logo=docker)](https://hub.docker.com/r/lcaparros/<nameService>)
[![Docker Stars](https://img.shields.io/docker/stars/lcaparros/<nameService>.svg?color=4edafc&labelColor=555555&logoColor=ffffff&style=for-the-badge&label=stars&logo=docker)](https://hub.docker.com/r/lcaparros/<nameService>)
[![GitHub](https://img.shields.io/static/v1.svg?color=4edafc&labelColor=555555&logoColor=ffffff&style=for-the-badge&label=lcaparros&message=GitHub&logo=github)](https://github.com/lcaparros "view the source for all of our repositories.")
[![GitHub Stars](https://img.shields.io/github/stars/lcaparros/docker-<nameService>.svg?color=4edafc&labelColor=555555&logoColor=ffffff&style=for-the-badge&logo=github)](https://github.com/lcaparros/docker-<nameService>)
[![GitHub Release](https://img.shields.io/github/release/lcaparros/docker-<nameService>.svg?color=4edafc&labelColor=555555&logoColor=ffffff&style=for-the-badge&logo=github)](https://github.com/lcaparros/docker-<nameService>/releases)
[![GitHub Repository](https://img.shields.io/static/v1.svg?color=4edafc&labelColor=555555&logoColor=ffffff&style=for-the-badge&label=lcaparros/docker-<nameService>&message=GitHub%20Repo&logo=github)](https://github.com/lcaparros/docker-<nameService>)

## How to push a new version of the image

```shell
$ docker build --build-arg VERSION=<version> --build-arg BUILD_DATE="$(date +%Y/%m/%dT%H:%M:%S)" -t <nameService> .
$ docker tag terraform lcaparros/<nameService>:<version>
$ docker push lcaparros/<nameService>:<version>
```

## Usage

It is necessary to share a volume to the current directory to make the necessary <nameService> files available for the Docker container (use the `/files` volume in the container). A good way to use this image could be to create a new alias in your bash_profile file:

```shell
alias <nameService>='docker run --rm -it -v $(pwd):/files lcaparros/<nameService>:<version>'
```

Now you could just type `<nameService>` in the CLI and it will work as the real <nameService> binary.
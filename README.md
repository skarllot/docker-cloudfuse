# Cloudfuse Dockerfile

Dockerfile to build a Cloudfuse container image.

## Version

Current version: git-21358f159d

## Installation

Pull the latest version of the image from the docker index. This is the
recommended method of installation as it is easier to update image in the
future.

```
docker pull skarllot/cloudfuse:latest
```

Alternately you can build the image from source.

```
git clone https://github.com/skarllot/docker-cloudfuse.git
cd docker-cloudfuse
docker build -t="$USER/cloudfuse" .
```

## Quick Start

To run the Cloudfuse image you need to provide a configuration file. To create
the configuration file follow the instructions from
[Cloudfuse README](https://github.com/redbo/cloudfuse/blob/master/README).

Name the configuration file as `config` and move it to `/var/cloudfuse`
directory.

```
docker run --name=cloudfuse -d \
    -v /var/cloudfuse:/var/cloudfuse \
    skarllot/cloudfuse:latest
```


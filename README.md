# docker-ffmpeg

[![Latest Github release](https://img.shields.io/github/release/rugarci/docker-ffmpeg.svg)](https://github.com/rugarci/docker-ffmpeg/releases/latest)
[![Image size](https://img.shields.io/docker/image-size/rugarci/ffmpeg)](https://hub.docker.com/r/rugarci/ffmpeg)
[![Docker Pulls](https://img.shields.io/docker/pulls/rugarci/ffmpeg.svg)](https://hub.docker.com/r/rugarci/ffmpeg/)

Alpine image with ffmpeg and bash

Tested on Raspberry Pi 3, 4 

## Usage


For Docker compose

```yaml
  ffmpeg:
    image: rugarci/ffmpeg:dev
    entrypoint: bash -c "while true; do /data/run.sh; sleep 300; done"
    container_name: ffmpeg
    environment:
      PUID: 1000
      PGID: 1000
    volumes:
      - "/etc/timezone:/etc/timezone:ro"
      - "/etc/localtime:/etc/localtime:ro"
      - ffmpegVol:/data
    restart: always

```

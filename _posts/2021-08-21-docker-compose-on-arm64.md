---
layout: post
title: Install on docker compose on arm64
subtitle: docker-compose is a Docker CLI plugin
categories: docker
tags: [docker, docker-compose]
---
특이점
1. docker-compose is a Docker CLI plugin
2. `~/.docker/cli-plugins` 먼저 만들어야 함
3. OCI에서 uname -m을 하면 aarch64가 나오므로 매뉴얼로 url을 찾아줘야함
4. 커맨드가 docker-compose에서 docker compose로 바뀜

성공 Docker compose on arm64
```
1. mkdir -p ~/.docker/cli-plugins
2. sudo curl -L "https://github.com/docker/compose-cli/releases/download/v2.0.0-rc.1/docker-compose-linux-arm64" -o ~/.docker/cli-plugins/docker-compose
3. chmod +x ~/.docker/cli-plugins/docker-compose
```

기존에러 이유 (도커 공식 홈페이지)
```
1. sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
2. sudo chmod +x /usr/local/bin/docker-compose
```
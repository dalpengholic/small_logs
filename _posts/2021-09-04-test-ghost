---
layout: post
title: Ghost on arm server
subtitle: 
categories: Ghost
tags: [Ghost, docker]
---
실패1.
- docker run -d --name some-ghost arm64v8/ghost

성공1.
- security rule: open 3001 ingress
- docker run -d --name some-ghost -e url=http://localhost:3001 -p 3001:2368 arm64v8/ghost

성공2.
- security rule: open 3001 ingress
- security rule: open 3002 ingress
- docker run -d --name some-ghost1 -e url=http://localhost:3001 -p 3001:2368 arm64v8/ghost
- docker run -d --name some-ghost2 -e url=http://localhost:3001 -p 3001:2368 arm64v8/ghost

성공3.
- security rule: open 2368 ingress
- docker run -d --name some-ghost -e url=http://localhost:2368 -p 2368:2368 arm64v8/ghost

성공4.
- security rule: open 3003 ingress
- docker run -d --name some-ghost5 -p 3003:2368 arm64v8/ghost

성공5.
- docker run -d --name some-ghost -p 3001:2368 -v /path/to/ghost/blog:/var/lib/ghost/content arm64v8/ghost:alpine

성공6.
- docker run -d --name some-ghost1 -p 3001:2368 -v some-ghost1-data:/var/lib/ghost/content arm64v8/ghost
- docker run -d --name some-ghost2 -p 3002:2368 -v some-ghost2-data:/var/lib/ghost/content arm64v8/ghost

성공7.
- [link](https://blog.ssdnodes.com/blog/docker-backup-volumes/)
- mkdir ~/backup
- docker run --rm --volumes-from some-ghost1 -v ~/backup:/backup ubuntu bash -c "cd /var/lib/ghost/content && tar cvf /backup/ghost.tar ."

---
layout: post
title: Golang package
subtitle: 
categories: Golang
tags: [Golang, package]
---
고랭 패키지 관련

```
MainFolder
 |
 | main.go (package mainFolder)
 | go.mod
 |
 --SubFolder (package subFolder)
   |
   | sub.go
```

위와 같은 구조의 경우 
1. 최상위 폴더서 go mod init blahblah/mainfolder 혹은 go mod init mainfolder
2. main.go 에서 import시 `mainFolder/subFolder` 

최상위 폴더서 go mod init을 하게 되면 그 하위에 있는 것들은 모듈의 일부로 파악하는듯

---
layout: post
title: Golang package 2
subtitle: 
categories: Golang
tags: [Golang, package]
---
고랭 패키지 관련

하나의 폴더 밑에 두개의 go 파일을 같은 이름의 페키지로 묶어도 잘 불러온다

```
MainFolder
 |
 | main.go (package mainFolder)
 | go.mod
 |
 --SubFolder (package subFolder)
   |
   | sub.go
   | sub2.go
```

위와 같은 구조의 경우 
1. 최상위 폴더서 go mod init blahblah/mainfolder 혹은 go mod init mainfolder
2. main.go 에서 import시 `mainFolder/subFolder` 

그러면 sub.go 그리고 sub2.go에 있는 블럭을 모두 사용가능

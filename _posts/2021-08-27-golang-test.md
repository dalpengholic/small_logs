---
layout: post
title: Golang test 1
subtitle: Golang test command
categories: Golang
tags: [Golang, test]
---
Create a coverage report

```Shell
go test -coverprofile=coverage.out
tag.ItemTag
PASS
coverage: 100.0% of statements
```

See in html format
```Shell
go tool cover -html=coverage.out
```

Test at the current folder
```Shell
$  go test .

ok      gomarket/tag    0.006s
```

Test verbose?
```Shell
$  go test -v

=== RUN   TestNewTag
tag.ItemTag
--- PASS: TestNewTag (0.00s)
PASS
ok      gomarket/tag    0.006s
```